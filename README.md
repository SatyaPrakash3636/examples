### Below codes were converted from Jupyter Notebook to README.md using below command

```bash
jupyter nbconvert --ClearMetadataPreprocessor.enabled=True --ClearOutput.enabled=True --to markdown examples.ipynb
```

```python
import random

def who_wins(user: str, computer: str) -> bool|None:
    """
    Returns True if user wins
    """
    # r>s, s>p, p>r
    if user == "r" and computer == "s" or user == "s" and computer == "p" or user == "p" and computer == "r":
        return True

def rps():
    computer = random.choice(["r", "p", "s"])
    user = input("Enter your choice- Rock(R), Paper(P), Sessior(S): ").lower()
    user_wins = who_wins(user, computer)
    print(f"{computer=}, {user=}")
    if computer == user:
        print("Tie")
    elif user_wins is True:
        print("Yay!!, You won")
    else:
        print("You Lost")

rps()

```

    computer='r', user='s'
    You Lost
