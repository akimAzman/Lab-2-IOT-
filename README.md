# Lab-2-IOT-

# Exercise 3
class SavingsAccount(BankAccount):

    def __init__(self):
        super().__init__()
        self._interestRate = 0.06

    def interest(self):
        self._balance = self._balance + (self._balance * self._interestRate)
        return self._balance

