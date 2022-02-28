# Java.Bank
import java.util.Random;   
import java.util.*;
interface Operation
{
	abstract void Withdraw(double amount,int lan);
	abstract void Deposit(double amount,int lan);
}
class SBI implements Operation
{
	Random r=new Random();
	int l=r.nextInt(999999999);
	double balance=500;
	public void Withdraw(double amount,int lan)
	{
		System.out.println();
		System.out.println("***********************************");
		if(amount>balance)
		{
			if(lan==1)
			{
			System.out.println();
			System.out.println("!!!!!!!!!!!!WARNING!!!!!!!!!!!!!!");
			System.out.println();
			System.out.println();
			System.out.println("***********************************");
			System.out.println("Your Balance Is ₹ "+balance+" To Not Withdraw  ₹ "+amount);
			}
			else
			{
				
				System.out.println("????????? चेतावनी???????");
				System.out.println();
				System.out.println();
				System.out.println("******************************");
				System.out.println("आपका खाता बैलेंस  ₹  "+balance+" ओर आपकी उपाड रकम  ₹ "+amount+" ईस लीऐ ऐ व्यव्हार नहि हो सकेगा");
			}
		} 
		else
		{
			balance=balance-amount;
			if(lan==1)
			{
			System.out.println("Your Transaction Is Succesfully Complated");
			System.out.println("₹ "+amount+" Withdraw Is Complated");
			System.out.println("Current Balance Is = ₹ "+balance);
			}
			else
			{
				System.out.println("आपका व्यव्हार सफलता पूर्वक हो चुका हे");
				System.out.println("₹ "+amount+" आपके खाते से उपाड कीया गया है");
					System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
			}
		}
		System.out.println("***********************************");
	}
	public void Deposit(double amount,int lan)
	{
		System.out.println();
		System.out.println("***********************************");
		balance+=amount;
		if(lan==1)
		{
		System.out.println("Your Transaction Is Succefully Compalated");
		System.out.println("₹ "+amount+" Deposit Is In Your Account");
		System.out.println("Current  Balance : ₹ "+balance);
		}
		else
		{
			System.out.println("आपका व्यव्हार सफलता पूर्वक हो चुका हे");
			System.out.println("₹ "+amount+" आपके खाते मे जमा कर दीये है");
			System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
		}
		System.out.println("***********************************");
	}
	void Display(int lan)
	{
		System.out.println();
		System.out.println("*************************");
		if(lan==1)
		{
			System.out.println("Account No = "+l);
		System.out.println("CURRENT BALANCE IS = ₹ "+balance);
		}
		else
		{
			System.out.println("खाता संख्या =  "+l);
			System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
		}
		System.out.println("*************************");
	}
}
class HDFC implements Operation
{
	Random r=new Random();
	int l=r.nextInt(999999999);
	double balance=500;
	public void Withdraw(double amount,int lan)
	{
		System.out.println();
		System.out.println("***********************************");
		if(amount>balance)
		{
			System.out.println();
			if(lan==1)
			{
			System.out.println("!!!!!!!!!!!!WARNING!!!!!!!!!!!!!!");
			System.out.println();
			System.out.println();
			System.out.println("***********************************");
			System.out.println("Your Balance Is ₹ "+balance+" To Not Withdraw ₹ "+amount);
			}
			else
			{
				System.out.println("????????? चेतावनी???????");
				System.out.println();
				System.out.println();
				System.out.println("******************************");
				System.out.println("आपका खाता बैलेंस  ₹  "+balance+" ओर आपकी उपाड रकम  ₹ "+amount+" ईस लीऐ ऐ व्यव्हार नहि हो सकेगा");
	              	}
		}
		else
		{
			balance=balance-amount;
			if(lan==1)
			{
			System.out.println("Your Transaction Is Succesfully Complated");
			System.out.println("₹ "+amount+"Withdraw Is Complated");
			System.out.println("Current Balance Is = ₹ "+balance);
			}
			else
			{
				
				System.out.println("आपका व्यव्हार सफलता पूर्वक हो चुका हे");
				System.out.println("₹ "+amount+" आपके खाते से उपाड कीया गया है");
					System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
			}
		}
		System.out.println("***********************************");
	}
	public void Deposit(double amount,int lan)
	{
		System.out.println();
		System.out.println("***********************************");
		balance+=amount;
		if(lan==1)
		{
		System.out.println("Your Transaction Is Succefully Compalated");
		System.out.println("₹ "+amount+"Deposit Is Complated");
		System.out.println("Current  Balance : ₹ "+balance);
		System.out.println("***********************************");
		}
		else
		{
			System.out.println("आपका व्यव्हार सफलता पूर्वक हो चुका हे");
			System.out.println("₹ "+amount+" आपके खाते मे जमा कर दीये है");
			System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
		}
	}
	void Display(int lan)
	{
		System.out.println();
		System.out.println("*************************");
		if(lan==1)
		{
			System.out.println("Account No = "+l);
		System.out.println("CURRENT BALANCE IS = ₹ "+balance);
		}
		else
		{
			System.out.println("खाता संख्या =  "+l);
			System.out.println("आपके खाते का उपलब्ध बैलेंस ₹ "+balance);
		}
		System.out.println("*************************");
	}
}
public class BANK{
	public static int lan;
	public static  double withdraw()
	{
		System.out.println();
		Scanner s=new Scanner(System.in);
		double amount;
		System.out.println();
		if(lan==1)
		{
		System.out.println("*************************");
		System.out.println("Enter Withdraw Amount");
		System.out.println("*************************");
		}
		else
		{
			System.out.println("*************************");
			System.out.println("उपाड रकम डाखल करै");
			System.out.println("*************************");
		}
		amount=s.nextDouble();
		return amount;
	}
	public static double diposit()
	{
		Scanner s=new Scanner(System.in);
		double amount;
		System.out.println();
		if(lan==1)
		{
		System.out.println("*************************");
		System.out.println("Enter Deposit Amount");
		System.out.println("*************************");
		}
		else
                {
			System.out.println("*************************");
			System.out.println("जमा करने की रकम डाखल करै");
			System.out.println("*************************");
		}
		amount=s.nextDouble();
		return amount;
	}
	public static int submanu()
	{
		Scanner s=new Scanner(System.in);
		int a;
		System.out.println();
		if(lan==1)
		{
		System.out.println("**********OPERATION**********");
		System.out.println("1 : Withdraw");
		System.out.println("2 : Deposit");
		System.out.println("3 : Display");
		System.out.println("4 : BACK");
		System.out.println("*****************************");
		System.out.println();
		System.out.println("Enter Your Operation");
		}
		else
		{
			System.out.println("************* कार्य **********");
			System.out.println("१ : उपाड करे");
			System.out.println("२ : जमा करे ");
			System.out.println("३ : खाता का विवरन देखे");
			System.out.println("४ : बहार निकले");
			System.out.println("*****************************");
			System.out.println();
			System.out.println("अपना कायॅ पसद करे");
		}
		a=s.nextInt();
		return a;
	}
	public static void main(String[] args) {
		int sbi,hdfc,ch=1,co=1,user=0;
		Scanner s=new Scanner(System.in);
		System.out.println("*******************************************");
		System.out.println("Press 1 To English /हिंदी के लीये कोई भी नंबर दबाये");
		System.out.println("*******************************************");
		lan=s.nextInt();
		System.out.println();
		double amount;
		if(lan==1)
		{
		System.out.println("Enter  Number Of SBI User ");
		}
		else
		{
			System.out.println("ऐसबीई खाता धारक की संख्या डाले");
		}
		sbi=s.nextInt();
		System.out.println();
		if(lan==1)
		{
		System.out.println("Enter Number Of HDFC User");
		}
		else
		{
			System.out.println("ऐचडीऐफसी खाता धारक की संख्या डाले");
		}
		hdfc=s.nextInt();
		SBI []sb=new SBI[sbi+1];
		HDFC []hd=new HDFC[hdfc+1];
		for(int i=1;i<=sbi;i++)
		{
			sb[i]=new SBI();
		}
			for(int i=1;i<=hdfc;i++)
		{
			hd[i]=new HDFC();
		}
		while(ch!=0)
		{
		    if(lan==1)
		    {
		    System.out.println();
			System.out.println("***********MANU**********");
			System.out.println("1 : SBI");
			System.out.println("2 : HDFC");
			System.out.println("**************************");
			System.out.println();
			System.out.println("Enter Your Option And 0 To Exit");            }
			else
			{
				System.out.println();
				System.out.println("*****बैंक का चयन करे*****");
				System.out.println("१ : ऐसबीआई");
				System.out.println("२ : ऐचडीऐफसी");
				System.out.println("**************************");
				System.out.println();
				System.out.println("अपना विकल्प पसंद करे ओर बहार नीकल ने के लीयै 0 दबाये");
				
			}
			ch=s.nextInt();
			if(ch!=0)
			{
			System.out.println();
			if(lan==1)
			{
			System.out.println("Enter User Number");
			}
			else
			{
				System.out.println("खाता धारक की संख्या डाले");
			}
			user=s.nextInt();
			}
			if(ch!=0)
			{
				co=1;
			while(co!=0)
			{
			if(ch==1)
			{  
			    if(user>sbi)
			    {
			    	System.out.println();
			    	if(lan==0)
			    	{
			    	System.out.println("User Is Not Present On This Number");
			    	}
			    	else
			    	{
			    		System.out.println("ईस संख्या का कोई खाता धारक उपलब्ध नहि है ");
			    	}
			    	co=0;
                                }
			    else
			    {
				co=submanu();
				if(co==1)
				{
					amount=withdraw();
					sb[user].Withdraw(amount,lan);
				}
				else if(co==2)
				{
					amount=diposit();
					sb[user].Deposit(amount,lan);
				}
				else if(co==3)
				{
					sb[user].Display(lan);
				}
				else if(co==4)
				{
					co=0;
				}
				else 
				{
					System.out.println();
					if(lan==1)
					{
					System.out.println("Enter Right Operation");
					}
					else
					{
						System.out.println("कृपया सही कायॅ पंसद करे");
					}
				}
			    }
			}
			if(ch==2)
			{
			    if(user>hdfc)
			    {
			    	System.out.println();
			    	if(lan==1)
			    	{
			    	System.out.println("User Is Not Present On This Number");
			    	}
			    	else
			    	{
			      	System.out.println("ईस संख्या का कोई खाता धारक उपलब्ध नहि है ");
			    	}
			    	co=0;
			    }
			    else
			    {
				co=submanu();
				if(co==1)
				{
					amount=withdraw();
					hd[user].Withdraw(amount,lan);
				}
				else if(co==2)
				{
					amount=diposit();
					hd[user].Deposit(amount,lan);
				}
				else if(co==3)
				{
					hd[user].Display(lan);
				}
				else if(co==4)
				{
					co=0;
				}
				else 
				{
					System.out.println();
					if(lan==1)
					{
					System.out.println(" Enter Right Operation");
					}
					else
					{
					  	System.out.println("कृपया सही कायॅ पंसद करे");
					}
				}
			    }
			}
			if(ch!=0&&ch==1&&ch==2)
			{
				System.out.println();
				if(lan==1)
				{
				System.out.println("Enter Right Option");
				}
				else
				{
					System.out.println("कृपया सही विकल्प पंसद करे");
				}
			}
			}
			}
			else 
			{
				System.out.println();
				if(lan==1)
				{
				System.out.println("THANK YOU USING THIS BANKING SYSTEM !!!");
				}
				else
				{
					System.out.println("ईस बैंकिंग प्रणाली का प्रयोग करने के लिये धन्यवाद !!!!");
				}
			}
			
		}
	}
}

