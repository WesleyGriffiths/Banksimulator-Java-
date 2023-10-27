# Bank simulator

This is a Java project that simulates a bank through the use of synchronized threads.
The synchronization allows multiple withdrawal and depositing threads to operate without there being errors such as withdrawing from an account with a $0 balance

There are 5 depositor threads and 10 withdrawal threads, along with one auditor thread all working on a single bank account.
The auditor thread simply periodically records the balance of the account and the amount of transactions done since the last audit, while withdrawal threads perform withdrawals and deposit threads make deposits.

Threads get blocked if another thread is currently executing, Withdrawal threads can be blocked for the account having insufficient funds.
Threads go to "sleep" for a period of time after being active so it is unlikely for one thread to take over CPU and run repeatedly.
The threads are set to run endlessly until the process is manually terminated
