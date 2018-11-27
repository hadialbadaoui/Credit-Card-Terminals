# Credit-Card-Terminals
This Java Library Communicate With Vx520

If you want to try how that library work please, follow this link: https://github.com/hadialbadaoui/Vx520-JAVA-Interface.git
to download a simple application, help you to communicate with Vx520.

# Note: Don't forget to download all 3 libraries:
- jssc-2.8.0.jar
- org.json.jar
- Credit_Card_Terminals.jar
# And the 3 classes too, You can found it in the link below:
- Settlement
- Transaction
- Status

Tutorial:

1- Create a reference from class "Manage". Example: Manage MR = new Manage();
    Manage Class contains these Attributes:
      - boolean status: return true or false.
      - String "errormessage": return an error message when the status was false.
      - Status statuslog: return all status happens in Vx520.
      - boolean settlementfound: return true when Vx520 return a settlement response.
      - Settlement settlement: Class has all attribute of settlement response.
      - boolean transactionfound: return true when Vx520 return a transaction response.
      - Transaction transaction: Class has all attribute of transaction response.

2- Create a reference from class "AreebaPOS". Example: AreebaPOS apos = new AreebaPOS(COM);
  COM is a string variable containing the name of the serial port. Example: "COM1"
  
  # Now you can create a reference from class "AreebaPOS" without parameter: the library will return the name of COM connected to serial port of Vx520.

3- We have three methods to use:
   - SendTestToPOS: 
        to test the connectivity of Vx520.
   - SendTransactionToPOS(String TypeRequest, String Reference, String Amount, String Currency): 
        Send a transaction to Vx520:
        
          . TypeRequest: "Sale", "Refund" and "Void".
          
          . Reference: Should be 8 digits.
          
          . Amount: Should be 12 digits.
          
          . Currency: Should be ($/USD) or (LL/LBP).
          
        This function return a class Manage.
        
   - SendSettlementToPOS: This function return a class Manage.

Thank you, best regards.
