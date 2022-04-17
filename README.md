# Studentdetails.java
Student details login
import java.awt.*;
import java.awt.event.*;
public class student extends Frame implements ActionListener
 {
     TextField t1,t2,t3;
     TextArea t4;
     Label l1,l2,l3;
     Button b1,b2;
     student()
     {
      l1 = new Label("Enter Name");
      l2 = new Label("Enter Number");
      l3 = new Label("Enter Address");
    
      t1 = new TextField(20);
      t2 = new TextField(20);
      t3 = new TextField(20);
      t4 = new TextArea("");
      b1 = new Button("Submit");
      b2 = new Button("Clear");
      setLayout (new GridLayout(6,2));
      add(l1);
      add(t1);
      add(l2);
      add(t2);
      add(l3);
      add(t3);
    
      add(b1);
      add(b2);
      add(t4);
      b1.addActionListener(this);
      b2.addActionListener(this);
      setVisible(true);
      setSize(200,200);
      addWindowListener(new WindowAdapter()
      {
          public void windowClosing(WindowEvent we)
          {
              System.exit(0);
            }
        });

     
    }
    public static void main(String args[])
    {
        new student();
    }
    public void actionPerformed(ActionEvent ae)
    {
        String result;
        StringBuilder str;
        if(ae.getSource()==b1)
        {
            String sdetails = " Enter Name  " + t1.getText() + "Enter Number" + t2.getText() + "Enter Address " + t3.getText();
            t4.setText(sdetails);
        
        }
        else
        {
            t1.setText("");
            t2.setText("");
            t3.setText("");
        }
    }
    
}
