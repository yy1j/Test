# Test
do it better!
package 记事本;

import java.awt.Button;
import java.awt.FileDialog;
import java.awt.FlowLayout;
import java.awt.TextArea;
import java.awt.event.ActionListener;
import java.io.BufferedReader;
import java.io.BufferedWriter;

import javax.swing.JFrame;
import javax.swing.JMenu;
import javax.swing.JMenuBar;
import javax.swing.JMenuItem;

public class RecordText extends JFrame implements ActionListener {
private JMenuBar menuBar; //打开菜单
private TextArea text; //文本内容
private BufferedWriter out;  //字符缓冲流输出
private BufferedReader in; //字符缓冲流输入
private FileDialog f_Save;
public RecordText() {

	this.setTitle("学生信息统计程序");
	this.setSize(800,600);
	this.setLayout(new FlowLayout());
	
}
public void jfame() {
	menuBar=new JMenuBar();
	this.setJMenuBar(menuBar);
	JMenu menu1=new JMenu("文件");
	menuBar.add(menu1);
	JMenuItem menuItem1=new JMenuItem("打开");
	JMenuItem menuItem2=new JMenuItem("保存");
	menu1.add(menuItem1);
	menuItem1.addActionListener(this);
	menu1.add(menuItem2);
	menuItem1.addActionListener(this);
	text=new TextArea(100,100);
	f_Save=new FileDialog(this,"保存文件对话框",FileDialog.SAVE);
	f_Save
	this.add(text);
	 this.setVisible(true);
}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		RecordText A=new RecordText();
		A.jfame();
	}

}
