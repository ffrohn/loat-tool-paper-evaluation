<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8" >
    <title>Proving Non-Termination and Lower Runtime Bounds with LoAT</title>
    <style>
      table, th, td {border: 1px solid black;}
      td {text-align: center}
    </style>
  </head>
  <body>

    <p>
      This is the empirical evaluation of the paper <a href="https://arxiv.org/abs/2202.04546"><i>Proving Non-Termination and Lower Runtime Bounds with LoAT</i></a>.
      You can find the source code for our tool LoAT at <a href="https://github.com/aprove-developers/LoAT">GitHub</a>.
    </p>

    <p>Moreover, we refer to the <a href="https://aprove-developers.github.io/LoAT/">general LoAT website</a> for further information.</p>

    <h1>Running LoAT</h1>

    We provide a <a href="loat-static">pre-compiled binary of LoAT (Linux, 64 bit)</a>.

    <ul>
      <li>Invocation for proving non-termination: <tt>./loat-static --timeout $TO --mode non_termination $INPUT</tt></li>
      <li>Invocation for proving worst-case lower bounds on the runtime complexity: <tt>./loat-static --timeout $TO $INPUT</tt></li>
      <li>LoAT can parse three different input formats:</li>
      <ul>
        <li><a href="http://aprove.informatik.rwth-aachen.de/eval/IntegerComplexity/"><tt>.koat</tt></a><br/>

          the format from the category <i>Complexity of Integer Transition Systems</i> of the anual
          <i><a href = "http://termination-portal.org/wiki/Termination_Competition">Termination and Complexity Competition</a></i>
        </li>
        <li><a href="https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/SMTPushdownPrograms.pdf"><tt>.smt2</tt></a><br/>

          the format from the category <i>Termination of Integer Transition Systems</i> of the anual
          <i><a href = "http://termination-portal.org/wiki/Termination_Competition">Termination and Complexity Competition</a></i>
        </li>
        <li><a href="https://github.com/mmjb/T2"><tt>.t2</tt></a> (<b>experimental</b>)<br/>

          the native format of the tool T2
        </li>
      </ul>
    </ul>

    <h1>Evaluation</h1>

    <h2>StarExec Bundles</h2>

    We provide StarExec bundles for all tools used in our evaluation.

    <ul>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?id=35527">LoAT '22</a>, configuration <code>nonterm_proofout</code> or <code>cpx_proofout</code>, respectively</li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=5950ad6e-cebd-45fa-9f23-cfeb7d906648">LoAT '19</a>, configuration <code>proofout</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=93e878e6-5c5e-4a6e-b0e7-6ebd11d75376">LoAT '20</a>, configuration <code>proofout</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=788f0245-548d-4148-b840-50df112c3f8f">iRankFinder</a>, configuration <code>competition</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=89fb1947-fd52-4693-8b72-854e18f93363">KoAT</a>, configuration <code>cfr_mprf_five</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=a737357a-83c6-4d1e-b144-40e68d621037">T2</a>, configuration <code>default fixed</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=4798c8a9-e698-4029-a052-5ba641e2e0ea">VeryMax</a>, configuration <code>termcomp2019_ITS</code></li>
    </ul>

    <h2>Results</h2>

    Below we provide tables with the detailed results of our benchmarks:
    <ul>
      <li>Evaluation on the examples from the category <i>Termination of Integer Transition Systems</i> of the <i><a href="https://github.com/
TermCOMP/TPDB">Termination Problems Data Base</a></i></li>
      <ul>
        <li><a href="./loat22.html">LoAT '22</a></li>
        <li><a href="./loat19.html">LoAT '19</a></li>
        <li><a href="./t2.html">T2</a></li>
        <li><a href="./verymax.html">VeryMax</a></li>
        <li><a href="./irankfinder.html">iRankFinder</a></li>
      </ul>
      <li>Evaluation on the examples from the category <i>Complexity of Integer Transition Systems</i> of the <i><a href="https://github.com/
TermCOMP/TPDB">Termination Problems Data Base</a></i></li>
      <ul>
        <li><a href="./loat22_cpx.html">LoAT '22</a></li>
        <li><a href="./loat20_cpx.html">LoAT '20</a></li>
        <li><a href="./koat.html">KoAT</a></li>
        <li><a href="./loat22_vs_loat20.html">LoAT '22 vs LoAT '20</a></li>
        <li><a href="./loat22_vs_koat.html">LoAT '22 vs KoAT</a></li>
      </ul>
    </ul>

  </body>
</html>
