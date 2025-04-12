import javax.swing.*;
import java.awt.*;

public class LabActivityGUI {
    public static void main(String[] args) {
        JFrame frame = new JFrame("JFrame Lab Activity");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(400, 350);
        frame.setLayout(new BorderLayout());

        // Title
        JLabel titleLabel = new JLabel("My Activity: (write your full name)", SwingConstants.CENTER);
        frame.add(titleLabel, BorderLayout.NORTH);

        // Panel for form
        JPanel panel = new JPanel(new GridLayout(5, 2, 10, 10));
        panel.setBorder(BorderFactory.createEmptyBorder(10, 10, 10, 10));

        JLabel courseLabel = new JLabel("COURSE:");
        JTextField courseField = new JTextField();

        JLabel yearLabel = new JLabel("YEAR LEVEL & SECTION:");
        JTextField yearField = new JTextField();

        JLabel addressLabel = new JLabel("ADDRESS:");
        JTextField addressField = new JTextField();

        JLabel reflectionLabel = new JLabel("SELF-REFLECTION:");
        JTextArea reflectionArea = new JTextArea(3, 20);
        JScrollPane scrollPane = new JScrollPane(reflectionArea);

        panel.add(courseLabel);
        panel.add(courseField);
        panel.add(yearLabel);
        panel.add(yearField);
        panel.add(addressLabel);
        panel.add(addressField);
        panel.add(reflectionLabel);
        panel.add(scrollPane);

        frame.add(panel, BorderLayout.CENTER);

        // Buttons
        JPanel buttonPanel = new JPanel();
        JButton saveButton = new JButton("save");
        JButton cancelButton = new JButton("cancel");

        buttonPanel.add(saveButton);
        buttonPanel.add(cancelButton);

        frame.add(buttonPanel, BorderLayout.SOUTH);

        frame.setVisible(true);
    }
}