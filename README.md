 # 鲁昊 计181 2018310724
# 一、实验目的
再次了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法； 掌握面向对象的类设计方法（属性、方法）； 掌握类的继承用法，通过构造方法实例化对象； 掌握使用Object根类的toString（）方法，在自定义的类中覆盖Object的toString方法，使其可以输出类的信息（比如：学生基础信息及其所选课程的信息）
# 二、任务
1、编写上述实体类以及测试主类（注意类之间继承关系的适用）
2、在测试主类中，实例化多个类实体
3、针对操作过程中可能会出现的各种异常，做异常处理
# 三、实验核心方法
模拟学生选课操作、打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课教师 等）；模拟学生退课操作，再打印课程信息。

#   核心代码演示
void modclass(int i) {

		System.out.println("选择想要的课程：");
		System.out.println("1.体育");
		System.out.println("2.物理");
		System.out.println("3.化学");
		Scanner num2 = new Scanner(System.in);
		int a = num2.nextInt();
		switch(a) { 
		case 1: 
			class1[i] = 1;
			tea1[i] = 1;
			break;
		case 2:
			class1[i] = 2;
			tea1[i] = 2;
			break;
		case 3:
			class1[i] = 3;
			tea1[i] = 3;
			break;
			default :
				modclass(i);
			
		}
		
	
		
		
	}
# 实验结果
![avatar]（https://github.com/lu-hao123/XSXK/blob/master/987262219.jpg）
![avatar]（https://github.com/lu-hao123/XSXK/blob/master/1140646437.jpg）
# 五、实验心得
虽然这是我第二次再做这个实验，但是这个实验很锻炼我的综合考虑能力，通过第二次再做这个实验，我学到了许多，让我对于程序有了更深一步的理解。
