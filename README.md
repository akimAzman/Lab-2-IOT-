# Lab-2-IOT-

# Exercise 4
class FeeSavingsAccount(SavingsAccount):

    def __init__(self):
        super().__init__()
        self.fee = 1

    def withdraw(self, pin, amount):
        if self.pin == pin:
            self._balance = self._balance - (amount + self.fee)
            return self._balance
        else:
            return "Wrong Pin"


my_bank = BankAccount()
savings_account = SavingsAccount()
fee_account = FeeSavingsAccount()

print(savings_account.interest())

pin = input('insert pin')
amount = int(input('insert amount'))

newpin = input('newpin')
oldpin = input('oldpin')
print(my_bank.deposit(pin=pin, amount=amount))
# print(my_bank.withdraw('pin', 2))
# print(fee_account.deposit(pin='pin', amount=12))
# print(fee_account.withdraw('pin', 2))
print(my_bank.change_pin(oldpin, newpin))
