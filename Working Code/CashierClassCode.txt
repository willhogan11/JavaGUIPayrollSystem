package Payroll;

// This is the Public Class for The Cashier. 
public class cashier {

    // These are Private Variables declared & Initialised with default values, Accessible in this Class.
    private String name = "";
    private String address = "";
    private String PPSNo = "";
    private int payrollNo = 0;
    private String DOB = "";
    private int age = 0;
    private int hoursWorked = 0;
    private int hourlyRate = 0;
    private int overTime = 0;
    private int cashierOverTimeRate = 0;


    // The below methods are getting and setting the values inputted into the text fields
    // When they are called upon the Stored values are sent to the Associated Frame.

    // Setting name, sets the Value of the Variable to the Value of the textField.
    public void setName(String nameText)
    {
        name = nameText;
    }

    // Getting Name, when called upon, sends the value to the main frame that has been entered in the TextField
    public String getName()
    {
        return name;
    }

    // This repeats as far as the getOverTime Method.
    public void setAddress(String addressText)
    {
        address = addressText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public String getAddress()
    {
        return address;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setPPSNo(String PPSNoText)
    {
        PPSNo = PPSNoText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public String getPPSNo()
    {
        return PPSNo;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setPayrollNo(int payrollNoText)
    {
        payrollNo = payrollNoText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getPayrollNo()
    {
        return payrollNo;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setDOB(String DOBText)
    {
        DOB = DOBText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public String getDOB()
    {
        return DOB;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setAge(int ageText)
    {
        age = ageText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getAge()
    {
        return age;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setHoursWorked(int hoursWorkedValue)
    {
        hoursWorked = hoursWorkedValue;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getHoursWorked()
    {
        return hoursWorked;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setHourlyRate(int hourlyRateValue)
    {
        hourlyRate = hourlyRateValue;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getHourlyRate()
    {
        return hourlyRate;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setOverTime(int overTimeText)
    {
        overTime = overTimeText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getOverTime()
    {
        return overTime;
    }

    // Method to Calculate & return the Wage.
    public int calcWage(int hoursWorkedCalc, int hourlyRateCalc)
    {
        double wage = hoursWorkedCalc * hourlyRateCalc;
        return (int) wage;
    }

    // This Method Calculates & Returns the Overtime Rate. 
    public int calcOverTime(int HoursWorked)
    {
        cashierOverTimeRate = (HoursWorked * 150) / 100;

        return cashierOverTimeRate;
    }

    // Method to Calculate & Return Gross Pay.
    public int calcGross(int cHoursWorkedCalc, int cHourlyRateCalc, int cOverTimeRate, int otHoursWorked)
    {
        double grossPay = (cHoursWorkedCalc * cHourlyRateCalc) + (cOverTimeRate * otHoursWorked);

        return (int) grossPay;
    }

    // Method to Calculate & Return Net Pay.
    public int calcNetPay(int netPayHoursWorked, int netPayHourlyRateCalc, int netPayOverTimeRate, int netPayOTHoursWorked)
    {
        double tax = 20;
        double grossPay = (netPayHoursWorked * netPayHourlyRateCalc) + (netPayOverTimeRate * netPayOTHoursWorked);
        double taxAmount = (grossPay * tax / 100);
        double netPay = grossPay - taxAmount;

        return (int) netPay;
    }
}