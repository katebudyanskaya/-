import java.util.Scanner;

public class Button {

	Button[] b = { new Button('2', "a,b,c"), new Button('3', "d,e,f"),
		       new Button('4', "g,h,i"), new Button('5', "j,k,l"),
		       new Button('6', "m,n,o"), new Button('7', "p,q,r,s"),
		       new Button('8', "t,u,v"), new Button('9', "w,x,y,z"),
		       new Button('0', " ") };

char digit;
String letters;
int counter=0;
public int press(){
	return counter+1;
}
public String getResult(){
	return char c=b[counter-1];
}
public void reset(){
	counter=0;
}

}
public class Phone {
Button[] b;
	public void press(char c) {
		switch (c) {
		case '2': {
			b[0].press();
			break;}
		case '3': {
			b[1].press();
			break;}
		case '4': {
			b[2].press();
			break;}
		case '5': {
			b[3].press();
			break;}
		case '6': {
			b[4].press();
			break;}
		case '7': {
			b[5].press();
			break;}
		case '8': {
			b[6].press();
			break;}
		case '9': {
			b[7].press();
			break;}
		case '0': {
			b[8].press();
			break;}
		}

	}

	public void press (String s){
			for (int i = 0; i < s.length(); i++) {
				s[i].press();
				if s[i+1].equals(s[i]){
					continue;
				}else 
					{b.getResult()
					b.reset();}
				
			}
		}

	public String getResult(char c) {
		String s;
		s+=c;
		return s;
	}

	public void reset() {

	}

	public static void main(String[] args) {
		Scanner i = new Scanner(System.in);
		Phone p = new Phone();
		p.press("4433555666");
		System.out.print(p.getResult());
	}

}
