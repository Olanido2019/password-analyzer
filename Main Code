#!/usr/bin/env python3

import math
from zxcvbn import zxcvbn
from colorama import Fore, Style, init

init(autoreset=True)


def entropy_estimate(password):
    pools = 0

    if any(c.islower() for c in password):
        pools += 26

    if any(c.isupper() for c in password):
        pools += 26

    if any(c.isdigit() for c in password):
        pools += 10

    if any(not c.isalnum() for c in password):
        pools += 32

    if pools == 0:
        return 0

    return math.log2(pools) * len(password)


def analyze(password):
    zx = zxcvbn(password)
    entropy = entropy_estimate(password)

    print(f"\n{Fore.CYAN}Analyzing password{Style.RESET_ALL}: {password}")
    print(f"zxcvbn score: {zx['score']}/4")
    print(f"Entropy estimate: {entropy:.2f} bits")
    print(f"Feedback: {zx['feedback']}")

    if entropy < 30:
        print(Fore.RED + "Weak password!" + Style.RESET_ALL)
    elif entropy < 70:
        print(Fore.YELLOW + "Moderate Strength." + Style.RESET_ALL)
    else:
        print(Fore.GREEN + "Strong password!" + Style.RESET_ALL)


if __name__ == "__main__":
    pw = input("Enter password to analyze: ")
    analyze(pw)
