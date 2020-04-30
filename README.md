 # 鲁昊 计181 2018310724
# 一、实验目的
分析学生选课系统
使用GUI窗体及其组件设计窗体界面
完成学生选课过程业务逻辑编程
# 二、任务
1、设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
2、基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
3、针对操作过程中可能会出现的各种异常，做异常处理
# 三、实验核心方法
先确定需要哪些包（swing\awt\IO），将包导入，导入后先构建整体的GUI的所有界面。将界面通过监听事件相连接。然后在需要文本写入与文本读出的地方的界面写上文本操作。而打印课表则是通过将文件打开，显示出学生基本信息、所选课程来实现的。
#   代码演示
package 学生选课;
/*
 * 该部分主要用于让学生选择是选课还是输出信息
 */
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.*;
public class caozuo extends JFrame implements ActionListener{
	JButton Choosing = new JButton("选      课");
	JButton Printing = new JButton("输出信息");
	JLabel wel = new JLabel("欢迎！请进行以下操作");
	
	caozuo(){
		setTitle("学生");
		setSize(250,250);
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		setVisible(true);
		setLayout(new BorderLayout());
		add("North",wel);
		add("West",Choosing);add("East",Printing);
		validate();
		Choosing.addActionListener(this);;
		Printing.addActionListener(this);
	}
	public void actionPerformed(ActionEvent e) {
		if(e.getSource()==Choosing) {
			new Choosing();
		}
		if(e.getSource()==Printing) {
			try {
				Runtime.getRuntime().exec("C:\\Users\\Thinkpad\\Desktop\\学生选课.txt");
				} catch (Exception e1) {
					System.out.println("txt打开失败！");
					e1.printStackTrace();
				}
				} 
	   
	}
	public static void main(String[] args) {
		caozuo c = new caozuo();
	}
}
# 实验结果
a

# 五、实验心得
虽然这是我第二次再做这个实验，但是这个实验很锻炼我的综合考虑能力，像文件输入时如何保证是在末尾添加而不是刷新界面、如何将输在文本框的内容添加到txt文件中等，这些十分考验我在文件处理时所需要的编程能力。通过第二次再做这个实验，我学到了许多，让我对于程序有了更深一步的理解。
