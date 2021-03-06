# Biological Concepts

## Alleles
Alternative forms of a particular sequence. 

## Single nucleotide polymorphism (SNP)

A variation in a single nucleotide that occurs at a specific position in the
genome. For example, at a specific base position, there could be two possible
nucleotide variations, C or A. These are called alleles for this base
position. 

## Genotype

The pair of alleles carried by an individual. If there are n alternative
alleles, there will be n(n+1)/2 possible genotypes. In most cases, there are
3 possible genotypes. Individual 1 could have A (in one chromsome) and A
(in the other chromosome), Individual 2: A and C, Individual 3: CC.

## MAF

Each allele has a frequency, which is the proportion of chromosomes of that
type in the population. Note that here the term frequency is used to refer
to a population proportion. The minor allele frequency (MAF) refers to the
frequency of the less common allele at a variable site. 

## Homozygotes

The two alleles are in the same state (e.g. CC, GG, AA)

## Heterozygotes

The two alleles are different (e.g. CG, AC)


## Example 1

Consider the simple example of a SNP for which AA is present in 75% of the
population, AC is present in 20% and CC is present in 5%. The frequency of
the A allele is then equal to (75+75+20)/2 = 85%, while the frequency of C is
(20+5+5)/2 = 15%. In this case, the minor allele (C) frequency is equal to 15%.

## Example 2
The frequency of A equals the following: 
2 x (number of AA) + (number of AC) divided by 2 x (total number of
individuals). 

AA 0
AA 0
CC 2
AC 1

Thus for A: 2 x (2) + (1) divided by 2 * (4). This is 0.625. Since the
frequency of the other allele is simply 1 - f, then frequency of C is
1 - 0.625 or 0.375.

## Linkage disequilibrium (LD)

Linkage disequilibrium (LD), indicates non-random association of alleles at
two or more loci, not necessarily on the same chromosome. It refers to the
phenomenon that SNP allele or DNA sequence which are close together in the
genome tend to be inherited together. LD is affected by two parameters:

1) The distance between the SNPs [the larger the distance the lower the LD].

2) Recombination rate [the lower the recombination rate the higher the LD].

Variations in the DNA sequences of humans can affect how humans develop
diseases. Association studies determine whether a particular allele in the
population is associated with a disease or trait.

A tag SNP is a representative SNP in a region of the genome with high linkage
disequilibrium (the non-random association of alleles at two or more loci). 


# Statistical Concepts

## Linear model

A linear model is a model in which the response variable is a linear function
of the dependent variable. In genetics, the response variable is the trait
and the dependent variable is the SNP.

## Effect size

Effect size measures the strength of influence of a variable on the out come.
In genetics, the variable is the SNP, and the outcome is the trait.

## Estimated effect size

In reality, one doesn't know the true effect size under the model, but can
obtain an estimation of the effect by fitting the model on the data (e.g.
through linear regression).

## Standard error

Standard error is the uncertainty one has about an estimate. The larger
the standard error, the less certain one is about an estimate. Standard
error usually decreases with the number of samples.

## Z-score

Z-score is a measure of the strength of assiciation.
Z-score is calculated as (estimated effect size) / (standard error of the
effect size). (Note that the standard error here can be interpreted as
standard deviation.) If the null hypothesis is that the true effect size
is 0, then Z-score tells you how many standard deivation the estimated effect
is away from 0. Thus, the higher the Z-score (the more far away the estimated
effect is from the null) the stronger the association signal.

## Hypothesis testing

In hypothesis testing, we are interested in finding out whether a statistical
model is supported by the data or not. Usually, we have a null hypothesis
(denoted by H0), and we want to test whether the data support the null
hypothesis or not. If the data does not support the null hypothesis, then
we reject the null hypothesis, and is in favor of the alternative hypothesis
(denoted by H1).

For GWAS, H0 is the hypothesis that the SNP is not causal for the trait, or
the SNP has no effect on the trait.

## Correcting for multiple hypothesis tests

Statistical hypothesis testing is based on rejecting the null hypothesis if the likelihood of the observed data under the null hypotheses is low.  We usually test each hypothesis separately, using some level of significance α. If multiple hypotheses are tested, the probability of getting a significant result simply due to chance increases,  even if all of the tests are actually not significant. 
Most common is Bonferroni corretcion. If a significance threshold of α is used (usually 0.05), and n separate tests are performed, then the Bonferroni adjustment considers a score significant only if the corresponding P-value is ≤α/n.
The cut-off of 5x10^-8 is normally chosen as a threshold to reach genome-wide significance because it is a Bonferroni correction for multiple testing where the number of tests (associations with SNPs tested across the genome) is on the order of 10^6  (0.05/10^6 = 5×10^−8). If observed P-value is less than this value, a SNP is considered significant after correction.

## QQ plot
In genomics, a QQ plot shows the expected distribution of association test statistics (X-axis) across the many SNPs compared to the observed values (Y-axis), in other words, the negative logarithm of the observed (y axis) and the expected (x axis) p-values are plotted for each SNP (dot), and compared to the normal distribution. A clean QQ plot should show a solid line matching X=Y until it sharply curves at the end (representing the small number of true associations among thousands of unassociated SNPs). Other deviations from the X=Y line imply a consistent difference across the genome (suggesting a systematic bias from unrecognized population structure, analytical approach, genotyping artifacts, etc.)

## Standardization

For us, standardization means center and scale the data such that after the
transformation, the mean of the data is 0 and variance is 1.

## Heritability

Heritability is the amount of variance in a trait that is accounted for by
genetic variations. More precicsely, if we assume
Trait = Genetics + Environment, then heritability is
Var(Genetics) / Var(Trait). Heritability is always a value between 0 and 1.

## Genetic covariance

Genetic covariance is the covariance between two traits that is due to
genetic variations. If we assume

1. Trait1 = Genetics1 + Environment1
2. Trait2 = Genetics2 + Environment2

then the genetic covariance between the two traits is
Cov(Genetics1, Genetics2).

## Estimator

In statistics, an estimator is a method to quantify a parameter of a data.
For example, taking a sum of a list of numbers and dividing the sum by the
size of the list is a way to estimate the mean of the data.

## Bias

The same estimator may yield different results on different samples of data.
We say the estimator is biased if the mean of the estimated parameter after
we apply the estimator on different samples of data is not equal to the true
parameter. And bias is the difference between the mean and the true parameter.

## Unbiased estimator

An unbiased estimator is an estimator that estimates the true parameter in
expectation. That is, after we apply the estimator on different samples of
data, and take the mean of the estimated parameter, we get the true parameter
back.

## Simulation

To see how well an estimator works, we usually apply it on simulated data
first, where we can control the parameter. An estimator is good if it gives
back the parameter we use in the simulation.

## Eigenvalue and Eigenvectors

Eigenvectors and eigenvalues have many important applications for dimensionality reduction (such as Principal Component Analysis). There are a lot of problems that can be modeled with linear transformations.

Eigenvectors are the "axes" (directions) along which a linear transformation acts simply by "stretching/compressing" and/or "flipping"; eigenvalues give you the factors by which this compression occurs. They are multipliers, i.e. numbers that represent how much stretching has taken place or how much something has been scaled up by.

The more directions you have along which you understand the behavior of a linear transformation, the easier it is to understand the linear transformation; so you want to have as many linearly independent eigenvectors as possible associated to a single linear transformation.

An eigenvalue is a number that is derived from a square matrix. Usually represented by λ. 
Let A be a square matrix (a collections of n rows of n numbers which means that there are n x n numbers in total). 
Let x be a nonzero vector. 

We say that a number is the eigenvalue for this square matrix if and only if there exists a nonzero vector x such that Ax = λx where:

A is the square matrix
x is the nonzero vector
λ is a nonzero value.
In this circumstance, λ is the eigenvalue and x is the eigenvector.

## Value decomposition of LD

A = UΣV*

Columns of U and V are, respectively, left- and right-singular vectors for the corresponding singular values. 

The columns of V (right-singular vectors) are eigenvectors of M^tM.

The columns of U (left-singular vectors) are eigenvectors of MM^t.

The non-zero elements of Σ (non-zero singular values) are the square roots of the non-zero eigenvalues of M^tM or MM^t.

We will use the R library "svd" to obtain the singular values (diagonal entries Σ) and the left singular vectors (U). 

# Suggested books

Applied Statistical Genetics with R: For Population-based Association Studies
By Andrea S. Foulkes
