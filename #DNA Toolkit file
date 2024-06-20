
Nucleotides = ["A", "C", "G", "T"]
DNA_ReverseComplement = {'A': 'T', 'T': 'A', 'G': 'C', 'C': 'G'}


# Check the sequence to make sure it is a DNA string
def validateSeq(dna_seq):
    tmpseq = dna_seq.upper()
    for nuc in tmpseq:
        if nuc not in Nucleotides:
            return False
     return tmpseq 
    
import random

               
randDNAStr = 'aaaatttgggccc'



DNAStr = validateSeq(randDNAStr)
def countNucFrequency(seq):
    tmpFreqDict = {"A": 0, "C": 0, "G": 0, "T": 0}
    for nuc in seq:
        tmpFreqDict[nuc] += 1
    return tmpFreqDict
result = countNucFrequency(DNAStr)

print(f'\nSequence: {DNAStr}\n')
print(f'[1] + Sequence length: {len(DNAStr)}\n')
print(f'[2] + Nucleotide Frequency: {countNucFrequency(DNAStr)}\n')

#"""DNA -> RNA Transcription. Replacing Thymine with Uracil"""
def transcription(seq):
    # DNA -> Transcription
    return seq.replace("T", "U")



print(f'[3] + DNA/RNA transcriptation: {transcription(DNAStr)}\n')



#swapping adenine with thymine and guanine with cytosine. Reversing newly generated string
def reverse_complement(seq):
    return''.join([DNA_ReverseComplement[nuc] for nuc in seq])[::-1]

print(f"[4] + DNA String + Reverse Complement:\n5' {DNAStr} 3'")
print(f"   {''.join([ '|' for c in range(len(DNAStr))])}")
print(f"3' {reverse_complement(DNAStr)} 5'\n")


def gc_content(seq):
    return round((seq.count('C') + seq.count('G')) / len(seq) * 100)


print(f'[5] + GC Content: {gc_content(DNAStr)}%\n')


def gc_content_subsec(seq, k=20):
    res = []
    for i in range(0, len(seq) - k + 1, k):
        subseq = seq[i:i + k]
        res.append(gc_content(subseq))
    return res

print(
    f'[6] + GC Content in Subsection k=5: {gc_content_subsec(DNAStr, k=5)}\n')