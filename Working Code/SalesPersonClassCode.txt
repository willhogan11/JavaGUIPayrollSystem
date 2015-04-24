package Payroll;

// This is the Public Class for The Sales Person.
public class salesPerson {

    // These are Private Variables declared & Initialised with default values, Accessible in this Class.
    private String name = "";
    private String address = "";
    private String PPSNo = "";
    private int payrollNo = 0;
    private String DOB = "";
    private int age = 0;
    private int hoursWorked = 0;
    private int hourlyRate = 0;
    private int salesAchieved = 0;
    private int commission = 0;


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

    // This Method sets the Variable to the new Variable inside the Method
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
    public double getHourlyRate()
    {
        return hourlyRate;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setSalesAchieved(int salesAchievedValue)
    {
        salesAchieved = salesAchievedValue;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getSalesAchieved()
    {
        return salesAchieved;
    }

    // This Methods deals with Calculating & Returning the Commission based on the Sales Achieved.
    public double getCommission()
    {
        if(salesAchieved >= 10)
        {
            commission = 150;
        }
        else if(salesAchieved >= 15)
        {
            commission = 200;
        }

        else if(salesAchieved >= 20)
        {
            commission = 250;
        }

        else
        {
            commission = 0;
        }
        return commission;
    }

    // Method to Calculate & return the Wage.
    public int calcWage(int hoursWorkedCalc, int hourlyRateCalc)
    {
        double wage = hoursWorkedCalc * hourlyRateCalc;
        return (int) wage;
    }

    // Method to Calculate & Return Gross Pay.
    public int grossPayCalc(int spWage, int spCommission)
    {
        double gross = spWage + spCommission;
        return (int) gross; 
    }

    // Method to Calculate & Return Net Pay. 
    public int netPayCalc(int hoursWorkedCalc, int hourlyRateCalc, int commissionCalc)
    {
         double tax = .2;
         double grossPay = (hoursWorkedCalc * hourlyRateCalc) + commissionCalc;
         double taxAmount = grossPay * tax;
         double netPay = (grossPay - taxAmount);
         int finalPay = (int) netPay ;

         return finalPay;
    }
}