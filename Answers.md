<!-- Answers to the Short Answer Essay Questions go here -->
1.  Describe Middleware, Sessions (as we know them in express), bcrypt and JWT.

   * Middleware is software written to communicate between other programs, either hardware directly, or software- as in the server and the client.

   * Sessions are packets of information, also called cookies, created uniquely for the client and stored on the server in order to handle
     the user's data specifically and not conflict with other users employing the same endpoints.  

   * bcrypt is a node package that encrypts user data, such as the password on a website, by putting it through a hash function and rendering
     a very long, very hard to guess, string of characters and numbers.

   * JWT is an acronym that stands for JSON Web Token.  This token, which has three unique parts, is then stored client-side, and used to communicate
     to the server to which endpoints the user has access, as well as how long the user can stay logged in the application.  Upon logout, the client
     dissolves the token.

2.  What does bcrypt do in order to prevent attacks?

   * bcrypt not only hashes a given password, but salts the password in order to increase complexity and render rainbow tables virtually ineffective
     at retrieving the hash.   It is also impossible to reverse the hash back to its plaintext state.  Further, special functionality makes its
     iteration count very slow with options to slow it down further, making attacks very difficult to mount.

3.  What are the three parts of the JSON Web Token?

    * The Header, which consists of the type (JSON), and the hash function, which is then encoded in Base64URL.

    * The Payload, which includes all the claims regarding the user, and is also encoded in the same fashion.

    * The Signature, which includes the header, the payload, and the secret, the specifically encrypted string provided by the function in the header.
