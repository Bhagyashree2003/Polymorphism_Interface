# Polymorphism_Interface
java code of Polymorphism with Interface.

interface camera

{

	 void takephoto();
   
	 void recording();
   
}
interface wifi

{

	String[] getnetworks();
  
	void connectToNetwork(String networks);
  
}

class cellphone

{

	void callnumber(int phonenumber)
  
	{
  
		System.out.println("calling :"+phonenumber);
    
	}
  
	void pickthecall()
  
	{
  
		System.out.println("Connecting....");
    
	}
  
}


class Mysmartphone extends cellphone implements camera, wifi

{

	public void takephoto()
  
	{
  
		System.out.println("taking snap");
    
	}
  
	public void recording()
  
	{
  
		System.out.println("start recording");		
    
	}
  

	public String[] getnetworks()
  
	{
  
		System.out.println("List Of Networks");	
    
		String[] networklist = {"Bhagyashree","Azad","Jainul", "Kinal","Kirtan","Kinal"};
    
		return networklist;	
    
	}
	
	public void connectToNetwork(String network)
  
	{
  
		System.out.println("connecting to " + network);
    
	}
  
}


class PolymorphismInterface

{

	public static void main(String args[])
  
	{
  
		camera cam=new Mysmartphone();
    
		Mysmartphone msp=new Mysmartphone();
    
		msp.takephoto();
    
		msp.recording();
    
		msp.getnetworks();
    
	}
  
}
