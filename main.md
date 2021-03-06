% Two models of the evolution of (non-)Universal Grammar
% COGS 269 April 5, 2017
% Matthew Turner


# Introduction

## Outline

1. Some words on the debate
2. Nowak, Komoarova, & Niyogi (2001)
3. Thompson, Kirby, & Smith (2016)

## Language: A product of evolution, culture, or both?

Debate on whether language is 

1. innate, specially-evolved language faculty, or

2. a tool that has been developed and maintained through culture, just like
pizza or a bow and arrow\footnote{\tiny Everett, D. L. (2012). Language: The cultural tool. New York: Random House.}

## But what is language, exactly?

\includegraphics[width=\textwidth]{figures/chimp.png}

## But what is language, exactly?

\includegraphics[width=0.6\textwidth]{figures/imitation.png}

\footnotesize{Hauser, M. D., Chomsky, N., \& Fitch, W. T. S. (2002). The faculty of language: what is it, who has it, and how did it evolve? Science, 298(5598), 1569–79.}

## But what is language, exactly?

\includegraphics[width=\textwidth]{figures/animals-gaze.png}

\footnotesize{Fitch, W. T., Huber, L., \& Bugnyar, T. (2010). 
Social Cognition and the Evolution of Language: Constructing Cognitive Phylogenies. Neuron, 65(6), 795–814.}

# Motivation

## Violence metaphors in cable news election coverage

![Violent words used in figurative violence constructions over time. 
Debates seem to increase usage](figures/fig_uses_violent_words-FIG1.pdf)

## Word meaning in culture (and changes over time)

![Difference in semantics between Fox News and MSNBC](figures/liberal.pdf)

## Word meaning in culture (and changes over time)

![Difference in semantics between Fox News and MSNBC](figures/islam.pdf)


# Nowak, Komarova, & Niyogi (2001)

## Key results

* There is a threshold for learning fidelity, $q$, that results in a
"coherence threshold" for Universal Grammar
* Rule-based generative grammar is more advantageous than list-based only
under certain conditions
    * **Rule-based:** Grammar as we would define it; infinitely recursive;
    _the man who was very very very (very very very...) old_  is still
    grammatically correct
    * **List-based:** Every type of grammatical construction is memorized
* As seen in humans, the model reveals learners have a limited language
acquisition period
* In the case of competing "universal grammars", the universal grammar with
a smaller "search space" is preferred

## Key concepts & facts

Foundational differential equation of the paper:

\begin{equation}
    \dot{x}_i = \sum_{j=1}^n x_j f_j Q_{ji} - \phi x_i \quad i=1, \ldots, n
    \label{eq:nowak-main}
\end{equation}

All results derive from the equilibrium solution, which means

\begin{equation}
    \dot{x}_i = \frac{dx_i}{dt} = 0 \quad \forall i   
\end{equation}


## Key concepts & facts

Foundational differential equation of the paper:

$$
    \dot{x}_i = \sum_{j=1}^n x_j f_j Q_{ji} - \phi x_i \quad i=1, \ldots, n
$$

* $f_i = \sum_j x_j F(G_i, G_j)$ (fitness of speakers of $G_i$)
* $F(G_i, G_j) = \frac{1}{2}(a_{ij} + a_{ji})$, where $a_{ij}$ is the "distance"
or "probability that a speaker who uses grammar $G_i$ formulates a sentence
that a speaker of $G_j$ will understand
* $Q_{ji}$ is the probability that a speaker of $G_j$ will transition to
speaking $G_i$

## Key concepts & facts

Other pieces of model framework that are considered:

* Two types of solutions to Equation \ref{eq:nowak-main}:
    * Symmetric: all frequencies of grammar users, $x_i = x_j \quad \forall i,j$
    * Asymmetric: e.g. $x_i = X$ and $x_j = X/(n-1)$ or unspecified mixture

* Two types of learners:
    * memoryless learners, corresponding to rule-based learners; Bayesian (in spirit)
    * batch learners, correspond to list-based learners; memorize all $n$ rules
      of a Universal Grammar


## Preliminary solutions
$$
    \dot{x}_i = \sum_{j=1}^n x_j f_j Q_{ji} - \phi x_i \quad i=1, \ldots, n
$$

* In the case where learning is perfect within each grammar, 
i.e. $Q_{ii} = 1$, there are $n$ asymmetric solutions: $x_i = 1$ and
$x_j = 0 \quad \forall i \neq j$.

* With high error rates in learning, there is only a stable symmetric solution,
where approximately $x_i \approx 1/n$. In this case $Q_{ii} \approx 0$ and
$Q_{ji} \approx 1/(n-1)$

## Coherence conditions

At this point, Nowak, Komoarova, & Niyogi (2001) ask, "what is the minimum
value of $Q_{ii} = q$ such that one grammar dominates?" They assume
$Q_{ji} = (1 - q)/(n - 1) \quad i \neq j$. 

More technically, the question is, "for what values of $q$ is the
do the symmetric and asymmetric solution exist and is stable?"

The asymmetric solution is now given as $x_i = X$ and $X_{j \neq i} = (1-X)/(n-1)$

## Coherence conditions

\includegraphics[width=\textwidth]{figures/nowak-fig-1.png}

## Now with learners

To this point, the mechanism for learning has not been considered.

Recall two learner types:

1. Memoryless learner
2. Batch learner

## Now with learners: Memoryless learner

* Starts by guessing it is learning grammar $G_r$ ($r$ as in _random_). 
* If learner can understand teacher's utterance, it keeps $G_r$. Otherwise, 
switch to another grammar at random.

Results in 

$$
q(b) = 1 - \left(1 - \frac{1-a}{n}\right)^b
$$

## Now with learners: Batch learner

* Given $b$ example sentences then chooses the most consistent grammar

Results in

$$
q(b) = \frac{1 - (1 - a^b)^n}{na^b}
$$

## Average coherence vs. learning period (uniform random $a_{ij}$)

\includegraphics[width=\textwidth]{figures/nowak-fig-2.png}

## Comparing two universal grammars

Nowak, et al., derive dynamics equations\footnote{see (34) in references} 
for two competing universal grammars in order determine conditions for 
one to be an evolutionarily stable strategy (ESS).

## Evolutionarily Stable Solution (memoryless learner)

\includegraphics[width=\textwidth]{figures/nowak-fig-3.png}

## Coherence thresholds as a function of learning period, $b$

With $q > q_1$

* Batch learner:

\begin{equation}
  b > C_1 n
\end{equation}

* Memoryless learner:

\begin{equation}
  b > C_2 \log{n}
\end{equation}

$n$ is the number of candidate grammars, $G_i$


## When rule-based grammars are evolutionarily stable

Combining the results from before Nowak, et al., obtain the condition for
rule-based grammars to yield greater fitness

$$
N > \frac{\log{n}}{\log{1/a}}
$$

# Thompson, Kirby, and Smith (2016)

## Key concepts & facts

Only two choices of grammar (to match Nowak, et al.), 
or "languages" as they say: $T_0$ and $T_1$. The dynamics of the population
in this model is given recursively

\begin{equation}
g_j^{t+1} = \frac{1}{\phi} \sum_{j=0}^n g_j^t f_j m_{ij}
\end{equation}

* $g_j^t$ is proportion of speakers with prior $\alpha_j \in [0, 1]$, but
now with an explicit time dependence 
* $f_j$ is still the fitness, though with a different definition (Equation [2]
  in the paper)
* $m_{ij}$ is like $Q_{ji}$: it is the probability that a learner with 
$T_j$ at time $t$ will speak $T_i$ at time $t+1$
* $\phi = \sum_{i=0}^n g_i f_i$, still the average fitness of the population

## Key concepts & facts

$$
g_j^{t+1} = \frac{1}{\phi} \sum_{j=0}^n g_j^t f_j m_{ij}
$$

$$
f_i = a_ic + (1 - a_i)(1 - c)
$$

* $c$ is the proportion of the population speaking $T_1$.

* $a_i$ is the probability a learner with prior, $\alpha_i$

## Key results

* Linguistic universals emerge in learning cultures without strong biological
adaptation for such universals
    * But only for a specific type of learning
* Can be generalized for any "behavioral universal"
* Genetic variation contributes to universals, but weakly, 
to a significantly lesser degree than cultural "evolution"


## Transition probability $m_{ij}$

"$m_{ij}$ is the probability that the offspring of a learner with prior 
$\alpha_j$ will, through mutation..., inherit $\alpha_i$.

* "each of the learner's $n$ genes may mutate with independent probability,
  $\mu$ into a gene of the opposite type...there are $n \choose i$ possible
  genomes with $i$ genes favoring $T_1$"

**Proof:** ...magic... yields Equation [7] in the paper

\begin{equation}
m_{ij} = \sum_{k=0}^{n-i}{n-i \choose j - i + k}{i \choose k} \mu^{j - i + 2k}(1 - \mu)^{n-j-i+2k}
\end{equation}

## Key concepts & facts, continued

* Like Nowak, et al., two types of learners
    * Maximum _a posteriori_ (MAP) learners: select hypothesis with maximum
      prior
    * Sampling learners: either $T_0$ or $T_1$ could be selected with 
    probability equal to the prior

* Two different models
    1. A "distinct linguistic feature" evolves through bioloigical and/or
       cultural evolution
    2. A binomial distribution of syntactic orderings $S \rightarrow X Y$
       or $S \rightarrow Y X$

In the first model, the inference agents must make is discrete: "choose"
between linguistic "feature" $T_0$ or $T_1$. The second model has agents
infer $p = Pr(S \rightarrow XY | \mathcal{L})$, where $L$ is a grammar that
allows for either the ordering $S \rightarrow XY$ in $p$ of all constructions
and $S \rightarrow Y X$ in $(1 - p)$ of all constructions.


## Discrete feature learning ($n \rightarrow \infty$)
\begin{figure}
\includegraphics[width=\textwidth]{figures/thompson-fig-1-ninf.png}
\caption{
(Upper) Solid line is $\alpha$ over time, the dotted line is $c$ (fraction of speakers
speaking $T_1$). (Lower) $\alpha$ is the probability distribution of priors, $\alpha_i$. 
}
\label{fig:thompson-1-ninf}
\end{figure}

## Discrete feature learning ($n=100$ agent-based model)

\begin{figure}
\includegraphics[width=0.7\textwidth]{figures/thompson-fig-1-abm.png}
\caption{
Acultural populations are green, MAP populations are blue, and sample learners
are red.  The results are plotted at the end of 300 trials with 1000
generations.
}
\label{fig:thompson-1-abm}
\end{figure}


##  ($n \rightarrow \infty$)

\begin{figure}
\includegraphics[width=\textwidth]{figures/thompson-fig-2-ninf.png}
\caption{
(Upper) Solid line is $\alpha$ over time, the dotted line is $c$ (fraction of speakers
speaking $T_1$). (Lower) $\alpha$ is the probability distribution of priors, $\alpha_i$. 
}
\label{fig:thompson-2-inf}
\end{figure}

## Model 2 of 2 ($n=300 agent-based model)

\begin{figure}
\includegraphics[width=0.7\textwidth]{figures/thompson-fig-2-abm.png}
\caption{
Acultural populations are green, MAP populations are blue, and sample learners
are red.  The results are plotted at the end of 300 trials with 1000
generations.
}
\label{fig:thompson-2-abm}
\end{figure}

# Assumptions

## Assumptions

1. Discrete, unchanging, finite language types
2. "Learning" algorithms are highly abstract
