<<<<<<< HEAD
package calculatour2;

import java.awt.Color;
import java.awt.Font;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.SwingConstants;

public class Calculator implements ActionListener {

	boolean operaterclicked;

	double num1;
	String result;

	double num2;
	int calculation;

	JFrame lx;

	JLabel displaylabel;

	JButton seven;

	JButton eight;

	JButton zero;

	JButton backspace;

	JButton nine;

	JButton six;

	JButton one;

	JButton two;

	JButton three;

	JButton four;

	JButton five;

	JButton minze;

	JButton plus;

	JButton division;

	JButton equal;

	JButton dot;

	JButton multiplication;

	JButton clear;

	JButton square;

	JButton squareRoot;

	Calculator() {
		lx = new JFrame("Calculator");
		lx.setLayout(null);
		lx.getContentPane().setBackground(Color.BLACK);
		lx.setSize(600, 600);
		lx.setVisible(true);
		lx.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

		displaylabel = new JLabel();
		displaylabel.setBounds(30, 50, 461, 45);
		displaylabel.setBackground(Color.orange);
		displaylabel.setOpaque(true);
		displaylabel.setHorizontalAlignment(SwingConstants.RIGHT);
		displaylabel.setForeground(Color.black);
		lx.add(displaylabel);

		Font displayFont = displaylabel.getFont();
		displaylabel.setFont(new Font(displayFont.getName(), Font.BOLD, 18));

		lx.add(displaylabel);

		Font buttonfont = new Font("Arial", Font.BOLD, 18);
		seven = new JButton("7");
		seven.setFont(buttonfont);
		seven.setForeground(Color.ORANGE);
		seven.setBounds(30, 130, 80, 80);
		seven.setBackground(Color.BLACK);
		seven.addActionListener(this);
		lx.add(seven);

		Font buttonfont8 = new Font("Arial", Font.BOLD, 18);
		eight = new JButton("8");
		eight.setFont(buttonfont8);
		eight.setForeground(Color.ORANGE);
		eight.setBounds(135, 130, 80, 80);
		eight.setBackground(Color.BLACK);
		eight.addActionListener(this);
		lx.add(eight);

		Font buttonfont9 = new Font("Arial", Font.BOLD, 18);

		nine = new JButton("9");
		nine.setFont(buttonfont9);
		nine.setForeground(Color.ORANGE);
		nine.setBounds(230, 130, 80, 80);
		nine.setBackground(Color.BLACK);
		nine.addActionListener(this);
		lx.add(nine);

		Font buttonfont4 = new Font("Arial", Font.BOLD, 18);

		four = new JButton("4");
		four.setFont(buttonfont4);
		four.setForeground(Color.ORANGE);
		four.setBounds(30, 220, 80, 80);
		four.setBackground(Color.BLACK);
		four.addActionListener(this);
		lx.add(four);

		Font buttonfont5 = new Font("Arial", Font.BOLD, 18);

		five = new JButton("5");
		five.setFont(buttonfont5);
		five.setForeground(Color.ORANGE);
		five.setBounds(135, 220, 80, 80);
		five.setBackground(Color.BLACK);
		five.addActionListener(this);
		lx.add(five);

		Font buttonfont6 = new Font("Arial", Font.BOLD, 18);

		six = new JButton("6");
		six.setFont(buttonfont6);
		six.setForeground(Color.ORANGE);
		six.setBounds(230, 220, 80, 80);
		six.setBackground(Color.BLACK);
		six.addActionListener(this);
		lx.add(six);

		Font buttonfont1 = new Font("Arial", Font.BOLD, 18);

		one = new JButton("1");
		one.setFont(buttonfont1);
		one.setForeground(Color.ORANGE);
		one.setBounds(30, 310, 80, 80);
		one.setBackground(Color.BLACK);
		one.addActionListener(this);
		lx.add(one);

		Font buttonfont2 = new Font("Arial", Font.BOLD, 18);

		two = new JButton("2");
		two.setFont(buttonfont2);
		two.setForeground(Color.ORANGE);
		two.setBounds(135, 310, 80, 80);
		two.setBackground(Color.BLACK);
		two.addActionListener(this);
		lx.add(two);

		Font buttonfont3 = new Font("Arial", Font.BOLD, 18);

		three = new JButton("3");
		three.setFont(buttonfont3);
		three.setForeground(Color.ORANGE);
		three.setBounds(230, 310, 80, 80);
		three.setBackground(Color.BLACK);
		three.addActionListener(this);
		lx.add(three);

		Font buttonfontd = new Font("Arial", Font.BOLD, 18);

		dot = new JButton(".");
		dot.setFont(buttonfontd);
		dot.setForeground(Color.black);
		dot.setBounds(30, 400, 80, 80);
		dot.setBackground(Color.orange);
		dot.addActionListener(this);
		lx.add(dot);

		backspace = new JButton("⌫");
		backspace.setForeground(Color.black);
		backspace.setBounds(410, 400, 80, 80);
		backspace.setBackground(Color.orange);
		backspace.addActionListener(this);
		lx.add(backspace);

		Font buttonfont0 = new Font("Arial", Font.BOLD, 18);

		zero = new JButton("0");
		zero.setFont(buttonfont0);
		zero.setForeground(Color.ORANGE);
		zero.setBounds(135, 400, 80, 80);
		zero.setBackground(Color.BLACK);
		zero.addActionListener(this);
		lx.add(zero);

		Font buttonfonte = new Font("Arial", Font.BOLD, 18);

		equal = new JButton("=");
		equal.setFont(buttonfonte);
		equal.setForeground(Color.black);
		equal.setBounds(230, 400, 80, 80);
		equal.setBackground(Color.orange);
		equal.addActionListener(this);
		lx.add(equal);

		Font buttonfontp = new Font("Arial", Font.BOLD, 18);

		plus = new JButton("+");
		plus.setFont(buttonfontp);
		plus.setForeground(Color.black);
		plus.setBounds(320, 130, 80, 80);
		plus.setBackground(Color.orange);
		plus.addActionListener(this);
		lx.add(plus);

		Font buttonfontm = new Font("Arial", Font.BOLD, 18);

		minze = new JButton("-");
		minze.setFont(buttonfontm);
		minze.setForeground(Color.black);
		minze.setBounds(320, 220, 80, 80);
		minze.setBackground(Color.orange);
		minze.addActionListener(this);
		lx.add(minze);

		Font buttonfontml = new Font("Arial", Font.BOLD, 18);

		multiplication = new JButton("×");
		multiplication.setFont(buttonfontml);
		multiplication.setForeground(Color.black);
		multiplication.setBounds(320, 310, 80, 80);
		multiplication.setBackground(Color.orange);
		multiplication.addActionListener(this);
		lx.add(multiplication);

		Font buttonfontdi = new Font("Arial", Font.BOLD, 18);

		division = new JButton("÷");
		division.setFont(buttonfontdi);
		division.setForeground(Color.black);
		division.setBounds(320, 400, 80, 80);
		division.setBackground(Color.orange);
		division.addActionListener(this);
		lx.add(division);

		Font buttonfontc = new Font("Arial", Font.BOLD, 18);

		clear = new JButton("clear");
		clear.setFont(buttonfontc);
		clear.setForeground(Color.black);
		clear.setBounds(410, 130, 80, 80);
		clear.setBackground(Color.orange);
		clear.addActionListener(this);
		lx.add(clear);

		Font buttonfonts = new Font("Arial", Font.BOLD, 18);

		square = new JButton("x²");
		square.setFont(buttonfonts);
		square.setForeground(Color.black);
		square.setBounds(410, 310, 80, 80);
		square.setBackground(Color.orange);
		square.addActionListener(this);
		lx.add(square);

		Font buttonfontsr = new Font("Arial", Font.BOLD, 18);

		squareRoot = new JButton("√");
		squareRoot.setFont(buttonfontsr);
		squareRoot.setForeground(Color.black);
		squareRoot.setBounds(410, 220, 80, 80);
		squareRoot.setBackground(Color.orange);
		squareRoot.addActionListener(this);
		lx.add(squareRoot);
	}

	public static void main(String[] args) {
		new Calculator();
	}

	@Override
	public void actionPerformed(ActionEvent e) {

		if (e.getSource() == seven) {
			if (operaterclicked) {
				displaylabel.setText("7");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "7");
			}
		} else if (e.getSource() == eight) {
			if (operaterclicked) {
				displaylabel.setText("8");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "8");
			}
		} else if (e.getSource() == nine) {
			if (operaterclicked) {
				displaylabel.setText("9");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "9");
			}
		} else if (e.getSource() == two) {
			if (operaterclicked) {
				displaylabel.setText("2");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "2");
			}
		} else if (e.getSource() == one) {
			if (operaterclicked) {
				displaylabel.setText("1");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "1");
			}
		} else if (e.getSource() == three) {
			if (operaterclicked) {
				displaylabel.setText("3");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "3");
			}
		} else if (e.getSource() == four) {
			if (operaterclicked) {
				displaylabel.setText("4");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "4");
			}
		} else if (e.getSource() == five) {
			if (operaterclicked) {
				displaylabel.setText("5");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "5");
			}
		} else if (e.getSource() == six) {
			if (operaterclicked) {
				displaylabel.setText("6");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "6");
			}
		} else if (e.getSource() == zero) {
			if (operaterclicked) {
				displaylabel.setText("0");
				operaterclicked = false;
			} else {
				displaylabel.setText(displaylabel.getText() + "0");
			}
		} else if (e.getSource() == multiplication) {
			operaterclicked = true;
			String str = displaylabel.getText();
			num1 = Double.parseDouble(displaylabel.getText());
			calculation = 3;
			displaylabel.setText(str + "×");
		} else if (e.getSource() == equal) {
			num2 = Double.parseDouble(displaylabel.getText());
			switch (calculation) {
			case 1:
				result = String.valueOf(num1 + num2);
				break;
			case 2:
				result = String.valueOf(num1 - num2);
				break;
			case 3:
				result = String.valueOf(num1 * num2);
				break;
			case 4:
				if (num2 != 0) {
					result = String.valueOf(num1 / num2);
				} else {
					result = "Error: Division by zero";
				}
				break;
			}
			displaylabel.setText(result);
		} else if (e.getSource() == dot) {
			displaylabel.setText(displaylabel.getText() + ".");
		} else if (e.getSource() == minze) {
			operaterclicked = true;
			String str = displaylabel.getText();
			num1 = Double.parseDouble(displaylabel.getText());
			calculation = 2;
			displaylabel.setText(str + "-");
		} else if (e.getSource() == plus) {
			operaterclicked = true;
			String str = displaylabel.getText();
			num1 = Double.parseDouble(displaylabel.getText());
			calculation = 1;
			displaylabel.setText(str + "+");
		} else if (e.getSource() == division) {
			operaterclicked = true;
			String str = displaylabel.getText();
			num1 = Double.parseDouble(displaylabel.getText());
			calculation = 4;
			displaylabel.setText(str + "÷");
		} else if (e.getSource() == clear) {
			displaylabel.setText("");
		} else if (e.getSource() == square) {
			double num = Double.parseDouble(displaylabel.getText());
			displaylabel.setText(String.valueOf(num * num));
		} else if (e.getSource() == squareRoot) {
			double num = Double.parseDouble(displaylabel.getText());
			if (num >= 0) {
				displaylabel.setText(String.valueOf(Math.sqrt(num)));
			} else {
				displaylabel.setText("Error: Invalid input");
			}

		} else if (e.getSource() == backspace) {

			String currentText = displaylabel.getText();
			if (!currentText.isEmpty()) {
				String newText = currentText.substring(0, currentText.length() - 1);
				displaylabel.setText(newText);
			}
		}

	}
}
=======
# Maths-Calculator-
A simple calculator app 
>>>>>>> 85868bcf63f4f5bc881d1afdfb833ae3ec3581f7
