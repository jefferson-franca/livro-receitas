**** Controle Inserção campos (ideia de como fazer) *******


namespace abc.xyz
{
    class intTextBox : TextBox
    {
        protected override void OnKeyDown(System.Windows.Forms.KeyEventArgs e)
        {
            if (e.KeyCode == Keys.NumPad0 || e.KeyCode == Keys.NumPad1 || e.KeyCode == Keys.NumPad2
                || e.KeyCode == Keys.NumPad3 || e.KeyCode == Keys.NumPad4 || e.KeyCode == Keys.NumPad5
                || e.KeyCode == Keys.NumPad6 || e.KeyCode == Keys.NumPad7 || e.KeyCode == Keys.NumPad8
                || e.KeyCode == Keys.NumPad9
                || e.KeyCode == Keys.D0 || e.KeyCode == Keys.D1 || e.KeyCode == Keys.D2 || e.KeyCode == Keys.D3
                || e.KeyCode == Keys.D4 || e.KeyCode == Keys.D5 || e.KeyCode == Keys.D6 || e.KeyCode == Keys.D7
                || e.KeyCode == Keys.D8 || e.KeyCode == Keys.D9 
                || e.KeyCode == Keys.Delete || e.KeyCode == Keys.Enter || e.KeyCode == Keys.Back
                || e.KeyCode == Keys.Tab
                || e.KeyCode == Keys.Left  || e.KeyCode == Keys.Right || e.KeyCode == Keys.Up || e.KeyCode == Keys.Down
                || e.KeyCode == Keys.End || e.KeyCode == Keys.Home || e.KeyCode == Keys.PageDown || e.KeyCode == Keys.PageUp)
            {
                e.SuppressKeyPress = false;
            }
            else
            {
                e.SuppressKeyPress = true;
            }
        }

        protected override void OnGotFocus(EventArgs e)
        {
            base.OnGotFocus(e);
            this.BackColor = Color.Yellow;
        }

        protected override void OnLostFocus(EventArgs e)
        {
            base.OnLostFocus(e);
            this.BackColor = Color.Empty;
        }
    }
} 


Editado