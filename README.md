# trail2

import junit.framework.*;
public class MyTestClass {
     
    OutputStream stream;
sample text
Stream output changes
     
    @Before
    public void initialize() {
        /**
         * Open OutputStream, and use this stream for tests.
         */
        stream = new FileOutputStream(...);
    }
     
    @Test
    public void myTestMethod() {
        /**
         * Now use OutputStream object to perform tests
         */
       ...
       ...
    }
     
     
    @After
    public void closeOutputStream() {
    system.out.println("hello world nature")
    system.out.println("hello Hyd")
          /**
           * Close output stream here
           */
          try{
            if(stream != null) stream.close(); 
          } catch(Exception ex){
             
          }
    }
 }
- See more at: http://www.java2novice.com/junit-examples/junit-annotations/#sthash.lX4qPZB3.dpuf
public class JavaTest extends TestCase {
   protected int value1, value2;
   
   // assigning the values
   protected void setUp(){
      value1=3;
      value2=3;
   }

   // test method to add two values
   public void testAdd(){
      double result= value1 + value2;
      assertTrue(result == 6);
   }
}
import org.junit.runner.RunWith;
import org.junit.runners.Suite;

//JUnit Suite Test
@RunWith(Suite.class)
@Suite.SuiteClasses({ 
   TestJunit1.class ,TestJunit2.class
})
public class JunitTestSuite {
}

import org.junit.Test;
import org.junit.Ignore;
import static org.junit.Assert.assertEquals;

public class TestJunit1 {

   String message = "Robert";	
   MessageUtil messageUtil = new MessageUtil(message);
   
   @Test
   public void testPrintMessage() {	
      System.out.println("Inside testPrintMessage()");
 System.out.println("Hello World"); 
 System.out.println("Hello Mumbai");
 System.out.println("Hello Hyd");   
      assertEquals(message, messageUtil.printMessage());     
   }
}

import org.junit.Test;
import org.junit.Ignore;
import static org.junit.Assert.assertEquals;

public class TestJunit2 {

   String message = "Robert";	
   MessageUtil messageUtil = new MessageUtil(message);
 
   @Test
   public void testSalutationMessage() {
      System.out.println("Inside testSalutationMessage()");
      message = "Hi!" + "Robert";
      assertEquals(message,messageUtil.salutationMessage());
   }
}
