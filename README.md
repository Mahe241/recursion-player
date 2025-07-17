def player_A(n):
    if n==0:
        print("player A reached!! player A loses")
        return 
    print(f"\n player A's turn.Current number{n}")
    move=int(input("player A,subtract 1 or 2:"))
    while move not in [1,2]:
        move=int(input("player A,subtract 1 or 2:"))
    player_B(n-move)
def player_B(n):
    if n<=0:
        print("player B reached 0!! player B loses")
        return
    print(f"\n player B's turn.Current number{n}")
    move=int(input("player B,subtract 1 or 2:"))
    while move not in [1,2]:
        move=int(input("player B,subtract 1 or 2:"))
    player_A(n-move)
start=int(input("enter starting number:"))
player_A(start)
