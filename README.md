# project-chapter-6

import java.util.Random;
import java.util.List;
import java.util.Arrays;
import java.util.HashMap;
/**
 * The responder class represents a response generator object.
 * It is used to generate an automatic response to an input string.
 * 
 * @author     Michael Kölling and David J. Barnes
 * @version    0.1 (2016.02.29)
 */
public class Responder
{
    
    
    
    /**
     * Construct a Responder - nothing to do
     */
    public Responder()
    {
    }

    /**
     * Generate a response.
     * @return   A string that should be displayed as the response
     */
    public String generateResponse(String input)
    {
        HashMap<String, String> match = new HashMap<String, String>();
        
        match.put("slow","This is usually a hardware problem. Have you tried upgrading your processor?");
        match.put("microsoft","This is a problem that Microsoft needs to deal with.");
        match.put("fire","Try dabbing it with a dry towel.");
        match.put("broken","I dont think thats the problem. It should work regardless.");
        
        if(input.containsKey(){
        }
        
                
         }
         
    public String generateRandomResponse(){
        List<String> listofgeneric = Arrays.asList(
            "That's interesting tell me more...",
            "Have you tried restarting your computer?",
            "Are you sure you're computer is on?",
            "Seems strange. I've never heard of this kind of problem before"
            );
        
            Random random = new Random();
            return listofgeneric.get(random.nextInt(listofgeneric.size()));
             
    }
}



/**
 * This class implements a technical support system. It is the top level class 
 * in this project. The support system communicates via text input/output 
 * in the text terminal.
 * 
 * This class uses an object of class InputReader to read input from the user,
 * and an object of class Responder to generate responses. It contains a loop
 * that repeatedly reads input and generates output until the users wants to 
 * leave.
 * 
 * @author     Michael Kölling and David J. Barnes
 * @version    0.1 (2016.02.29)
 */
public class SupportSystem
{
    private InputReader reader;
    private Responder responder;
    
    /**
     * Creates a technical support system.
     */
    public SupportSystem()
    {
        reader = new InputReader();
        responder = new Responder();
    }

    /**
     * Start the technical support system. This will print a welcome
     * message and enter into a dialog with the user, until the user
     * ends the dialog.
     */
    public void start()
    {
        boolean finished = false;

        printWelcome();

        while(!finished) {
            String answer = reader.getInput();
            String input = answer.trim();
            
            if(input.equalsIgnoreCase("bye")) {
                finished = true;
            }
            else if(){
                String reposnse = reposnder.generateResponse();
                System.out.println(response);
            }
            
            else{
                String response = responder.generateRandomResponse();
                System.out.println(response);
            }
        }

        printGoodbye();
    }

    /**
     * Print a welcome message to the screen.
     */
    private void printWelcome()
    {
        System.out.println("Welcome to the DodgySoft Technical Support System.");
        System.out.println();
        System.out.println("Please tell us about your problem.");
        System.out.println("We will assist you with any problem you might have.");
        System.out.println("Please type 'bye' to exit our system.");
    }

    /**
     * Print a good-bye message to the screen.
     */
    private void printGoodbye()
    {
        System.out.println("Nice talking to you. Bye...");
    }
}

