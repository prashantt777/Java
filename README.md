# Platform used
Eclipse IDE8.


# Introduction
A simple console based social network java programe.
The first menu prompt users to login or quit.
The program will then ask you to create a username.
In this programe, users can create new post, they can add post for an event, job or sales.
Every post has a unique post ID that can be used to search and reply for a perticular post.
Users also has an option to view all the post in the programe, delete post or close post.

# Classes
These are the different classes made for implication of this project.

### Event
public class Event extends Post {
	private static long uniqueID = 0;//creating unique ids
	private String Venue;
	private String Date;
	private int Capacity;
	private int Attendee;
	public Event() {
		super();//calling parent class constructor
		setAttendee(0);
		
	
### Job
public class Job extends Post {

	private static long uniqueID = 0;//create unique if
	private double PropPrice;//proposed price
	private double LowestOffer;//
	
### Post
public abstract class Post {

	protected String ID;
	protected String Title;
	protected String Des;
	protected String Cid;//Id of Post creator
	protected Boolean Status;//Showing post open or close
	protected ArrayList<Reply> vec ;//Array list for storing replies
	public abstract boolean handleReply(Reply reply);//Abstract function used in child
	public abstract String getReplyDetails();

### Reply
public class Reply {

	private String Id;//id of post
	private double Value;//value to be put on post
	private String ResponderId;//id of person going to reply
	//parametrized constructor
	public Reply(String I, double val, String RI)
  
### Sale
public class Sale extends Post {

	private static long uniqueID = 0;//this will create unique ids
	private double AskingPrice;
	private double HighestOffer;
	private double MinRaise;
  
### Startup
public class Startup {

	public Startup() {
		// TODO Auto-generated constructor stub
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Unilink ob= new Unilink();
		 try {
			ob.main1();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

	}
  }
### Unilink
	public Unilink() {
		// TODO Auto-generated constructor stub
	}
	//Hard code for few enetries of post
	public void HardCode(ArrayList<Post> Poly)
	{
		Poly.add(new Event("Event1","Birthday","S1","Cafe","29/01/2020",5));
		Poly.add(new Event("Event2","Conference","S2","BoardRoom","30/02/2020",50));
		Poly.add(new Sale("Bike","used","S4",4560,100));
		Reply R =new Reply("EVE001",1, "S3");
		Poly.get(0).handleReply(R);
		R =new Reply("EVE001",1, "S6");
		Poly.get(0).handleReply(R);
		R =new Reply("SAL001",4789, "S99");
		Poly.get(2).handleReply(R);
		
	}
	//Menu to pop up again and again
	public  void Menu() {
		System.out.print("\n1. New Event Post\n2. New Sale Post\n3. New Job Post\n");
		System.out.print("4. Reply To Post\n5. Display My Posts\n6. Display All Posts");
		System.out.print("\n7. Close Post\n8. Delete Post\n9. Log Out\nEnter your choice:");

# Conclusion
This project uses the concept of all object oriented programming like polymorphism,inheritance,encapsulation and abstraction.It generates automated event ID for every post and users can use this Ids to track post and update purposes.

