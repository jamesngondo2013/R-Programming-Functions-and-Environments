# R Programming Functions and Environments

```# James Ngondo - 16232372
account <- function(acc){ #
  accnum <- acc
  lodgement <- 0
  withdrawal <- 0
  closingBal<- 0
  openAmount <- 0
  currentBal <- 0
  txnum <- 0
  transId <-0
  transactionList<-list() #empty list that will hold accnum, transNo,date,balance
  totalListTrans<-list()
  list(credit = function(y){  #list of functions used for the account transactions
    openAmount <- currentBal
    lodgement <<- y
    currentBal <<-  currentBal + y
    closingBal <<- currentBal
    transId <<- transId+1
    #appending each transaction to a new list 
    totalListTrans <<- append(totalListTrans,transactionList[[length(transactionList)+1]] <- list(accnum,                                   TransNo=transId,Date=date(),OpeningAmount = openAmount,Lodgement=lodgement,Balance= currentBal, ClosingBalance=closingBal))
    #printing the list of transactions
    print(transactionList[[length(transactionList)+1]] <- list(accnum, TransNo=transId,Date=date(),OpeningAmount =                           openAmount,Lodgement=lodgement,Balance= currentBal, ClosingBalance=closingBal))
    },
    balance = function(){  #balance function
      currentBal     
    },
    debit = function(x){  #debit function
      openAmount <<- currentBal
      currentBal <<- currentBal - x
      withdrawal <<- x
      closingBal <<- currentBal
      transId <<- transId+1
      #appending each transaction to a new list 
      totalListTrans <<- append(totalListTrans,transactionList[[length(transactionList)+1]] <- list(accnum,                                   TransNo=transId,Date=date(),OpeningAmount = openAmount,Lodgement=lodgement,Balance= currentBal, ClosingBalance=closingBal))
      #printing the list of transactions
      print(transactionList[[length(transactionList)+1]] <- list(accnum, TransNo= transId,Date=date(),OpeningAmount =                         openAmount,Withdrawal=withdrawal,Balance= currentBal,ClosingBalance=closingBal))     
    },
    transaction = function(){  # transaction list function
     
      #printing the list of all transactions and appending each transaction to a new list 
      print(totalListTrans)     
    },
    accNumber = function(){  # account number function
    print(acc)    
    }
    
    )
}
a1<-account("AIB-200-90-30") #create an object of the account
#calling different functions for performing the transactions
a1$accNumber()
a1$credit(200)
a1$balance()
a1$debit(50)
a1$balance()
a1$credit(10)
a1$balance()
a1$transaction()
```
