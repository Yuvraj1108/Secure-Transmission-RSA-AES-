# Secure-Transmission-using-RSA-AES (Encryption & Decryption Algorithms)

#### Under the guidance of Prof. Milind Sohoni

## Abstract

Data is increasingly central to our personal lives, economic prosperity, and security.
That data must be kept secure. Just as we lock our homes, restrict access to critical
infrastructure, and protect our valuable business property in the physical world, we
rely on encryption to keep cybercriminals from our data. Proposals to regulate this
crucial form of protection — however well-intended — could weaken our security.
Digital security is becoming increasingly important to protect us as we bank, as we
shop, and as we communicate. Our digital world is constantly under attack by
cybercriminals and at the core of that security lies encryption. It is a secure envelope
that keeps hackers from reading our personal communications.
In this project, we will begin with understanding the basics of encryption and
decryption. Followed by learning RSA and AES algorithms. Then we will use these
algorithms and model a real life situation of secure data transmission between army
personnel.

## INTRODUCTION

Encryption can be understood using the following example :
Alice wants to send a private message to Bob, and the only easy way they have to
communicate is via postal mail.
Unfortunately, Alice is pretty sure that the postman is reading the mail she sends.
That makes Alice sad, so she decides to find a way to send messages to Bob without
anyone else being able to read them.
So, she wants us to develop a way of encrypting the letter; of hiding its true meaning
so the postman can't read it, but Bob can.
So before devising an algorithm to help Alice, let's look into the basics of Encryption and Decryption.

## Encryption and Decryption

**Encryption** ​ is a process that encodes a message or file so that it can only be read by
certain people. Encryption uses an algorithm to scramble, or encrypt, data and then
uses a key for the receiving party to unscramble, or decrypt, the information. The
message contained in an encrypted message is referred to as plaintext. In its
encrypted, unreadable form it is referred to as ciphertext.

**Decryption** ​ is a way to change encrypted information back into plaintext. This is the
decrypted form.

**Key** ​: Random string of bits created specifically for scrambling and unscrambling data.
These are used to encrypt and/or decrypt data. Each key is unique and created via
algorithm to make sure it is unpredictable. Longer keys are harder to crack. Common
key lengths are 128 bits for symmetric key algorithms and 2048 bits for public-key
algorithms.

## Problem Statement:

We are trying to model a typical situation in PoK.

The Army outposts regularly want to communicate and exchange sensitive
information, but the data is at risk since it can be intercepted by the adversary.

Data breach is common and while delivering the data, the adversary might steal our
data, interpret it and may use it against us. So we plan to generate a way to secure the
communication among the army outposts.

## Our solution:

We propose a way through which the army personnel first uses asymmetric
encryption (RSA) to request and receive a key for further secure communication. And
then the army personnel can record an audio message, convert it to hexadecimal and
encrypt this data, use symmetric encryption (AES) and deliver it to his allies.

In layman terms, we, using the above method will try to develop a secure and fast
way of communication among the army outposts which can’t be intercepted by the
adversary.

**Understanding the solution in detail:**

The sensitive information at the border needs to get delivered as quickly as
possible to the concerned authorities, which will give them time to plan,
prepare and act according to the situation.

So, we are working on audio transmission. As the army javaan could record
audio messages at ease and deliver them quickly.

After recording the audio, the software will convert the audio into
hexadecimal format.

Then the software will contact the concerned department for setting up
encryption and will use the RSA algorithm to interchange private AES key for
further communication.

Once, the AES key gets delivered, secure communication can take place. Now
the hexadecimal encrypted file gets transferred from one end to another.

Decryption and reconversion of the file then takes place at the other end.

Now, the audio message is ready to be heard on the other side.

**For more details please go through the [report](report.pdf).**

## Instructions:

1. Clone the repository. 

2. Install Pycryptodome package for python using:

	`pip install pycryptodome`

3. Change the input.mp4 file present in the Input folder, to your desired file mp4 and rename it as input.mp4.

    (For the demo, we have kept a song file in the Input folder)

4. Open the terminal in the code directory and input the following command .
	
    `python3 secure.py`

5. You will find the decrypted output file in the Output folder.

## REFERENCES

1. How does RSA work? - HackerNoon.com
2. Cryptography with Alice and Bob
3. What is AES encryption (with examples) and how does it work?
4. Algorithms book by Dasgupta, Papadimitriou and Vazirani
