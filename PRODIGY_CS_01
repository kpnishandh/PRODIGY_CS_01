import sys
from colorama import Fore, init

def caesar_cipher(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            base = ord('a') if char.islower() else ord('A')
            shifted_char = chr((ord(char) - base + shift) % 26 + base)
            result += shifted_char
        else:
            result += char
    return result

def main():
    init()  # Initialize colorama for colored text
    try:
        plaintext = input("Enter your message: ")
        shift = int(input("Enter the shift value (positive for encryption, negative for decryption): "))
        encrypted_text = caesar_cipher(plaintext, shift)
        print(f"{Fore.GREEN}Encrypted text: {encrypted_text}{Fore.RESET}")
    except ValueError:
        print(f"{Fore.RED}Invalid input. Please enter a valid shift value.{Fore.RESET}")

if __name__ == "__main__":
    main()
