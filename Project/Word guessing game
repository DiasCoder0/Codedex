import random

# Kata yang akan ditebak
word_bank = ['jakarta', 'Jakarta']
word = random.choice(word_bank)

# Simpan huruf yang sudah ditebak
guessed_letters = ['Jakarta', 'jakarta']
attempts = 10

print("🎮 Game Tebak Kata:")
 # Tampilkan progres kata (contoh: j _ _ _ _ _ _ )
while attempts > 0:
   
    display_word = ""
    for letter in word:
        if letter in guessed_letters:
            display_word += letter + " "
        else:
            display_word += "_ "

    print("\nKata: " + display_word.strip())

    # Cek apakah sudah berhasil menebak semua huruf
    if all(letter in guessed_letters for letter in word):
        print("🎉 Selamat! Kamu berhasil menebak kata:", word)
        break

    # Input tebakan
    guess = input("Tebak Ibukota Indonesia: ").lower()

    if guess in guessed_letters:
        print("⚠️ Kamu sudah menebak huruf itu.")
    elif guess in word:
        print("✅ Benar!")
        guessed_letters.append(guess)
    else:
        attempts -= 1
        print("❌ Salah! Kesempatan tersisa:", attempts)
        guessed_letters.append(guess)

if attempts == 0:
    print("\n😢 Kamu kehabisan kesempatan. Jawabannya adalah:", word)
