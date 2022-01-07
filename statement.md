# Welcome!

This C# template lets you get started quickly with a simple one-page playground.

```C# runnable
using System;
using System.Drawing;
using Syste.Windows.Form

class Vector3{
    public int x;
    public int y;
    public int z;

    public Vector3(int x, int y, int z)
    {
        this.x = x;
        this.y = y;
        this.z = z;
    }
}

class Hello : Form
{
    static void Main() 
    {

        Console.WriteLine("Hello World!");

        Vector3 Position = new Vector3();

        Application.Run(new WinFormExample());
    }

    private Button button;

    public WinFormExample() {
        DisplayGUI();
    }

    private void DisplayGUI() {
        this.Name = "WinForm Example";
        this.Text = "WinForm Example";
        this.Size = new Size(150, 150);
        this.StartPosition = FormStartPosition.CenterScreen;

        button = new Button();
        button.Name = "button";
        button.Text = "Click Me!";
        button.Size = new Size(this.Width - 50, this.Height - 100);
        button.Location = new Point(
        (this.Width - button.Width) / 3 ,
        (this.Height - button.Height) / 3);
        button.Click += new System.EventHandler(this.MyButtonClick);

        this.Controls.Add(button);
    }

    private void MyButtonClick(object source, EventArgs e) {
        MessageBox.Show("My First WinForm Application");
    }

}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C# template](https://tech.io/select-repo/386)
