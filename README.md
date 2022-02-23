# Spamer in c#-
My First Repository in GitHub;
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace spamerwat
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            //Run
            richTextBox1.Enabled = false;
            timer1.Start();
            //Run
        }

        private void button2_Click(object sender, EventArgs e)
        {
            //Stop
            richTextBox1.Enabled=true;
            timer1.Stop();
            //Stop
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            //Timer
            SendKeys.Send(richTextBox1.Text);
            SendKeys.Send("{ENTER}");
            //Timer
        }
    }
}
