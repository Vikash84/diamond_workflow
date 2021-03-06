# DIAMOND workflow

Trivial DIAMOND nextflow workflow to perform ORF calling on a set of genomes 
and using DIAMOND-BLASTP to query ORF amino acid sequences against a user
supplied reference database

## Running

Install nextflow (requires Java 8 or later and conda on your system):

    curl -s https://get.nextflow.io | bash

Execute workflow (in this example on test data with 2 CPUs), requires a folder
containing genomes fastas (i.e. `data`) and a protein reference database fasta `reference/small_cazy.faa`

    ./nextflow run diamond.nf --input_sequences data --reference_database reference/small_cazy.faa --cpus 2

Results files will be output to `results/diamond_output/`

    results/
    └── diamond_output
        ├── GCF_000662585_orfs.out6
        └── GCF_902827215_orfs.out6

