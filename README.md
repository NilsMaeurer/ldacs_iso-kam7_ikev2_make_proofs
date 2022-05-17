# The LDACS 3-pass MAKE protocol 

Formal Security Verification of the LDACS 3-pass MAKE protocol
Variations:
- LDACS IKEv2 based 3-pass MAKE protocol
- LDACS ISO/IEC 11770-3:2021 key agreement mechanism 7 based 3-pass MAKE Protocol

## Author: 

Nils Mäurer: Institute of Communication and Navigation, German Aerospace Center (DLR), Wessling, Germany

## **File structure:**
- src
  - LDACS_MAKE_IKEv2_Proof
    - ldacs_ike_3-pass_preq_a_proof.spthy - Proof for DHKE based key establishment with GS certificate stored locally at AS
	- ldacs_ike_3-pass_preq_b_proof.spthy - Proof for DHKE based key establishment GS sending its certificate alongside an OCSP response to the AS
    - ldacs_ike_3-pass_pqc_a_proof.spthy  - Proof for KEM based key establishment with GS certificate stored locally at AS
	- ldacs_ike_3-pass_pqc_b_proof.spthy  - Proof for KEM based key establishment GS sending its certificate alongside an OCSP response to the AS
  - LDACS_MAKE_ISO-KAM7_Proof
    - ldacs_iso_3-pass_preq_a_proof.spthy - Proof for DHKE based key establishment with GS certificate stored locally at AS
	- ldacs_iso_3-pass_preq_b_proof.spthy - Proof for DHKE based key establishment GS sending its certificate alongside an OCSP response to the AS
    - ldacs_iso_3-pass_pqc_a_proof.spthy - Proof for KEM based key establishment with GS certificate stored locally at AS
    - ldacs_iso_3-pass_pqc_b_proof.spthy - Proof for KEM based key establishment GS sending its certificate alongside an OCSP response to the AS
  
## The Tamarin prover repository

For installation and usage instructions of the Tamarin prover see chapter 2 of the manual:

https://tamarin-prover.github.io/manual/book/002_installation.html

## Build environment

Tamarin prover: v1.6.1

OS: Windows 10 with WSL 2.0 - Ubuntu 20.04

Configuration: Intel(R) Core(TM) i7-8850U CPU 64GB of RAM

All proofs were done with tamarin-prover version 1.6.1


## Results

### LDACS IKEv2 based 3-pass MAKE protocol

Verification time: 
  - ~2m for each "path_a" version
  - ~15m+ for each "path_b" version


- ldacs_ike_3-pass_preq_a_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_ike_3-pass_preq_a_proof.spthy

  exists_session_a (exists-trace): verified (28 steps)
  exists_two_sessions_a (exists-trace): verified (54 steps)
  mutual_authentication_A (all-traces): verified (57 steps)
  mutual_authentication_B (all-traces): verified (57 steps)
  session_uniqueness_A (all-traces): verified (30 steps)
  session_uniqueness_B (all-traces): verified (30 steps)
  secrecy_AS (all-traces): verified (207 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (20 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (77 steps)
  key_consistency_B (all-traces): verified (77 steps)

- ldacs_ike_3-pass_preq_b_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_ike_3-pass_preq_b_proof.spthy

  exists_session_a (exists-trace): verified (30 steps)
  exists_two_sessions_a (exists-trace): verified (57 steps)
  mutual_authentication_A (all-traces): verified (59 steps)
  mutual_authentication_B (all-traces): verified (59 steps)
  session_uniqueness_A (all-traces): verified (30 steps)
  session_uniqueness_B (all-traces): verified (30 steps)
  secrecy_AS (all-traces): verified (213 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (30 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (77 steps)
  key_consistency_B (all-traces): verified (77 steps)

- ldacs_ike_3-pass_pqc_a_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_ike_3-pass_pqc_a_proof.spthy

  exists_session_a (exists-trace): verified (27 steps)
  exists_two_sessions_a (exists-trace): verified (52 steps)
  mutual_authentication_A (all-traces): verified (78 steps)
  mutual_authentication_B (all-traces): verified (78 steps)
  session_uniqueness_A (all-traces): verified (28 steps)
  session_uniqueness_B (all-traces): verified (28 steps)
  secrecy_AS (all-traces): verified (200 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (21 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (74 steps)
  key_consistency_B (all-traces): verified (74 steps)
 
- ldacs_ike_3-pass_pqc_b_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:
  
  analyzed: ldacs_ike_3-pass_pqc_b_proof.spthy

  exists_session_a (exists-trace): verified (31 steps)
  exists_two_sessions_a (exists-trace): verified (59 steps)
  mutual_authentication_A (all-traces): verified (84 steps)
  mutual_authentication_B (all-traces): verified (84 steps)
  session_uniqueness_A (all-traces): verified (30 steps)
  session_uniqueness_B (all-traces): verified (30 steps)
  secrecy_AS (all-traces): verified (215 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (32 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (77 steps)
  key_consistency_B (all-traces): verified (77 steps)


### LDACS ISO/IEC 11770-3:2021 key agreement mechanism 7 based 3-pass MAKE Protocol

Verification time: 
  - ~1m for each "path_a" version
  - ~1m for each "path_b" version

- ldacs_iso_3-pass_preq_a_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_iso_3-pass_preq_a_proof.spthy

  exists_session_a (exists-trace): verified (26 steps)
  exists_two_sessions_a (exists-trace): verified (50 steps)
  mutual_authentication_A (all-traces): verified (30 steps)
  mutual_authentication_B (all-traces): verified (30 steps)
  session_uniqueness_A (all-traces): verified (28 steps)
  session_uniqueness_B (all-traces): verified (28 steps)
  secrecy_AS (all-traces): verified (56 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (19 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (74 steps)
  key_consistency_B (all-traces): verified (74 steps)


- ldacs_iso_3-pass_preq_b_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_iso_3-pass_preq_b_proof.spthy

  exists_session_b (exists-trace): verified (29 steps)
  exists_two_sessions_b (exists-trace): verified (63 steps)
  mutual_authentication_A (all-traces): verified (33 steps)
  mutual_authentication_B (all-traces): verified (33 steps)
  session_uniqueness_A (all-traces): verified (30 steps)
  session_uniqueness_B (all-traces): verified (30 steps)
  secrecy_AS (all-traces): verified (62 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS (exists-trace): verified (28 steps)
  secrecy_PFS_GS (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (77 steps)
  key_consistency_B (all-traces): verified (77 steps)


- ldacs_iso_3-pass_pqc_a_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_iso_3-pass_pqc_a_proof.spthy

  exists_session_a (exists-trace): verified (26 steps)
  exists_two_sessions_a (exists-trace): verified (50 steps)
  mutual_authentication_A (all-traces): verified (35 steps)
  mutual_authentication_B (all-traces): verified (35 steps)
  session_uniqueness_A (all-traces): verified (28 steps)
  session_uniqueness_B (all-traces): verified (28 steps)
  secrecy_AS (all-traces): verified (47 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS_1 (exists-trace): verified (19 steps)
  secrecy_PFS_GS_2 (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (74 steps)
  key_consistency_B (all-traces): verified (74 steps)


- ldacs_iso_3-pass_pqc_b_proof.spthy
  - /* All well-formedness checks were successful. */
  - summary of summaries:

  analyzed: ldacs_iso_3-pass_pqc_b_proof.spthy

  exists_session_b (exists-trace): verified (30 steps)
  exists_two_sessions_b (exists-trace): verified (58 steps)
  mutual_authentication_A (all-traces): verified (42 steps)
  mutual_authentication_B (all-traces): verified (42 steps)
  session_uniqueness_A (all-traces): verified (30 steps)
  session_uniqueness_B (all-traces): verified (30 steps)
  secrecy_AS (all-traces): verified (65 steps)
  secrecy_GS (all-traces): verified (11 steps)
  secrecy_PFS_AS (exists-trace): verified (30 steps)
  secrecy_PFS_GS (all-traces): verified (11 steps)
  key_consistency_A (all-traces): verified (77 steps)
  key_consistency_B (all-traces): verified (77 steps)