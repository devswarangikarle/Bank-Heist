# Bank-Heist

A boy is planning a heist in the bank. He is planning to hijack the bank for D days and print the money. The initial rate of printing the currency is P dollars per day and they increase the production by Q dollars after every interval of d days. For example, after d days the rate is P + Q dollars per day, and after 2d days the rate is P + 2Q dollars per day, and so on. Output the amount of money they will be able to print in the given period.

def solve():

    D, d, P, Q = map(int, input().split())
    
    n = D // d  
    r = D % d   
    
    total_full_intervals = d * (n * P + Q * (n * (n - 1)) // 2)
    
    total_remaining_days = r * (P + n * Q)   
    total_money = total_full_intervals + total_remaining_days
    
    print(total_money)
solve()
