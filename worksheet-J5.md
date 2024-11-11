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
   
   6. Lambda expressions only work if there is a single method to implement. So ```ActionListener``` can implement it because it is only using a single method.  

