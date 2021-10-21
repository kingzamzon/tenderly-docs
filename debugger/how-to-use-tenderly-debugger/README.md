# How to use Tenderly Debugger

The Visual Debugger is one of the tools people love the most. Instead of wasting countless hours debugging transactions, you can use the Visual Debugger so you can focus more on buidling and less on scratching your head.

![](<../../.gitbook/assets/image (15).png>)

Just like you would expect from a debugger in other modern languages, you have the current call stack at the left-hand side, Jump Up/Previous/Next stack navigation controls, and most importantly, **Input, Output, Local and State variables** to the right.

**The level of detail present here doesn't exist anywhere else and reduces development time by orders of magnitude**.

## Debugging a Transaction

Go to the **Transactions **tab in the left navigation bar, and paste the transaction hash into the top **Explorer **bar:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.15.20.png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.15.58.png>)

By clicking on **Contracts** (or **Addresses**) on the left we can see all of the contracts that have been involved in this transaction:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.17.52.png>)

When you click on the **Debugger **tab, you will see the following:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.26.51.png>)

On the top right you will see the code that was executed, below are the listed parameters for code execution and inputs that were passed into the function.

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.28.19.png>)

For example the function `multicall` has a single input labeled `data` which is shown below:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.29.15.png>)

On the left you will see a list of all the function that were called in this transaction which are further broken down in the order of execution in the [**Stack Trace**](broken-reference):

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.30.15.png>)

You can search for the exact term in the code either by double clicking a word and searching for it using the markup to the right, or by hitting CTRL+F to open up the integrated search bar:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.38.01.png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.38.49.png>)

### Stack Traces

While we debug our transaction, the **Stack Trace **will show all of the functions that are being executed in each step:

![](<../../.gitbook/assets/image (69) (1) (1).png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.35.12.png>)

### Decoded Events/Logs

When in **Transaction **overview, **Events **tab will show you all of the events emitted in this transaction, with options to filter them out by _event name_ or _contract/address_:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.19.45.png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.20.12.png>)

### Decoded State Changes

**State Changes **allows us to see all of the variables that were changed/updated during the course of the transaction:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.21.17.png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.22.19.png>)

### Gas Profiler

**Gas Profiler **shows you the most detailed view of how your transaction spent gas, down to every single function call and the amount of gas spent by it:

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.23.42.png>)

![](<../../.gitbook/assets/Screenshot 2021-10-14 at 14.24.05.png>)