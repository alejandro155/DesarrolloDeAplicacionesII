# DesarrolloDeAplicacionesII
Se subira codigo y mas.
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package Inicio;

import javax.microedition.midlet.*;
import javax.microedition.lcdui.*;

/**
 * @author TICS
 */
public class Prueba extends MIDlet implements CommandListener {
    
    private boolean midletPaused = false;
    public int resp0,res_correctas,res_incorrectas=0;
    public String val;

//<editor-fold defaultstate="collapsed" desc=" Generated Fields ">                      
    private Form Intro;
    private StringItem stringItem;
    private Form PREG1;
    private ChoiceGroup choiceGroup;
    private Form PREG2;
    private ChoiceGroup choiceGroup1;
    private Form PREG3;
    private ChoiceGroup choiceGroup2;
    private Form PREG4;
    private TextField textField;
    private Form PREG5;
    private ChoiceGroup choiceGroup3;
    private Alert alert;
    private Form FIN;
    private StringItem stringItem1;
    private Command okCommand;
    private Command okCommand1;
    private Command okCommand2;
    private Command okCommand3;
    private Command okCommand4;
    private Command okCommand5;
    private Command okCommand6;
//</editor-fold>                    
    /**
     * The Prueba constructor.
     */
    public Prueba() {
    }

//<editor-fold defaultstate="collapsed" desc=" Generated Methods ">                       
//</editor-fold>                     

//<editor-fold defaultstate="collapsed" desc=" Generated Method: initialize ">                                           
    /**
     * Initializes the application. It is called only once when the MIDlet is
     * started. The method is called before the <code>startMIDlet</code> method.
     */
    private void initialize() {
                                         
        // write pre-initialize user code here
                                           
        // write post-initialize user code here
}                            
//</editor-fold>                          

//<editor-fold defaultstate="collapsed" desc=" Generated Method: startMIDlet ">                                        
    /**
     * Performs an action assigned to the Mobile Device - MIDlet Started point.
     */
    public void startMIDlet() {
                                      
        // write pre-action user code here
                                        
        // write post-action user code here
}                             
//</editor-fold>                           

//<editor-fold defaultstate="collapsed" desc=" Generated Method: resumeMIDlet ">                                         
    /**
     * Performs an action assigned to the Mobile Device - MIDlet Resumed point.
     */
    public void resumeMIDlet() {
                                       
        // write pre-action user code here
                                         
        // write post-action user code here
}                              
//</editor-fold>                            

//<editor-fold defaultstate="collapsed" desc=" Generated Method: switchDisplayable ">                                              
    /**
     * Switches a current displayable in a display. The <code>display</code>
     * instance is taken from <code>getDisplay</code> method. This method is
     * used by all actions in the design for switching displayable.
     *
     * @param alert the Alert which is temporarily set to the display; if
     * <code>null</code>, then <code>nextDisplayable</code> is set immediately
     * @param nextDisplayable the Displayable to be set
     */
    public void switchDisplayable(Alert alert, Displayable nextDisplayable) {
                                            
        // write pre-switch user code here
Display display = getDisplay();                                               
        if (alert == null) {
            display.setCurrent(nextDisplayable);
        } else {
            display.setCurrent(alert, nextDisplayable);
        }                                             
        // write post-switch user code here
}                                   
//</editor-fold>                                 

//<editor-fold defaultstate="collapsed" desc=" Generated Method: commandAction for Displayables ">                                                 
    /**
     * Called by a system to indicated that a command has been invoked on a
     * particular displayable.
     *
     * @param command the Command that was invoked
     * @param displayable the Displayable where the command was invoked
     */
    public void commandAction(Command command, Displayable displayable) {
                                               
 // write pre-action user code here
if (displayable == FIN) {                                           
            if (command == okCommand6) {                                         
 // write pre-action user code here
exitMIDlet();                                           
 // write post-action user code here
}                                           
} else if (displayable == Intro) {
    if (command == okCommand) {                                         
 // write pre-action user code here
exitMIDlet();                                           
 // write post-action user code here
}                                           
} else if (displayable == PREG1) {
    if (command == okCommand1) {                                         
 // write pre-action user code here
 resp0=this.choiceGroup.getSelectedIndex();
 if(resp0==1){
     res_correctas=res_correctas+1;
 }
        switchDisplayable(null, getIntro());                                           
 // write post-action user code here
}                                           
} else if (displayable == PREG2) {
    if (command == okCommand2) {                                         
 // write pre-action user code here
 resp0=this.choiceGroup1.getSelectedIndex();
 if(resp0==1){
     res_correctas=res_correctas+1;
 }
        switchDisplayable(null, getPREG1());                                           
 // write post-action user code here
}                                           
} else if (displayable == PREG3) {
    if (command == okCommand3) {                                         
 // write pre-action user code here
 
        switchDisplayable(null, getPREG4());                                            
 // write post-action user code here
 resp0=this.choiceGroup2.getSelectedIndex();
 if(resp0==1){
     res_correctas=res_correctas+1;
 }
    }                                            
} else if (displayable == PREG4) {
    if (command == okCommand4) {                                          
 // write pre-action user code here
 val=this.textField.getString();
 if(val.equals("C")){
     res_correctas=res_correctas+1;
 }
        switchDisplayable(null, getPREG5());                                            
 // write post-action user code here
}                                            
} else if (displayable == PREG5) {
    if (command == okCommand5) {                                          
 // write pre-action user code here
switchDisplayable(getAlert(), getFIN());                                            
 // write post-action user code here
 resp0=this.choiceGroup3.getSelectedIndex();
 if(resp0==2){
     res_correctas=res_correctas+1;
 }
 res_incorrectas=5-res_correctas;
 this.alert.setString("ACIERTOS"+res_correctas+"ERRORES"+res_correctas);
            }                                                   
        }                                                 
 // write post-action user code here
}                                
//</editor-fold>                              

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: Intro ">                                   
    /**
     * Returns an initialized instance of Intro component.
     *
     * @return the initialized component instance
     */
    public Form getIntro() {
        if (Intro == null) {
                                 
 // write pre-init user code here
Intro = new Form("form", new Item[]{getStringItem()});                                    
            Intro.addCommand(getOkCommand());
            Intro.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return Intro;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: stringItem ">                                   
    /**
     * Returns an initialized instance of stringItem component.
     *
     * @return the initialized component instance
     */
    public StringItem getStringItem() {
        if (stringItem == null) {
                                 
 // write pre-init user code here
stringItem = new StringItem("Bienvenido..", "TEST SOBRE MI..");                                   
 // write post-init user code here
}                         
        return stringItem;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: PREG1 ">                                   
    /**
     * Returns an initialized instance of PREG1 component.
     *
     * @return the initialized component instance
     */
    public Form getPREG1() {
        if (PREG1 == null) {
                                 
 // write pre-init user code here
PREG1 = new Form("form", new Item[]{getChoiceGroup()});                                    
            PREG1.addCommand(getOkCommand1());
            PREG1.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return PREG1;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: choiceGroup ">                                   
    /**
     * Returns an initialized instance of choiceGroup component.
     *
     * @return the initialized component instance
     */
    public ChoiceGroup getChoiceGroup() {
        if (choiceGroup == null) {
                                 
 // write pre-init user code here
choiceGroup = new ChoiceGroup("Una red es un conjunto de equipos unidos?", Choice.EXCLUSIVE);                                    
            choiceGroup.append("Falso.", null);
            choiceGroup.append("Verdadero.", null);
            choiceGroup.setSelectedFlags(new boolean[]{false, false});                                  
 // write post-init user code here
}                         
        return choiceGroup;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: PREG2 ">                                   
    /**
     * Returns an initialized instance of PREG2 component.
     *
     * @return the initialized component instance
     */
    public Form getPREG2() {
        if (PREG2 == null) {
                                 
 // write pre-init user code here
PREG2 = new Form("form", new Item[]{getChoiceGroup1()});                                    
            PREG2.addCommand(getOkCommand2());
            PREG2.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return PREG2;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: choiceGroup1 ">                                   
    /**
     * Returns an initialized instance of choiceGroup1 component.
     *
     * @return the initialized component instance
     */
    public ChoiceGroup getChoiceGroup1() {
        if (choiceGroup1 == null) {
                                 
 // write pre-init user code here
choiceGroup1 = new ChoiceGroup("Redes locales como una oficina.", Choice.MULTIPLE);                                    
            choiceGroup1.append("MAN", null);
            choiceGroup1.append("LAN", null);
            choiceGroup1.append("WAN", null);
            choiceGroup1.setSelectedFlags(new boolean[]{false, false, false});                                  
 // write post-init user code here
}                         
        return choiceGroup1;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: PREG3 ">                                   
    /**
     * Returns an initialized instance of PREG3 component.
     *
     * @return the initialized component instance
     */
    public Form getPREG3() {
        if (PREG3 == null) {
                                 
 // write pre-init user code here
PREG3 = new Form("form", new Item[]{getChoiceGroup2()});                                    
            PREG3.addCommand(getOkCommand3());
            PREG3.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return PREG3;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: choiceGroup2 ">                                   
    /**
     * Returns an initialized instance of choiceGroup2 component.
     *
     * @return the initialized component instance
     */
    public ChoiceGroup getChoiceGroup2() {
        if (choiceGroup2 == null) {
                                 
 // write pre-init user code here
choiceGroup2 = new ChoiceGroup("Medio de Transmicion no Guiado como:", Choice.POPUP);                                    
            choiceGroup2.append("Par Trenzado", null);
            choiceGroup2.append("Antenas.", null);
            choiceGroup2.append("Fibra Optica.", null);
            choiceGroup2.setSelectedFlags(new boolean[]{false, false, false});                                  
 // write post-init user code here
}                         
        return choiceGroup2;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: PREG4 ">                                   
    /**
     * Returns an initialized instance of PREG4 component.
     *
     * @return the initialized component instance
     */
    public Form getPREG4() {
        if (PREG4 == null) {
                                 
 // write pre-init user code here
PREG4 = new Form("form", new Item[]{getTextField()});                                    
            PREG4.addCommand(getOkCommand4());
            PREG4.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return PREG4;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: textField ">                                   
    /**
     * Returns an initialized instance of textField component.
     *
     * @return the initialized component instance
     */
    public TextField getTextField() {
        if (textField == null) {
                                 
 // write pre-init user code here
textField = new TextField("Escribe la clase de la direccion 192.168.1.12", "", 32, TextField.ANY);                                   
 // write post-init user code here
}                         
        return textField;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: PREG5 ">                                   
    /**
     * Returns an initialized instance of PREG5 component.
     *
     * @return the initialized component instance
     */
    public Form getPREG5() {
        if (PREG5 == null) {
                                 
 // write pre-init user code here
PREG5 = new Form("form", new Item[]{getChoiceGroup3()});                                    
            PREG5.addCommand(getOkCommand5());
            PREG5.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return PREG5;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: choiceGroup3 ">                                   
    /**
     * Returns an initialized instance of choiceGroup3 component.
     *
     * @return the initialized component instance
     */
    public ChoiceGroup getChoiceGroup3() {
        if (choiceGroup3 == null) {
                                 
 // write pre-init user code here
choiceGroup3 = new ChoiceGroup("Cual es el grupo de colores utilizado en un cable de red.", Choice.MULTIPLE);                                    
            choiceGroup3.append("B/N,A,B,C", null);
            choiceGroup3.append("C,B/C,V,A", null);
            choiceGroup3.append("B/N,B,N", null);
            choiceGroup3.setSelectedFlags(new boolean[]{false, false, false});                                  
 // write post-init user code here
}                         
        return choiceGroup3;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: alert ">                                   
    /**
     * Returns an initialized instance of alert component.
     *
     * @return the initialized component instance
     */
    public Alert getAlert() {
        if (alert == null) {
                                 
 // write pre-init user code here
alert = new Alert("RESULTADO");                                    
            alert.setTimeout(Alert.FOREVER);                                  
 // write post-init user code here
}                         
        return alert;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: FIN ">                                   
    /**
     * Returns an initialized instance of FIN component.
     *
     * @return the initialized component instance
     */
    public Form getFIN() {
        if (FIN == null) {
                                 
 // write pre-init user code here
FIN = new Form("form", new Item[]{getStringItem1()});                                    
            FIN.addCommand(getOkCommand6());
            FIN.setCommandListener(this);                                  
 // write post-init user code here
}                         
        return FIN;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand ">                                   
    /**
     * Returns an initialized instance of okCommand component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand() {
        if (okCommand == null) {
                                 
 // write pre-init user code here
okCommand = new Command("Iniciar.", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand1 ">                                   
    /**
     * Returns an initialized instance of okCommand1 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand1() {
        if (okCommand1 == null) {
                                 
 // write pre-init user code here
okCommand1 = new Command("Ok", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand1;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand2 ">                                   
    /**
     * Returns an initialized instance of okCommand2 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand2() {
        if (okCommand2 == null) {
                                 
 // write pre-init user code here
okCommand2 = new Command("NEXT", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand2;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand3 ">                                   
    /**
     * Returns an initialized instance of okCommand3 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand3() {
        if (okCommand3 == null) {
                                 
 // write pre-init user code here
okCommand3 = new Command("Ok", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand3;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand4 ">                                   
    /**
     * Returns an initialized instance of okCommand4 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand4() {
        if (okCommand4 == null) {
                                 
 // write pre-init user code here
okCommand4 = new Command("Ok", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand4;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand5 ">                                   
    /**
     * Returns an initialized instance of okCommand5 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand5() {
        if (okCommand5 == null) {
                                 
 // write pre-init user code here
okCommand5 = new Command("Ok", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand5;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: okCommand6 ">                                   
    /**
     * Returns an initialized instance of okCommand6 component.
     *
     * @return the initialized component instance
     */
    public Command getOkCommand6() {
        if (okCommand6 == null) {
                                 
 // write pre-init user code here
okCommand6 = new Command("Ok", Command.OK, 0);                                   
 // write post-init user code here
}                         
        return okCommand6;
    }
//</editor-fold>                       

//<editor-fold defaultstate="collapsed" desc=" Generated Getter: stringItem1 ">                                   
    /**
     * Returns an initialized instance of stringItem1 component.
     *
     * @return the initialized component instance
     */
    public StringItem getStringItem1() {
        if (stringItem1 == null) {                                 
 // write pre-init user code here
stringItem1 = new StringItem("La evaluacion a terminado.", null);                                   
 // write post-init user code here
}                         
        return stringItem1;
    }
//</editor-fold>                       

    /**
     * Returns a display instance.
     *
     * @return the display instance.
     */
    public Display getDisplay() {
        return Display.getDisplay(this);
    }

    /**
     * Exits MIDlet.
     */
    public void exitMIDlet() {
        switchDisplayable(null, null);
        destroyApp(true);
        notifyDestroyed();
    }

    /**
     * Called when MIDlet is started. Checks whether the MIDlet have been
     * already started and initialize/starts or resumes the MIDlet.
     */
    public void startApp() {
        if (midletPaused) {
            resumeMIDlet();
        } else {
            initialize();
            startMIDlet();
        }
        midletPaused = false;
    }

    /**
     * Called when MIDlet is paused.
     */
    public void pauseApp() {
        midletPaused = true;
    }

    /**
     * Called to signal the MIDlet to terminate.
     *
     * @param unconditional if true, then the MIDlet has to be unconditionally
     * terminated and all resources has to be released.
     */
    public void destroyApp(boolean unconditional) {
    }
    
}
