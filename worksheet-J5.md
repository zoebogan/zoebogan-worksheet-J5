# Questions
## Zoe Bogan

1. A GUI relies on the operating system to handle processes like clicking with a mouse. It also implements a java swing class that enables information hiding, encapsulation, and idea of abstract and inheritance.

2. ```WindowListener``` adds events and functionality to a GUI and ```WindowAdapter``` is a Java API that implements ```WindowListener```.

3. ![J5_Q3](https://github.com/user-attachments/assets/fbaab9ea-98eb-4141-90d3-f35e7ff4702d)

4.  ```jbutton.setText(...)``` used to update the text and can add a count. 

5.  ```java
    public class RedPillBluePill extends JFrame {
      JLabel label;

      public RedPillBluePill() {
          this.setSize(300, 300);
          this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

          JPanel panel = new JPanel(new BorderLayout());        
          JButton red = new JButton("red");
          JButton blue = new JButton("blue");
          panel.add(red, BorderLayout.EAST);
          panel.add(blue, BorderLayout.WEST);
          label = new JLabel("click a button");
          this.add(label, BorderLayout.NORTH);
          this.add(panel, BorderLayout.SOUTH);

          red.addActionListener((e) -> {
                if (l.getText().equals("RED")) {
                    l.setText("BLUE");
                } else {
                    l.setText("RED");
                }
            });

          blue.addActionListener((e) -> {
                if (l.getText().equals("BLUE")) {
                    l.setText("RED");
                } else {
                    l.setText("BLUE");
                }
           });
        }
    }
    ```
   
6. Lambda expressions only work if there is a single method to implement. So ```ActionListener``` can implement Lambda expressions because it is only using a single method.  

7. ```java
    import javax.swing.*;
    import java.awt.*;
    import java.util.*;

    public class J5_Problem7 {
        public static void main(String args[]) {
            JButton bt1 = new JButton("[ 1 ]");
            JButton bt2 = new JButton("[ 2 ]");
            JButton bt3 = new JButton("[ 3 ]");
            JButton bt4 = new JButton("[ 4 ]");
            JButton bt5 = new JButton("[ 5 ]");
            JButton bt6 = new JButton("[ 6 ]");
            JButton bt7 = new JButton("[ 7 ]");
            JButton bt8 = new JButton("[ 8 ]");
            JButton bt9 = new JButton("[ 9 ]");
            JButton bt = new JButton("[ < ]");
            JButton bt0 = new JButton("[ 0 ]");

            JPanel bt1Panel = new JPanel();
            JPanel bt2Panel = new JPanel();
            JPanel bt3Panel = new JPanel();
            JPanel bt4Panel = new JPanel();
            JPanel bt5Panel = new JPanel();
            JPanel bt6Panel = new JPanel();
            JPanel bt7Panel = new JPanel();
            JPanel bt8Panel = new JPanel();
            JPanel bt9Panel = new JPanel();
            JPanel btPanel = new JPanel();
            JPanel bt0Panel = new JPanel();

            bt1Panel.add(bt1);
            bt2Panel.add(bt2);
            bt3Panel.add(bt3);
            bt4Panel.add(bt4);
            bt5Panel.add(bt5);
            bt6Panel.add(bt6);
            bt7Panel.add(bt7);
            bt8Panel.add(bt8);
            bt9Panel.add(bt9);
            btPanel.add(bt);
            bt0Panel.add(bt0);

            JPanel panelGrid = new JPanel(new GridLayout(0,3));        

            panelGrid.add(bt1Panel);
            panelGrid.add(bt2Panel);
            panelGrid.add(bt3Panel);
            panelGrid.add(bt4Panel);
            panelGrid.add(bt5Panel);
            panelGrid.add(bt6Panel);
            panelGrid.add(bt7Panel);
            panelGrid.add(bt8Panel);
            panelGrid.add(bt9Panel);
            panelGrid.add(btPanel);
            panelGrid.add(bt0Panel);

            JPanel panelBrdLayout = new JPanel(new BorderLayout());
            panelBrdLayout.add(panelGrid, BorderLayout.SOUTH);
            JLabel label = new JLabel("[ DISPLAY PIN AS TYPED ]");
            panelBrdLayout.add(label, BorderLayout.NORTH);

            JFrame f = new JFrame();
            f.add(panelBrdLayout);
            f.pack();
            f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
            f.setVisible(true);

            bt1.addActionListener((e) -> updateLabel(label, "1"));
            bt2.addActionListener((e) -> updateLabel(label, "2"));
            bt3.addActionListener((e) -> updateLabel(label, "3"));
            bt4.addActionListener((e) -> updateLabel(label, "4"));
            bt5.addActionListener((e) -> updateLabel(label, "5"));
            bt6.addActionListener((e) -> updateLabel(label, "6"));
            bt7.addActionListener((e) -> updateLabel(label, "7"));
            bt8.addActionListener((e) -> updateLabel(label, "8"));
            bt9.addActionListener((e) -> updateLabel(label, "9"));
            bt0.addActionListener((e) -> updateLabel(label, "0"));

            bt.addActionListener((e) -> {
                if (label.getText().equals("[ DISPLAY PIN AS TYPED ]")) {
                    label.setText("[ DISPLAY PIN AS TYPED ]");
                }else {
                    String text = label.getText();
                    if (text.length() > 0) {
                        label.setText(text.substring(0, text.length() - 1));
                    }
                }
                checkPIN(label);
            });
        }

        private static void updateLabel(JLabel label, String text) {
            if (label.getText().equals("[ DISPLAY PIN AS TYPED ]")) {
                label.setText(text);
            } else {
                label.setText(label.getText() + text);
            }
            checkPIN(label);
        }
    
        private static void checkPIN(JLabel label) {
            if (label.getText().equals("202113")) {
                label.setText("YOU MAY ENTER");
            }
        }    
    }
   ```

