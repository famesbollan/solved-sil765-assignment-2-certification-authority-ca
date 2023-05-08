Download Link: https://assignmentchef.com/product/solved-sil765-assignment-2-certification-authority-ca
<br>
<ol>

 <li><strong><u> 0: Certification Authority (CA)</u></strong></li>

</ol>

<u>You are required to (a) build a CA, and (b) build clients that wish to confidentially send messages suitably encrypted</u> <u>with public key of receiver, but only after they know the other client’s public key in a secure manner.</u>  There are two ways for client A to know the public key of another client, B:

<ul>

 <li>Receive a “certificate” from B itself, or</li>

 <li>Get it from CA (which is rarely done).</li>

</ul>

We will presently limit the fields in the “certificate” to the following:

CERT<sub>A</sub> = ENC<sub>PR‐CA</sub> (ID<sub>A</sub>, PU<sub>A</sub>, T<sub>A</sub>, <span style="text-decoration: line-through;">DUR</span><sub>A</sub><span style="text-decoration: line-through;">, INFO<sub>CA</sub></span>) where

<ul>

 <li>PR‐CA is private key of certification authority (PU‐CA is public key of certification authority)</li>

 <li>ID<sub>A</sub> is user ID,</li>

 <li>PU<sub>A</sub> is public key of A,</li>

 <li>T<sub>A</sub> is time of issuance of certificate. To do so, you will need to:</li>

 <li>Decide you will use method (b) to obtain each other’s public key,</li>

 <li>Assume:

  <ol>

   <li>that clients already (somehow) know the public key of the certification authority,</li>

   <li>that the clients have their corresponding private keys with themselves, and</li>

   <li>that CA has the public keys of all the clients,</li>

  </ol></li>

 <li>Messages from CA to clients are encrypted using RSA algorithm and CA’s private key,</li>

 <li>Encrypted messages are sent/received between clients once they have each other client’s public key, and finally</li>

 <li>Find a way to generate and encode “current time”.</li>

</ul>

Use the above to ensure client A can send 3 messages to B, viz Hello 1, Hello 2, and Hello 3. Client B in turn responds with ACK 1, ACK 2, and ACK 3 to messages received from A.

<strong> </strong>

<strong><u>Project no. 1: Public Key Distribution Authority (PKDA)</u></strong>

<u>You are required to (a) build a </u>PKDA<u>, and (b) build clients that wish to confidentially send messages suitably</u> <u>encrypted with public key of receiver, but only after they know the other client’s public key in a secure manner.</u>

You are required to (a) build a, and (b) build clients that wish to send messages suitably encrypted with public key of receiver but of course only after they know each other’s public key in a secure manner. Specifically use the scheme described below.

To do so, you will need to:

<ul>

 <li>Assume:

  <ol start="4">

   <li>that clients already (somehow) know the public key of the distribution authority, PKDA,</li>

   <li>that the clients have their corresponding private keys with themselves, and</li>

   <li>that PKDA has the public keys of all the clients,</li>

  </ol></li>

 <li>Messages between PKDA and clients are encrypted using RSA algorithm and PKDA’s private key,</li>

 <li>Encrypted messages are sent/received between clients once they have each other client’s public key, and finally</li>

 <li>Find a way to generate and encode “current time” and “nonces”.</li>

</ul>

Use the above to ensure client A can send 3 messages to B, viz Hi 1, Hi 2, and Hi 3. Client B in turn responds with Gotit 1, Got‐it 2, etc. to messages received from A.





