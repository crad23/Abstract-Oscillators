# Development-of-Novel-Quantum-Algorithms
Womanium Quantum+AI 2024 Projects

**Please review the participation guidelines [here](https://github.com/womanium-quantum/Quantum-AI-2024) before starting the project.**

_**Do NOT delete/ edit the format of this read.me file.**_

_**Include all necessary information only as per the given format.**_

## Project Information:

### Team Size:
  - Maximum team size = 3
  - While individual participation is also welcome, we highly recommend team participation :

### Eligibility:
  - All nationalities, genders, and age groups are welcome to participate in the projects.
  - All team participants must be enrolled in Womanium Quantum+AI 2024.
  - Everyone is eligible to participate in this project and win Womanium grants.
  - All successful project submissions earn the Womanium Project Certificate.
  - Best participants win Womanium QSL fellowships with Classiq. Please review the eligibility criteria for QSL fellowships in the project description below.

### Project Description:
  - Click [here](https://drive.google.com/file/d/1PGNUShboB4ik_JHZGcIPTh3KYi-aajzp/view?usp=sharing) to view the project description.


## Project Submission:

In recent years, Quantum Computing has made remarkable strides, with increasingly powerful quantum computers being developed annually. Today, machines with hundreds of qubits 
can execute quantum algorithms with circuit depths reaching into the thousands, all while preserving a significant signal. However, a key challenge within the quantum computing 
ecosystem is the development of efficient and innovative quantum algorithms that are not only practical but also offer exponential advantages over classical methods.

One of the most promising areas of research in quantum algorithms is Hamiltonian simulation, particularly in simulating classical coupled harmonic oscillators. Our project aims to
bridge the gap between theory and practice by translating the theoretical framework presented in the **2023** study by R. Babbush, D. W. Berry, R. Kothari, R. D. Somma, and N. Wiebe,
*Exponential Quantum Speedup in Simulating Coupled Classical Oscillators*, published in Phys. Rev. X 13, 041041 (2023), into a practical implementation compatible with current quantum 
hardware and software capabilities.

The objective of our [Womanium Quantum+AI 2024](https://womanium.org/Quantum/AI) Final Project is to implement, optimize, and evaluate the simulation of classical coupled harmonic oscillators as detailed in the study. You can access the original paper [here](https://journals.aps.org/prx/abstract/10.1103/PhysRevX.13.041041).


### Installation and Usage

Please fork the repository and clone the fork to your local device. Certain files use other files which has helper functions. 

The project uses the following packages: classiq (0.43.3), scipy, numpy, matplotlib, tqdm, qutip (optional).

For installation run the following on codecell of jupyter notebook

`!pip install <package-name>` 

## Team Information:
Team Member 1:
 - Full Name: Kerem Yurtseven
 - Womanium Program Enrollment ID: WQ24-3PeZJI8Y4cyXsA6


Team Member 2:
 - Full Name: Cristina Radian
 - Womanium Program Enrollment ID: WQ24-dGX88XTBPxBKLvW


Team Member 3:
 - Full Name: Viraj Daniel DSouza
 - Womanium Program Enrollment ID: WQ24-OCerzcQy5eMOkUZ


## Project Solution:

### Table of Contents

1. **Implementation of toy problem** (the simplest possible cases) that covers:
- Basic theoretical details 
- Encoding of the problem. (Preprocessing)
- The key algorithmic building blocks
- The readout and post-processing.
<p align="center">
<img src="https://github.com/user-attachments/assets/0e59441e-b1e3-4f41-8410-d5be388b8bde" alt="Description" width="255">
</p>

Refer [here](https://github.com/virajd98/Abstract-Oscillators/blob/merge-private-repo/ToySuzuki.ipynb) and [here](https://github.com/virajd98/Abstract-Oscillators/blob/merge-private-repo/ToyExponentiation.ipynb) for two different simulations of 2 simplest cases (toy problems). Benchmarking using classical numerical methods has also been done. 

The implementation is fairly scalable, and it is straightforward to extend it to a more complicated scenario.

2) **Enlarging the problem for a more complicated scenario**

In this step, an actual problem from the paper has been implemented. We attempt to solve Problem 2 of estimating kinetic energy of system of Coupled Oscillators. Our codes are general, and for demonstration we simulate for $8$ masses. Please note that the simulation time on simulators is long for $N=2^3=8$. Refer [here](https://github.com/virajd98/Abstract-Oscillators/blob/merge-private-repo/KineticEnergyEstimationProblem2.ipynb) for Kinetic energy estimation for $N=8$ system. The results are benchmarked using classical numerical methods. 

A sneak peak into our simulator based results for this problem. 

<p align="center">
<img src="https://github.com/virajd98/Abstract-Oscillators-Pvt-/blob/main/Figures/Kinetic%20Energy%20Comparision.PNG" alt="Description" width="255">
</p>

We have also used advanced methods of Hamiltonian simulation through block-encoding based methods. We tried Qubitization methodology (which work very well for our toy cases) which can be found [here](https://github.com/virajd98/Abstract-Oscillators-Pvt-/blob/main/ToyQubitization.ipynb), as well as the QSVT methodology for Hamiltonian simulation that can be found [here](https://github.com/virajd98/Abstract-Oscillators-Pvt-/blob/main/QSVTapproach.ipynb). 

The execution on real hardware has been done for Qubitization based methodology for a simple case, which can be found [here](https://github.com/virajd98/Abstract-Oscillators/blob/merge-private-repo/HardwareSimulationwithQubitization.ipynb).

Resources estimation in terms of circuit depth, circuit width and number of 2-qubit gates should be made and compared across several hardwares has been done. 

3) **Optimization of the solution found in step 1 for the most adequate hardwares**


**Final Deliverables:**

● Slides that summarize the work
● **The .qmod and .qprog files for each step.** This can be found in the folder named [QMOD Files](https://github.com/virajd98/Abstract-Oscillators/tree/merge-private-repo/QMOD%20Files) and [QPROG Files](https://github.com/virajd98/Abstract-Oscillators/tree/merge-private-repo/QPROG%20Files) respectively. 
● The Python Jupyter notebooks with elaborate details for each step 



### Contributing

If you wish to contribute to this repository, please fork the repository, make your contributions in your fork, and submit a pull request


### License

This project is licensed under the MIT License - see the [LICENSE](MIT-LICENSE.txt) file for details.

### Bibliography:

1. R. Babbush, D. W. Berry, R. Kothari, R. D. Somma, and N. Wiebe, *Exponential Quantum Speedup in Simulating Coupled Classical Oscillators*, published in Phys. Rev. X 13, 041041 (2023), https://doi.org/10.1103/PhysRevX.13.041041, [link to paper](https://journals.aps.org/prx/abstract/10.1103/PhysRevX.13.041041)
2. G.H. Low, I.L. Chuang, *Hamiltonian simulation by Qubitization*, published in Quantum, 3 (2019), p. 163, 	https://doi.org/10.22331/q-2019-07-12-163, [link to paper](https://quantum-journal.org/papers/q-2019-07-12-163/)
3. András Gilyén, Yuan Su, Guang Hao Low, and Nathan Wiebe. 2019. Quantum singular value transformation and beyond: exponential improvements for quantum matrix arithmetics. In Proceedings of the 51st Annual ACM SIGACT Symposium on Theory of Computing (STOC 2019). Association for Computing Machinery, New York, NY, USA, 193–204. https://doi.org/10.1145/3313276.3316366, [link to paper](https://dl.acm.org/doi/10.1145/3313276.3316366)
4. M. Szegedy, "Quantum speed-up of Markov chain based algorithms," In 45th Annual IEEE symposium on foundations of computer science, pages 32–41, 2004, [link to paper](https://ieeexplore.ieee.org/abstract/document/1366222)
5. [Classiq Github Hamiltonian Qubitization](https://github.com/Classiq/classiq-library/tree/9c43f05f3d498c8c72be7dcb3ecdaba85d9abd6e/tutorials/hamiltonian_simulation/hamiltonian_simulation_with_block_encoding)
6.  [Classiq Github Glued Trees](https://github.com/Classiq/classiq-library/blob/9c43f05f3d498c8c72be7dcb3ecdaba85d9abd6e/algorithms/glued_trees/glued_trees.ipynb#L4)
7. [Classiq documentation](https://docs.classiq.io/latest/)


### Acknowledgments

- A heartfelt gratitude to [Womanium Team](https://womanium.org/Quantum/AI) for designing & organizing this program, and offering scholarships. 
- Special thanks to [Eden Shirman](https://www.linkedin.com/in/eden-schirman-71bb7a1b9/?originalSubdomain=il), [Tomer Goldfriend](https://www.linkedin.com/in/tomer-goldfriend-3422341b2/), and [everyone at Classiq](https://app.slack.com/client/T04KVKJKKFY/search).
- This project uses [Classiq Github](https://github.com/Classiq/classiq-library/tree/main) by [Classiq](https://www.classiq.io/).


## Project Presentation Deck:




