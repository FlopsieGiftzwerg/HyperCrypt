# HyperCrypt
HYPER CRYPT
Encryption Options (File)
Encryption algorithm used: AES-256
 Encryption Key: A unique user-defined secret sequence of
characters used for encryption and decryption. The same key
is used for both encryption and decryption. To decrypt
something the same key used to encrypt it is required. It must
be known only by you and those who you want to share
encrypted files with. The encryption key inputted should be at
least 8 characters. It is recommended though, that it is long
(16+ characters) to counter brute-force attacks.
A key with a strength of at least 70% should be used.
Avoid using keys with lower strength.

Do not, in any case, use keys with a strength of less than 50%.
If for some reason you have to use a weak encryption key, use
a HCV file with a high PBKDF2 iteration count (350,000+)
and keep it hidden. Keep in mind though that a high PBKDF2
iteration count results in slower initial encryptions and
decryptions.

 Overwrite Existing File: If checked the encrypted file will
overwrite the original file, effectively deleting it.
 Use HCV File: Whether to use a Hyper Crypt Variable file for
file encryption and decryption. The same HCV file provided
for the encryption of a file is required for its decryption. Using
an HCV file significantly improves encryption security.

You can create a HCV file form the Key Generator.
Use of HCV files is recommended.

File Encryption
  
   Encrypt File: Choose a file or files to encrypt using the
  provided encryption key and HCV file (if the “Use HCV file”
  option is checked). All file types are supported even if not
  shown when using filters.
  
   Decrypt File: Choose a file or files to decrypt using the
  provided encryption key and HCV file (if the “Use HCV file”
  option is checked). All file types are supported even if not
  shown when using filters.
  
   Encrypt Folder: Encrypt a whole folder and all its contents,
  including every subfolder it contains. Uses the provided
  encryption key and HCV file. If encryption or decryption of
  multiple folders is required, either put all of them in a single
  folder and encrypt that folder with Hyper Crypt, or select them
  and drag and drop them onto the “Encrypt Folder” or “Decrypt
  Folder” button.
  
   Decrypt Folder: Decrypt a whole folder and all its contents,
  including every subfolder it contains. Uses the provided
  encryption key and HCV file.
  
  Other Tools
  
Phrase Crypt

Encryption Algorithms used: AES-256, RSA or One-Time-Pad
A text encryption and decryption tool. It uses a separate encryption
algorithm than Hyper Crypt. Note that HCV files are not used.
 Encryption Options:
 Use Symmetric Encryption: Whether to use a
symmetric encryption algorithm, in this case AES-256,
for text encryption and decryption. An encryption key
will need to be provided.
o One-Time Pad (advanced users only): OneTime Pad is the only known unbreakable
cryptographic algorithm. To use One-Time Pad
you have to input an encryption key of at least the
same length of the text you want to encrypt. The
same key produces the same encrypted result for
the same text.
Use truly random encryption keys (for instance
type characters randomly on the keyboard
without looking. Hyper Crypt has key length
indicators to help you).
Avoid using key generators.
NEVER reuse the same key for more than one
encryption, or else the security of the one-timepad will be compromised.
Note: it is not possible to know what the
correct encryption key is during One-Time
pad decryption, so make sure you have the
correct key to avoid invalid decrypted text.
