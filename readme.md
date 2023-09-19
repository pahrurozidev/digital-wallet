# Digital Wallet Website

This Digital Wallet website allows users to manage their funds with deposit and withdrawal features. It incorporates essential JavaScript concepts such as classes, switch statements, and try-catch-finally statements for smooth functionality.

## Instructions

1. **Open the Website**: Simply open the HTML file in your preferred web browser to access the Digital Wallet interface.

2. **Check Your Balance**: On the main page, you'll see your current balance displayed as "$100.00" under the "Your Balance" section.

3. **Make a Transaction**:
   - Select the transaction type by choosing between "Deposit" and "Withdraw" from the dropdown menu in the "Make a Transaction" section.
   - Enter the desired transaction amount in the "Amount" field. You can use up to two decimal places (e.g., 10.50).
   - Click the "Submit" button to process your transaction.

4. **Transaction Result**:
   - After each transaction attempt, you'll receive a result message displayed under the "Transaction Result" section.
   - The message will inform you whether the transaction was successful or if an error occurred.

## How It Works

### Wallet Class

The website employs object-oriented programming with a `Wallet` class that encapsulates the user's balance. The class includes two methods:

- `constructor(balance)`: Initializes the wallet with an initial balance.
- `deposit(amount)`: Adds the specified amount to the wallet's balance.
- `withdraw(amount)`: Subtracts the specified amount from the wallet's balance, provided there are sufficient funds. If not, it throws an error.

### Switch Statements

The user's choice of transaction type (deposit or withdraw) is processed using a switch statement. This allows the website to execute the appropriate method based on the user's selection.

```javascript
switch (transactionType) {
    case "deposit":
        wallet.deposit(amount);
        break;
    case "withdraw":
        wallet.withdraw(amount);
        break;
    default:
        throw new Error("Invalid transaction type");
}
```
## Try-Catch-Finally Statements

To ensure smooth error handling, this Digital Wallet website makes use of try-catch-finally statements. These statements are crucial for maintaining a seamless user experience during transactions, handling errors gracefully, and keeping the user interface clean.

```javascript
try {
    // Transaction logic here
} catch (error) {
    // Handle and display the error message
} finally {
    // Clear the input field
    document.getElementById("amount").value = "";
}
```

The implementation of try-catch-finally statements in this Digital Wallet website follows this structured approach:

- **Try Block**: Inside the try block, the website executes the transaction logic, attempting to carry out the selected transaction type (deposit or withdrawal).

- **Catch Block**: In the event of an error during the transaction, such as insufficient balance, the catch block takes over to gracefully manage the error. It displays a user-friendly error message to inform users about the encountered issue.

- **Finally Block**: The finally block ensures that the input field is cleared after each transaction attempt, maintaining a clean and consistent user interface.

This error-handling mechanism not only enhances the reliability of the website but also provides users with a seamless experience when managing their digital wallet transactions.
