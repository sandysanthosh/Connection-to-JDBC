Welcome to the Connection-to-JDBC wiki!

http://www.javaguides.net/p/jdbc-tutorial.html?m=1`

`public class insertsql {
	static String username="";
	static String password="";
	static String url="";
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		try{
			  
			  
			Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/Rajendra","root","sandy");
			  
			//PreparedStatement stmt=con.prepareStatement("select * from family"); 
			PreparedStatement stmt=con.prepareStatement("insert into family values(?,?)");
			stmt.setString(1,"asdasd");
			stmt.setString(2,"asdas32423");
			int rs=stmt.executeUpdate();  
			System.out.println(rs); 
			con.close();
			
		}`