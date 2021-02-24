# Associated Profit Splitter Smart Contract

## The purpose of the contract is to accept Ether into the contract and divide the Ether evenly among the associate level employees. This will allow the Human Resources department to pay employees quickly and efficiently.

### Creating the Contract

1. The contract starts off with creating the three payable addresses for each of the three employees.
2. A constructor is created which will allow for the person using the contract to input the three addresses for the three employees that he/she wants to pay.
3. Then a balance function and it must return the contract's current balance. (the balance of the contract should always return 0)
4. Next the deposit fucntion is created. This is what allows to transfer money to each employee account.
  * The amount given should be dvided equally between the 3         employees  (uint amount = msg.value / 3; )
  * Then transfer the amounts (employeeOne.transfer(amount);) and repeat same process for every employee.
  * Then because no decimals should be left, transfer the remainder to the sender using ((msg.sender.transfer(msg.value - amount * 3);)
5. Fincally, because there is no withdraw function. The contract needs an external payable function that forces the deposit function to be used. So within the exteranl payable call the "deposit(); " function.

### Compiling the Contract

* Once the Contract is written we need to compile it clicking the button on the left that says compile.
* Next click on compile, and if no errrors are found then the contract will be compiled and ready for deployment

### Deploying the Contract
