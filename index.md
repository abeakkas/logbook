# logbook

## 6.857 Computer and Systems Security

### Diffie Hellman Key Exchange
Let g be a generator. (a, b)'s are secret, (g<sup>a</sup>, g<sup>b</sup>) are exchanged, and g<sup>ab</sup> is the key.

### Discrete Log Assumption
Given g and g<sup>x</sup>, it is computationally hard to find x.

### CDH - Computational Diffie Hellman Assumption
Given g<sup>a</sup> and g<sup>b</sup>, compute g<sup>ab</sup>.

### DDH - Decisional Diffie Hellman Assumption Assumption
Given g<sup>a</sup>, g<sup>b</sup>, and g<sup>c</sup>, decide whether g<sup>ab</sup> = g<sup>c</sup>.

### Pedersen Commitment
Alice gives (g, h=g<sup>a</sup>) to Bob.
Bob commits to c = g<sup>x</sup>h<sup>r</sup> where x is his secret and r is random.
Alice can't figure out what x is and Bob can't change his secret.

### Zero Knowledge Proof Example
Knowing a 3-coloring of a graph, Alice commits to a coloring of random three colors.
When asked two adjacent nodes Alice reveals the colors, showing Bob that they are distinctly colored.
Then Alice recommits to another randomized coloring and repeats the process until Bob is convinced.
This way Alice does not reveal any information about her coloring.

\* Every NP statement has zero knowledge proof.

### El-Gamal Encryption
Let (SK, PK) = (x, g<sup>x</sup>) be private/public key pair.
Pick random k and send (a, b) = (g<sup>k</sup>, m*PK<sup>k</sup>) as encrypted message.
To decrypt, compute b/a<sup>x</sup> = m.

### Digital Signature Scheme from Encyption Scheme
* Sign(SK, m) = Dec(SK, m)
* Verify(PK, m, sign) = (Enc(PK, m) == sign)

## Abel-Ruffini Theorem

### Abstract Algebra Preliminary

* **Group:** A set (G) and a binary operator (+). Has four properties: clousure (a+b is in G), associativity ((a+b)+c = a+(b+c)), identity element, inverse element.
* **Cyclic Group:** There's a g in G such that g^n generates all the elements.
* **Normal Subgroup:** N such that for all n in N and for all g in G g+n+g-1 is in N.
* **Coset:** Na = {n+a for n in N} where N is a subgroup and a is an element of G.
* **Quotient Group:** G/N = {Ng for g in G}. This is also a group since (Na)(Nb) = N(a+b).
* **Solvable Group:** G is solvable if there exists a chain:
{0}=G<sub>0</sub><=...<=G<sub>k</sub>=G
where G<sub>i-1</sub> is normal in G<sub>i</sub> and G<sub>i</sub>/G<sub>i-1</sub> is cyclic.
* **Field:** to be continued..
