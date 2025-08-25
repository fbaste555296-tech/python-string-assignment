# python-string-assignment
This Python program performs different operations on a sentence, like reversing, counting vowels, and checking palindromes. It uses a menu with options, repeats in a loop, and lets the user enter a new sentence or exit anytime.
<img width="906" height="350" alt="image" src="https://github.com/user-attachments/assets/36e0f35c-605c-4415-a0f6-a902d9274a53" />
<img width="322" height="295" alt="image" src="https://github.com/user-attachments/assets/947557af-a448-4997-a44e-3e4f5b856fb5" />
<img width="266" height="300" alt="image" src="https://github.com/user-attachments/assets/7f20d22c-f9bb-4428-85ea-ea180db38796" />
<img width="258" height="294" alt="image" src="https://github.com/user-attachments/assets/87b2ffbc-08a3-4683-a44c-1377ec680ca1" />
<img width="246" height="330" alt="image" src="https://github.com/user-attachments/assets/8d7ee575-fdc6-48fc-9a11-046e5ca16984" />
<img width="223" height="287" alt="image" src="https://github.com/user-attachments/assets/5ce50762-dd57-4c63-b5c9-671cb4114ee6" />
<img width="220" height="298" alt="image" src="https://github.com/user-attachments/assets/bf3deef2-a709-40bc-8e66-aa1008342249" />
<img width="228" height="283" alt="image" src="https://github.com/user-attachments/assets/9088064c-c86e-42e2-91f7-b910493b9e3b" />
<img width="219" height="289" alt="image" src="https://github.com/user-attachments/assets/799de88e-2cdf-4f76-98f7-a13ff272d44c" />
<img width="235" height="282" alt="image" src="https://github.com/user-attachments/assets/a932ce36-2636-416a-8e01-601d028abdd0" />
<img width="280" height="332" alt="image" src="https://github.com/user-attachments/assets/60afc08f-7300-4b05-b934-3ce5a058ea84" />



My experience by doing this activity was well although this is my first time doing a program using python language it was much easier than java as it suggested codes that best fits to run the program smoothly. By also doing this assignment I have recalled my coding experience when using java and I also came back from the basic to learn more on how to loop because I have already forgotten on how to do it. But then again it's much fun to code in python than java.


def reverse_sentence(sentence):
    return sentence[::-1]

def count_vowels(sentence):
    vowels = "aeiouAEIOU"
    return sum(1 for ch in sentence if ch in vowels)

def check_palindrome(sentence):
    cleaned = "".join(ch.lower() for ch in sentence if ch.isalnum())
    return cleaned == cleaned[::-1]

def find_and_replace(sentence):
    word_to_find = input("Enter word to find: ")
    word_to_replace = input("Enter word to replace with: ")
    return sentence.replace(word_to_find, word_to_replace)

def format_title(sentence):
    return sentence.title()

def split_into_words(sentence):
    return sentence.split()

def word_frequency(sentence):
    words = sentence.lower().split()
    freq = {}
    for word in words:
        freq[word] = freq.get(word, 0) + 1
    return freq

def swap_case(sentence):
    return sentence.swapcase()

# Main program
sentence = input("Enter a sentence: ")

while True:
    print("\nChoose an operation:")
    print("0. Enter a new sentence")
    print("1. Reverse the sentence")
    print("2. Count vowels")
    print("3. Check if palindrome")
    print("4. Find and replace a word")
    print("5. Format (title case)")
    print("6. Split into words")
    print("7. Word frequency counter")
    print("8. Swap case")
    print("9. Exit")

    choice = input("Enter your choice: ")

    if choice == "0":
        sentence = input("Enter a new sentence: ")
    elif choice == "1":
        print("Reversed:", reverse_sentence(sentence))
    elif choice == "2":
        print("Vowel count:", count_vowels(sentence))
    elif choice == "3":
        if check_palindrome(sentence):
            print("The sentence IS a palindrome")
        else:
            print("The sentence is NOT a palindrome")
    elif choice == "4":
        sentence = find_and_replace(sentence)
        print("Updated sentence:", sentence)
    elif choice == "5":
        print("Title case:", format_title(sentence))
    elif choice == "6":
        print("Words:", split_into_words(sentence))
    elif choice == "7":
        print("Word frequency:", word_frequency(sentence))
    elif choice == "8":
        print("Swap case:", swap_case(sentence))
    elif choice == "9":
        print("Exiting program... Goodbye!")
        break
    else:
        print("Invalid choice, try again.")
