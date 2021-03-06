Encryption Options
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
	
__________________________________________________________________________

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
	
__________________________________________________________________________

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
		
		 Use Asymmetric Encryption: Whether to use an
		asymmetric encryption algorithm, in this case RSA, for
		ext encryption and decryption. A public key file
		(.pubk), for encryption, will need to be specified, and
		also a private key file (.prvk) for decryption. The public
		key file can be shared with anyone so they can use it to
		encrypt data, as it can’t be used for decryption, but this
		data can only be decrypted by the corresponding
		
	Important Note
	Asymmetric encryption can only encrypt data smaller than the
	specified key size in bytes.
	
Tip
	You should use Asymmetric encryption to transmit symmetric
	(AES) keys over the internet without the fear of them being
	hijacked and stolen. For example if you want to send a key to
	a friend you should first create an asymmetric key pair from
	the key generator, and send the public key (.pubk) to your
	friend. Your friend should also generate a key pair and send
	his public key to you. Then encrypt the symmetric key with
	your friend’s public key and send it over to him. Your friend
	should then be able to decrypt it with his private key (.prvk).
	
	Example: Eliza has encrypted a file she wants to send to
	Maria. Eliza has not told Maria the encryption key previously,
	so she wants to send it as well. Eliza knows that sending the
	encryption key unprotected is wrong, as it could get hijacked
	by an attacker. So she decides to use asymmetric encryption
	to protect the encryption key. She asks Maria to create an
	asymmetric key pair and send her the public key (.pubk file).
	Maria generates it and sends it. Eliza then uses Maria’s public
	key to encrypt the encryption key and then sends it over to 
	
	her. Maria then decrypts it using her private key (.prvk file).
	She is then able to decrypt the encrypted file Eliza sent her.
	The public key is useless to an attacker as it only contains info
	used to encrypt data, but not to decrypt it.
__________________________________________________________________________

Key Generator
	A key/password generation tool.
	
		 Symmetric:
			 Key length: The length of the key to generate,
			
		 Asymmetric:
			 Key size: The RSA key size to generate (from 2048 bits
			to 16384 bits). The recommended size is 2048+ bits.
			
		 HCV:
			 Additional key length: The length of the additional
			key (will be concatenated to the inputted key when
			performing operations, increasing security) to generate.
			 PBKDF2 iterations: The number of PBKDF2 iterations
			to perform. The higher this, the slower encryption and
			decryption operations are, but the more secure.
			 The recommended iterations when using a strong
			encryption key are 64000+
			
Hyper Hash
Hyper Hash is a powerful hashing tool that allows hashing of text
and files using a range of popular hashing algorithms.

	 Computed hash: The generated hash based on the text or file
	entered using the selected hashing algorithm.
	
	 Reference hash: The hash to compare the computed hash
	with, to see whether they match or not.
	
	 Reference file: The file to compare with the selected file to
	see whether they are the same or not
__________________________________________________________________________

Algorithms

SHA-1			_:_	Used for data integrity such as
					text and files.
					Not secure. (only use for
					public hashes)
			
SHA-256
SHA-384
SHA-512			_:_	Used for data integrity such as
					text and files.
					Good for general data integrity
					validation. SHA-512 offers the
					most security.
			
HMAC-SHA-256
HMAC-SHA-384
HMAC-SHA-512	_:_	Used for secure data integrity
					such as text and files.
					-Requires an encryption key.
					-Can be used for integrity
					validation of encrypted files.
					Secure. HMAC-SHA-512 offers
					the most security.

HMAC vs Standard hashing
HMAC with the use of an encryption key, ensures a unique
generated hash, that only the holder of the key can create.


Common errors

	1) Encryption key could not be verified.
		You may get this reason for two reasons:
		Either you have entered the wrong decryption key
		or the key hash in the file been modified.
		If you are absolutely sure you have entered the correct
		decryption key and you still get this error, then there is
		nothing you can do to decrypt it.
		
	2) File authenticity could not be verified
		If you get this error, then the encrypted file has been modified
		or has been corrupted. 