<h1>Machine Understanding</h1>

<details>
    <summary style="font-size:3vw;">What is Computation</summary>
    <p>Arithmetic uses numbers and symbols to describe calculation, so ‘1+2’ can be read as ‘one plus two’ to obtain ‘3’. Here, it is not of interest how this answer is achieved, whether the computer is you or a desk calculator.</p>
    <details>
        <summary style="font-size:2vw;">Arithemtic</summary>
            <p>There are only a limited number of symbols—plus, minus, equals, and so on—but there are infinite numbers to which they can be applied. Further, these symbols can be constructed from each other, for example, times is the repetition of plus, so ‘3✕2’ is the same as ‘2+2+2’.</p>
            <p>Peano and Dedekind show that arithmetic is based upon plus and minus. Presenting a set number of calculations in a particular order—an algorithm—allows an arbitrary calculation—computation—to be achieved.</p>
        </details>
    <details>
        <summary style="font-size:2vw;">A Functional Notation</summary>
            <p>In order to expand the number of operations available, without having to memorise more symbols and their operations, a written representation of algorithms, a functional notation, can be used. </p>
            <p>Alonzo Church developed the Lambda Calculus in the early 1930s as just such a formal representation of algorithms. This textual representation of numbers and functions show how algorithms can operate using simple substitutions. Thus, TWO TIMES THREE represents the calculation, and each of these are substituted into their Lambda representations, two numbers and a function, which can be further substituted, using the instructions in the function, until the Lambda representation of SIX is obtained. This is a manual programming language.</p>
            <p>A simple example of this calculation-by-substitution, using a modern functional notation is as follows. The calculation ‘2+3’ is written as, ‘add( 2, 3 )’, which is the name followed by a list of parameters in parenthesis. The substitution is written as, ‘add( a, b ) {a + b}’: the parameters, a and b, algebraically represent the actual parameters; the body, in braces ‘{}’, define what is to be substituted, remembering ‘+’ and ‘–’ can be used. Thus, multiplication can be constructed, recursively, from two substitutions:</p>
            <pre>
            times( a, b ) {a + times( a, b-1 )}  (1)
            times( a, 1 ) {a}                    (2)
            </pre>
            <p>
            The first (1) is a recursive function, one re-substituting itself, with two parameters, the second (2) is the terminating function which is called with one parameter and whenever the second parameter is ‘1’. The substitution, ‘⇒’, can be applied, thus:</p>
            <pre>
            times( 2, 3 ) 				
            ⇒ 2 + times( 2, 2 )         (using substitution 1)
            ⇒ 2 + 2 + times( 2, 1 )     (using substitution 1)
            ⇒ 2 + 2 + 2                 (using substitution 2)
            </pre>
            <p>This means that once defined, a function can be <b><i>reused</i></b>,
            simplifing the code which uses it.</p>
        </details>
    <details>
        <summary style="font-size:2vw;">A Universal Machine</summary>
        <p>In 1936, Alan Turing proposed a different formal definition of algorithms in which a machine can compute. His Universal Machine is so named to signify that both the data and the machine instructions are stored on an ‘endless’ tape, divided into squares each containing a letter or digit. While such use of a physical machine is not a logical proof, its demonstration, in essence, echoing Peirce’s Pragmatism of things being defined by their effects. This determinism, repeatable and dependable, is something which modern large-language algorithms can only hope to achieve.
        <p>Turing’s PhD showed that the Universal Machine could be used to represent the Lambda Calculus, and so the two are known as Turing Complete. Church was Turing’s PhD supervisor. A compiler is a program which reads a file containing functional notation—a computer program—and if it conforms to that notation is output the equivalent machine code. In other words it takes a high-level language and converts it into a low-level language. A high-level language is a meta-language, a language which describes a language, but it is equivalent to the low-level representation; if it is an abstraction, the compiler, in knowing the mapping between the high and low levels, puts back any missing detail.
        <p>Central to Turing’s idea is that his squares are organised into pairs, one holding a letter to mark its pair, which holds a 1 or 0, for writing or reading. He described this <q>convention of writing the figures only on alternate squares is very useful: I shall always make use of it.</q> [Turing, pp. 235] The beginning of this tape is a pair containing dots.
        <p>Fig. 2. Turing’s Endless Tape, starting at a double dot.
        <p>This representation, however, is one of dualism, not because it is organised in pairs but, because the pair describe two different forms: a marker square is concerned with marking a square within the tape, it is concerned with the structure of the representation, whereas the data square contains a value which is concerned with the problem domain. This dualist mechanism was taken up in the von Neumann architecture and first manifested in the Manchester Baby, the first electronically stored program computer.
        </p>
        </details>
    </details>
<hr>

<details>
    <summary style="font-size:3vw;">Dualism vs. Monism</summary>
    Some details go here...
    </details>
<hr>

<details>
    <summary style="font-size:3vw;">So, what is Machine Understanding?</summary>
    <p style="font-size:2vw;">
        Machine understanding is: <q style="font-style:italic;"><strong>the conveyance of ideas to, and their subsequent use in interacting with, a machine</strong></q>.
        </p>
    </details>
<hr>


<details>
    <summary style="font-size:3vw;">...and this is demonstrated somewhere?</summary>
    <p style="font-size:2vw;">
        The Enguage source code is available from
        <a href="https://bitbucket.org/martinwehatman/enguage">
            <samp>https://bitbucket.org/martinwehatman/enguage</samp>
            </a>.
        </p>
    </details>
<hr>


