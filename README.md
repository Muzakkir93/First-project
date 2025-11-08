sig =  ["+","-","×","÷","%","∆","!","√"]
def under_root(no_1):
    (no_1 ** 0.5)
print("----------------------calculator-----------------------",end = "                                                       ")
def factorial(no1):
    g = 1
    for i in range(1, no1 + 1):
        g *= i
    print(g)
    if g == 1 or 0:
        return 1
while True:
    no1 = (input("number 1 : "))
    if no1.lower() == "exit":
        print("task complete")
        break
    else:
        try:
            no_1 = int(no1)
        except:
            print("error")
        sign = input("sign     : ")
        if sign not in sig :
            print("error")
            continue
        if sign == "!":
            factorial(no_1)
        elif sign == "√":
            under_root(no_1)
        else:
            try:
                no2 = int(input("number 2 : "))
            except:
                print("error")
                continue
            if sign == "+":
                print("         : =", no_1 + no2)
            elif sign == "-":
                print("         : =", no_1 - no2)
            elif sign == "×":
                print("          :=", no_1 * no2)
            elif sign == "÷":
                print("         : =", no_1 / no2)
            elif sign == "%":
                print("         : =", no_1 * no2 / 100, "%")
            elif sign == "∆":
                print("         : =", no_1 ** no2)