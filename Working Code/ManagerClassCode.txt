package Payroll;

// This is the Public Class for The Manager. 
public class manager {

    // These are Private Variables declared & Initialised with default values, accessible in this Class only.
    private String name = "";
    private String address = "";
    private String PPSNo = "";
    private int payrollNo = 0;
    private String DOB = "";
    private int age = 0;
    private int yearsOfService = 0;
    private int monthlySalary = 0;
    private int teamSalesAchieved = 0;
    private int bonus = 0;


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
    public void setYearsOfService(int YearsOfServiceText)
    {
        yearsOfService = YearsOfServiceText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getYearsOfService()
    {
        return yearsOfService;
    }

    // This method calculates the Monthly Salary based on the
    // Years of Service with the Company & Returns the Value.
    public int getMonthlySalary()
    {
        if(yearsOfService <= 5)
        {
            monthlySalary = 2500;
        }
        else if(yearsOfService <= 10)
        {
            monthlySalary = 3000;
        }
        else if(yearsOfService <= 15)
        {
            monthlySalary = 4000;
        }
        else if(yearsOfService <= 20)
        {
            monthlySalary = 5000;
        }
        else
        {
            monthlySalary = 6000;
        }
        return monthlySalary;
    }

    // This Method sets the Variable to the new Variable inside the Method
    public void setTeamSalesAchieved(int teamSalesAchievedText)
    {
        teamSalesAchieved = teamSalesAchievedText;
    }

    // Get Method that when called upon, sends the value to the main frame that has been entered in the TextField
    public int getTeamSalesAchieved()
    {
        return teamSalesAchieved; 
    }

    // This method calculates the Bonus based on the Amount of Team Sales
    // the Manager Achieved in a Particular Month.
    public int getBonus()
    { 
        if(teamSalesAchieved  > 150)
        {
            bonus =  25;
        }
        else if(teamSalesAchieved > 100)
        {
            bonus = 20;
        }
        else if(teamSalesAchieved > 50)
        {
            bonus = 15;
        }
        else
        {
            bonus = 0;
        }
        return bonus;
    }

    // This Method Calculates the Actual Bonus Amount for the Month.
    public int bonusCalculation(int mbSalary, int mbBonus)
    {
        int bonusCalc = mbSalary * mbBonus / 100;
        return bonusCalc;
    }

    // Method for Calculating the Total Wage before Tax.
    public int grossPayCalc(int mgSalary, int mgBonus)
    {
        int grossPayCalc = (mgSalary * mgBonus/100) + mgSalary;
        return grossPayCalc;
    }


    // This Method returns the Net Pay. 
    public int WageCalculation(int mSalary, int mBonus)
    {
        double tax = .2;
        double GrossPay = (mSalary * mBonus/100.0) + mSalary;
        double taxAmount = GrossPay * tax;
        double netPay = (GrossPay - taxAmount);
        int finalPay = (int) netPay ;

        return finalPay;
    }
}