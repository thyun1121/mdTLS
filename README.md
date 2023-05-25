# mdTLS (Middlebox-delegated TLS)
## Research Overview
We propose mdTLS protocol to improve performance based on the middlebox-aware TLS (maTLS), one of the most secure TLS protocols. We found
out that the computational complexity of mdTLS is about twice as low as that of maTLS. 
Furthermore, we verified that our proposal meets newly defined security goals as well as those verified by maTLS.

We used Tamarin prover to evaluate security of mdTLS, we verified that the mdTLS protocol meets the security goals.

We defined nine security lemmas and one source lemma for security verification.
Six security lemmas are from maTLS and three other security lemmas are newly added to prove the security property of proxy signature, which are Verifiability, Strong-Unforgeability and Strong-Identifiability.



## Commands for verification
- Command mode
  - To prove all lemmas in theory, execute command `$ tamarin-prover --prove mdTLS.spthy`
- Interactive mode
  - For GUI mode, after executing command `$ tamarin-prover interactive mdTLS.spthy`  then, point your browser to http://localhost:3001

## Results of verifications
  ### Command mode
   ![mdTLS_tamarin_verified_command](https://github.com/thyun1121/mdTLS/assets/18222806/2483cdb3-01aa-4cb2-89e0-967197897642)
  ### Interactive mode
  - Welcome Page
  - Source Lemma
  - Security Lemmas
    - Server Authentication (SA)
    - Middlebox Authentication (MA)
    - Middlebox Authentication (MA)
    - Middlebox Authentication (MA)
    - Middlebox Authentication (MA)
    - Middlebox Authentication (MA)
    - Verifiability (V)
    - Strong-Unforgeability (SU)
    - Strong-Identifiability (SI)
- On AWS EC2 c5a.24xlarge instance (), verifying all lemmas takes 96 minutes.
