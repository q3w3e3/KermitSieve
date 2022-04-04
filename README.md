# KermitSieve
bad prime sieve in ckermit

# Performance vs other sieves on a random laptop

KermitSieve
```
->time ./PrimeSieve.ksc 13033
real    0m6.278s
user    0m2.516s
sys     0m2.766s
```

[exorcism.io bash sieve](https://github.com/glennj/exercism.io/blob/c11d3977b391592a17eeb10b0ef8af708d39fb7d/bash/sieve/sieve.sh)
```
-> time bash sieve.sh 13033
real    0m0.192s
user    0m0.156s
sys     0m0.016s
```

[these?](https://github.com/jtulach/sieve.git)
ruby:
```
->ruby ruby/sieve.rb
Ready!
Computed 97 primes in 0 ms. Last one is 509.
Computed 194 primes in 2 ms. Last one is 1181.
Computed 388 primes in 4 ms. Last one is 2677.
Computed 776 primes in 8 ms. Last one is 5897.
Computed 1552 primes in 18 ms. Last one is 13033.
```
node js:
```
node js/sieve.js
Computed 97 primes in 1 ms. Last one is 509
Computed 194 primes in 8 ms. Last one is 1181
Computed 388 primes in 9 ms. Last one is 2677
Computed 776 primes in 15 ms. Last one is 5897
Computed 1552 primes in 19 ms. Last one is 13033
```
C:
```
->./c/sieve
Computed 97 primes in 0 ms. Last one is 509
Computed 194 primes in 0 ms. Last one is 1181
Computed 388 primes in 0 ms. Last one is 2677
Computed 776 primes in 0 ms. Last one is 5897
Computed 1552 primes in 0 ms. Last one is 13033
```

this is all to say that this kermit implementation is horrendous, though the comparisons are not particularly good as i believe the kermit implementation is limited by the line out speed to the terminal when printing the results, as other sieves are printing in a block (bash) or not printing results (jtulach)
