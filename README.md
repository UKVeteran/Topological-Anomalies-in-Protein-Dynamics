<!-- 
  ========================================================================
  GITHUB README: TOPOLOGICAL PROBLEMS IN PROTEIN FOLDING & UNFOLDING
  ========================================================================
-->

<p align="center">
  <a href="https://github.com/your-username/your-repo-name">
    <img src="https://img.shields.io/badge/Field-Biophysics%20%7C%20Topology-blueviolet?style=for-the-badge" alt="Field: Biophysics & Topology">
  </a>
  <a href="https://github.com/your-username/your-repo-name/stargazers">
    <img src="https://img.shields.io/badge/Status-Active%20Research-success?style=for-the-badge" alt="Research Status">
  </a>
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="License">
  </a>
</p>

<h1 align="center">Topological Anomalies in Protein Dynamics</h1>

<p align="center">
  <strong>A computational and analytical framework for identifying, modeling, and resolving non-trivial topological constraints (knots, slipknots, and links) in macromolecular folding and unfolding pathways.</strong>
</p>

<hr />

<h2>🧬 Overview & Research Scope</h2>
<p>
  The traditional paradigm of protein folding assumes a smooth, funneled energy landscape where a linear chain of amino acids spontaneously transitions into a functional tertiary structure. However, a significant subset of the proteome contains <strong>topological constraints</strong>—such as deep physical knots, slipknots, links, and complex lasso configurations—that present immense kinetic barriers.
</p>
<p>
  This project offers open-source computational tools to investigate how these complex architectures manage to fold efficiently without getting hopelessly entangled, and how they behave under mechanical stress during degradation or cellular translocation.
</p>

<hr />

<!-- 
  ========================================================================
  REWRITTEN SECTION: CORE OPEN TOPOLOGICAL PROBLEMS WE AIM TO TACKLE
  ========================================================================
-->

<hr />

<h2>🧩 Core Topological Hurdles We Aim to Tackle</h2>

<p>
  Unlike mathematical knots which exist strictly in closed loops, proteins are open polypeptide chains. This project is dedicated to building the algorithmic groundwork and computational tools required to confront three massive open hurdles in structural topology:
</p>

<h3>1. Open Knot Detection & Invariant Calculations</h3>
<ul>
  <li><strong>The Hurdle:</strong> Standard topological invariants (such as Alexander or Jones polynomials) completely break down on open curves. Because the chain ends are free, they can theoretically be pulled apart without changing the intrinsic "knotting" state, making classification unstable.</li>
  <li><strong>Proposed Roadmap:</strong> We intend to implement stochastic and deterministic closure algorithms alongside <strong>Knotoid theory</strong>. Our goal is to project open chains onto a 2D plane to generate bounded topological descriptors that remain valid regardless of absolute terminus positions.</li>
</ul>

<h3>2. Kinetic Traps & Self-Entanglement Barriers</h3>
<ul>
  <li><strong>The Hurdle:</strong> In predictive folding simulations, polypeptide chains frequently collapse into messy local architectures. They form "false knots" or severe kinetic traps that artificial intelligence and standard physics models cannot resolve, artificially inflating the timescale of successful folding.</li>
  <li><strong>Proposed Roadmap:</strong> We want to develop energy-landscape smoothing mechanisms coupled with biased molecular dynamics (MD) code. This will allow us to map and trace the exact, sequential threading mechanisms (such as slipknotting versus direct end-threading) needed to bypass these traps.</li>
</ul>

<h3>3. Mechanical Resistance in Unfolding Pathways</h3>
<ul>
  <li><strong>The Hurdle:</strong> When a knotted protein is pulled mechanically—either by cell machinery like AAA+ proteases or in a lab setting via atomic force microscopy—the knot often slides down the sequence and tightens into a rigid "topological jam," entirely halting the unfolding process.</li>
  <li><strong>Proposed Roadmap:</strong> We aim to design coarse-grained simulation modules capable of measuring the exact coordinate friction of sliding knots. This toolset will help researchers pinpoint which specific structural motifs or amino acid clusters prevent catastrophic mechanical lockups.</li>
</ul>

<h2>🛠️ Methodology & Algorithmic Pipelines</h2>

<p>The codebase is split into three modular pipelines designed to plug seamlessly into standard molecular trajectories (e.g., GROMACS, Amber, or AlphaFold PDB outputs):</p>

<table width="100%">
  <thead>
    <tr>
      <th align="left">Pipeline Component</th>
      <th align="left">Mathematical/Computational Engine</th>
      <th align="left">Primary Output Indicator</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Trajectory Parser</strong></td>
      <td>AlphaCarbon skeleton smoothing & spline interpolation</td>
      <td>Normalized continuous 3D coordinate matrices</td>
    </tr>
    <tr>
      <td><strong>Knot Analysis Engine</strong></td>
      <td>Jones Polynomials via random coordinate sphere closure</td>
      <td>Knot type classification (e.g., 3<sub>1</sub> trefoil, 4<sub>1</sub> figure-eight)</td>
    </tr>
    <tr>
      <td><strong>Free Energy Profiler</strong></td>
      <td>Umbrella Sampling & Steered Molecular Dynamics (SMD)</td>
      <td>Topological rupture forces & tightening thresholds (pN)</td>
    </tr>
  </tbody>
</table>

<hr />
<!-- 
  ========================================================================
  EXPANDED SECTION: OPEN MATHEMATICAL CHALLENGES & GETTING STARTED
  ========================================================================
-->

<hr />

<h2>🎯 Open Mathematical & Computational Challenges We Seek to Solve</h2>

<p>
  This repository is not just a static toolkit; it is an active research framework targeting unresolved anomalies at the intersection of knot theory, statistical mechanics, and structural biology. We welcome contributions, pull requests, and academic collaborations on the following core initiatives:
</p>

<details open>
  <summary><b>🔍 Challenge A: The Evolutionary Conservation Paradox of Knotted Proteomes</b></summary>
  <br />
  <p>
    From an evolutionary perspective, physical knots are high-risk architectures. They impose a severe <strong>kinetic penalty</strong>, radically slowing down folding rates and dramatically increasing the probability of aggregation or degradation by cellular quality-control machinery. Yet, deep knots (such as the 3<sub>1</sub> and 5<sub>2</sub> topologies) are strictly conserved across diverse phylogenetic kingdoms in vital enzymes like SPOUT-class tRNA methyltransferases.
</p>
  <h4>Current Directives for Contributors:</h4>
  <ul>
    <li><strong>The Stability Hypothesis:</strong> Use our <code>/modules/thermo_profile</code> library to simulate thermal, chemical (urea/guanidinium), and mechanical denaturation trajectories. We aim to quantify whether these knots act as structural "pins" that restrict global conformational fluctuations, thereby protecting active sites from denaturation under extreme physiological stress.</li>
    <li><strong>The Entropic Bottleneck:</strong> Develop free-energy perturbation (FEP) scripts to isolate the exact entropic penalty ($-\Delta S^\ddagger$) associated with the threading transition state compared to unknotted structural analogs.</li>
  </ul>
</details>

<details open>
  <summary><b>🔍 Challenge B: Deep Learning Bottlenecks & Differentiable Topological Invariants</b></summary>
  <br />
  <p>
    While geometric deep learning architectures (e.g., AlphaFold 3, ESMFold) achieve remarkable global RMSD accuracy, they operate fundamentally on local spatial coordinates. Consequently, they frequently exhibit a <strong>topological blind spot</strong>: generating ground-state predictions where the backbone cleanly occupies the correct 3D volume, but the pathway leading there requires non-physical chain self-intersections or features unthreaded slipknots that break physical folding trajectories.
  </p>
  <h4>Current Directives for Contributors:</h4>
  <ul>
    <li><strong>Persistent Homology Loss Functions:</strong> We are looking for contributors to help engineer a custom, fully differentiable PyTorch/JAX loss function utilizing 0-dimensional and 1-dimensional persistence diagrams. By tracking the birth and death of topological features during model training, we can penalize structural invalidity before coordinate refinement.</li>
    <li><strong>Knotoid Distance Metrics:</strong> Implement a generalized metric to evaluate the distance between predicted and experimental open-chain topologies without relying on arbitrary, artifact-inducing endpoint closures.</li>
  </ul>
</details>

<details>
  <summary><b>🔍 Challenge C: The Topological Jamming Threshold (Mechanical Unfolding)</b></summary>
  <br />
  <p>
    When a knotted protein is processed by a directional ATP-dependent cellular protease (like ClpXP), it is pulled sequentially from one terminus through a narrow pore. This pulling action frequently causes the open knot to slide along the sequence, eventually compressing into a tight "topological jam" or macroscopic friction lock.
  </p>
  <h4>Current Directives for Contributors:</h4>
  <ul>
    <li>Help optimize our coarse-grained Master Equation models to predict the exact amino acid sequences that act as "slip-planes" versus those that trigger catastrophic mechanical arrest under simulated steering forces ($>150\text{ pN}$).</li>
  </ul>
</details>

<hr />

<h2>🚀 Getting Started</h2>

<h3>📋 Prerequisites & System Dependencies</h3>
<p>
  The underlying topology engine relies on highly optimized C++ extensions to calculate polynomial invariants (such as the Alexander-Conway and Jones polynomials) across massive molecular dynamics trajectories. Because these calculations require arbitrary-precision arithmetic to avoid floating-point overflow during matrix determinants, you must install the following native libraries before building the Python extensions:
</p>

<h4>For Ubuntu/Debian Linux:</h4>
<pre><code># Install GNU Multiple Precision Arithmetic (GMP) and Multiple Precision Floating-Point Reliable (MPFR) libraries
sudo apt-get update
sudo apt-get install -y build-essential libgmp-dev libmpfr-dev python3-dev</code></pre>

<h4>For macOS (via Homebrew):</h4>
<pre><code>brew install gmp mpfr python</code></pre>

<h3>💻 Installation & Environment Setup</h3>
<p>
  We highly recommend isolating your installation within a virtual environment (conda or venv) to prevent dependency conflicts with existing geometric or structural biology packages.
</p>

<pre><code># 1. Clone the repository and navigate to the project root
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# 2. Create and activate an isolated virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# 3. Upgrade core packaging tools
pip install --upgrade pip setuptools wheel

# 4. Install dependencies (this will automatically compile the C++ topological extensions)
pip install -r requirements.txt</code></pre>

<h3>🧪 Quick Verification Run</h3>
<p>
  To verify that the C++ mathematical extensions are properly compiled and communicating with the geometric reduction pipeline, execute our baseline topological profiling test suite:
</p>
<pre><code># Runs a calculation on a pre-packaged PDB trajectory of a knotted methyltransferase (PDB ID: 1WNZ)
python -m unittest tests/test_knot_detection.py</code></pre>

<hr />

