OOPS concept

Program:

import java.util.Scanner;
public class oops {
    public static void main(String arg[]){


    //CUSTOMER SIDE
         costs_item cust1=new costs_item();
    order cust01=new order();
    cust1.topic();
    cust1.cost();
    Scanner sc=new Scanner(System.in);
    System.out.println("what would you like to have sir:");
    String order=sc.nextLine();
     System.out.println("how many sir");
     int quantity=sc.nextInt();
     cust01.orders(order,quantity);
     cust01.bills();
     cust01.setName(cust01.totals);
     payment pay01=new payment();
     System.out.println("sir your using (for gpay type 1 /for cash type 2)?");
     int pay_via=sc.nextInt();
     if (pay_via ==1){
      String a ="scanner";
      pay01.pay(a);
     }
     else{
       
      int a=0;
      pay01.pay(a);
     }


     //MANAGEMENT SIDE
    verification_bar ver=new verification_bar();
    sc.nextLine();
    for(;;){
     System.out.println("do you want to check the management side (staff only allowed)");
     
     String option=sc.nextLine();
     
     if (option.equals("yes")){
      System.out.println(option);
      ver.check();
      ver.management(order,quantity,cust01);
     }
     else{
        System.out.println("thank you!");
        break;
     }
    }
 
     
}
}
abstract class item_cost{
    public abstract void cost();
   void topic(){
    System.out.println("MENU (tdyavailable items)");
   }
}
class costs_item extends item_cost{
    int tea=15;
     int ginger_tea=20;
     int coffee=25;
     int milk=10;
     int black_coffee=15;
     int black_tea=15;
     int boost=30;
    int sandwitch=50;
    int bread_omelete=50;
    int french_fries=40;
    int burger=60;
    public void cost(){
    System.out.println(" ");
    System.out.println("tea = rs."+tea);
    System.out.println("ginger_tea= rs.20");
    System.out.println("coffee= rs.25");
    System.out.println("milk= rs.10");
    System.out.println("black_coffee= rs.15");
    System.out.println("black_tea= rs.15");
    System.out.println("boost= rs.30");
    System.out.println("SNACKS");
    System.out.println("sandwitch=rs.50");
    System.out.println("bread_omelete=rs.50");
    System.out.println("french_fries=rs.40");
    System.out.println("burger=rs.60");
    }
}
class order extends costs_item{
    special_orders spl=new special_orders();
     payment pay01=new payment();
    Scanner sc=new Scanner(System.in);
    int totals;
    private int cashbox;
    void orders(String order,int quantity){
       
         int item=0;
        if(order.equals("tea")){
        item=tea;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("ginger tea")){
        item=ginger_tea;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("coffee")){
       item=coffee;
       System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("milk")){
        item=milk;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("black coffee")){
        item=black_coffee;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("black tea")){
        item=black_tea;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("boost")){
         item=boost;
         System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("sandwitch")){
         item=sandwitch;
         System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("bread omelete")){
        item=bread_omelete;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("french fries")){
        item=french_fries;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
        else if(order.equals("burger")){
        item=burger;
        System.out.println("do you want anything special in that sir?");
        String opinion =sc.nextLine();
        if(opinion.equals("yes")){
       
          spl.prepare();
        }
        else{
       
          pay01.prepare();
        }
        }
       
        int total=item*quantity;
        this.totals=total;
        this.cashbox+=total;
   


    }


    public int getName(){
        return cashbox;
    }
    public void setName(int totals){
    this.cashbox=totals;
    }
    class special_orders{
        void prepare(){
            System.out.println("added special items");
        }
    }
   


   
    void bills(){
       
        System.out.println("rs."+totals+" your bill sir");
        System.out.println(cashbox);
       
    }
}
class payment{
     public void prepare(){
        System.out.println("your order sir");
    }
    void pay(String via){
     System.out.println("use this "+via+" sir ");
     System.out.println("thank you for coming sir");
    }
    void pay(int via ){
     System.out.println("thank you for coming sir");
    }
}






//management side






 class management_side extends oops{
     
     void check(){
        System.out.println("what you want to verify");
     }
    }
class verification_bar extends management_side {
    Scanner sc=new Scanner(System.in);
   public void management(String order,int quantity,order cust01){
     System.out.println("press (1) to enquire about staff ");
     System.out.println("press (2) to enquire about  raw products remaining ");
     System.out.println("press (3) to enquire about income and cost spent ");
     int enquire=sc.nextInt();
     if(enquire==1){
     staff st=new staff();
     st.staffs();
     }
     else if(enquire==2){
    products pro =new products();
    pro.remaining(order, quantity);
    pro.remaining();
     }
     else if(enquire==3){
    // products pro =new products();
    kanaku cal=new kanaku();
    cal.calc(cust01);
   
     }
    }


}
class staff {
  int tea_master=1;
        int tea_master_salary=12000;
        int coffee_master=1;
        int coffee_master_salary=12000;
        int chef=1;
        int chef_salary=10000;
        int clerk=1;
        int clerk_salary=5000;
    void staffs(){
       
        System.out.println("tea Master - "+tea_master+"salary - "+tea_master_salary);
        System.out.println("coffee Master - "+coffee_master+"salary - "+coffee_master_salary);
        System.out.println("chef - "+chef+"salary - "+chef_salary);
        System.out.println("clerk - "+clerk+"salary - "+clerk_salary);
     
    }
}
class products extends order {
      double boost_powder=30;//gm
      double sugar =5;//kg
      double ginger=10;//gram
      double milk =12;//litre
      double tea_powder=30;//gram
      double coffee_powder=30;//gram
      double bread_slice =40;//slice
      double egg=20;
      double potato=3;//kg
      double bun=20;//pcs
      double chesse=10;//pcs
      double veggies=2;//kg


      void remaining(String order,int quantity){
        if(order.equals("tea")){
          milk=milk-(0.1*quantity);
          sugar=sugar-(0.01*quantity);
          tea_powder=tea_powder-(1.5*quantity);
        }
        else if(order.equals("coffee")){
          milk=milk-(0.1*quantity);
          sugar=sugar-(0.01*quantity);
          coffee_powder=coffee_powder-(1.5*quantity);
        }
        else if(order.equals("giner_tea")){
          milk=milk-(0.1*quantity);
          sugar=sugar-(0.01*quantity);
          tea_powder=tea_powder-(1.5*quantity);
          ginger=ginger-(0.5*quantity);
        }
        else if(order.equals("milk")){
          milk=milk-(0.1*quantity);
          sugar=sugar-(0.01*quantity);
        }
        else if(order.equals("black_coffee")){
          coffee_powder=coffee_powder-(1.5*quantity);
          sugar=sugar-(0.01*quantity);
        }
         else if(order.equals("black_tea")){
          tea_powder=tea_powder-(1.5*quantity);
          sugar=sugar-(0.01*quantity);
        }
        else if(order.equals("boost")){
          boost_powder=boost_powder-(1.5*quantity);
          sugar=sugar-(0.01*quantity);
          milk=milk-(0.1*quantity);
        }
         else if(order.equals("bread_omelete")){
         bread_slice=bread_slice-(2*quantity);
         egg=egg-(2*quantity);
        }
         else if(order.equals("sandwitch")){
         bread_slice=bread_slice-(2*quantity);
         veggies=veggies-(0.02*quantity);
        }
         else if(order.equals("french_fries")){
         potato=potato-(0.25*quantity);
        }
        else if(order.equals("burger")){
         bun=bun-(2*quantity);
         veggies=veggies-(0.02*quantity);
        chesse=chesse-(1*quantity);
       
        }
     }
     void remaining(){
      System.out.println("remaining products and its quantities");
      System.out.println("remaining boost_powder ="+ boost_powder+"gm");
      System.out.println("remaining sugar = "+ sugar+"gm" );      
      System.out.println("remainingginger = "+ ginger+"gm");
      System.out.println("remaining milk = "+ milk+"l" );
      System.out.println("remaining tea powder = "+ tea_powder+"gm");
      System.out.println("remaining coffee powder = "+ coffee_powder+"gm");
      System.out.println("remaining bread slice = "+ bread_slice +"pcs");
      System.out.println("remaining egg = "+ egg+"pcs");  
      System.out.println("remaining potato = "+ potato+"gm");      
      System.out.println("remaining bun = "+ bun+"pcs");
      System.out.println("remaining chesse = "+ chesse +"pcs");
      System.out.println("remaining veggies = "+ veggies+"gm");
     }
     }
     class kanaku extends order {
      staff st =new staff();
     
      void calc(order obj){
       
      double income=(obj.totals*50)*30;
      double profit=income-(st.chef_salary+st.coffee_master_salary+st.tea_master_salary+st.clerk_salary);
       
        System.out.println("total income of an month "+income);
        System.out.println("today's total income "+obj.totals*50);
        System.out.println("the salary of chef is "+st.chef_salary+" the salary of coffee master is "+st.coffee_master_salary+" the salary of tea master is "+st.tea_master_salary+" the salary of clerkis "+st.clerk_salary);
        System.out.println("final profit of the month is " +profit);
       
      }


     }
 


   
   






