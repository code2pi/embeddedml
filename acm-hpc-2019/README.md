

# ACM Europe Summer School on HPC for AI and dedicated applications

https://europe.acm.org/2019-acm-europe-summer-school

17 - 24 July 2019

Barcelona Supercomputer Center
Universitat Politècnica de Catalunya
Barcelona, Spain

## Origins
- 1984.  European Center for Parellism.
- 2004. Spanish National Lab for Supercomputing

BCN-CNS

- Supercomputing services to Spanish and EU researches
- RnD in computer, Life, Earth and Engineering Sciences
- Phd programme. 100 Phds
- 2019=600 employees.

Departments

- Computer Sciences
- Earth Sciences
- Life Sciences. Personalised medicine
- CASE. Engineering SW

Supercomputer

- MareNostrum1. 2004. First commodity hardware and Linux supercomputer.
- MareNostrum2, MareNostrum3.
- MareNostrum4. 11 petaflops CPU.

- Yearly summerschool on CUDA. 90+ students.
- CSRankings. UPC. Several top rankings.
Computer Architecture. 1 in Eyrope, 3 in the world since 1980.

## ACM
Oldest and largest computer science organisation.

ACM Europe.
Running summerschools.
Data Science.

ACM Europe Conference 2017.

## Past, Present, Future of Computer Architecture
Mateo Valero.

Superscalar processors.
Instructino Set Architecture.
Pipeline. Inspired by car manufacturing.
Problem: Conditionsals. Branches.
Don't know what execution path will be taken.
Branch predictors. 
Execute out-of-order.
Decode in-order. Commit in-order.
Latency hiding.
Often waiting for LOADs.

### Contributions by UPC

Memory wall

- Kilo Instructinon Processor.
- Virtual-Physical registers. Using virtual instead of physical registers for in-flight instructions.
- Distant Parallelism. Had to fight current dogma: Never add instructions (to ISA).

Power wall

- Direct Wakeup. Pointer-based instruction queue design.
- Content-aware register file.
- Fuzzy computation.
Dynamic adaptation of bitwidth in hardware.
Now known as Approximate Computing (HPC) / Reduced Precision (ML)

Symmetric Multithreading

- Dymically Controlled Resource Allocation.
- Quality of Service in SMTs
- Runahead threads for SMT

Statically scheduled VLIW architecture.
Intel Itanium project. Failed.
Needed to change the compiler.
Relevant for Embedded.

Vector Architectures. Memory latency and power.
Statement: All high performance CPUs will be vector-based. 1998.
Today (2018) this is true. Short-vectors (SIMD).
Cross-pollination between superscalar and vector processor research.

New instructions for specific use-cases.

Multi-core era.
Unable to utilize efficiently the transistors added. Moores-law.
Challenge: Programming (heterogenous) multi-core systems.
Single-execution-path.
OmpSs. Data-flow execution of sequaltial programs.
Using OMP annotations to specify dependencies.
Compiler or hardware can rewrite the execution.
OmpSs was forerunner OpenMP. OMP3.0, 4.0, 5.0 etc 
PyCOMPS : OmpSs for Python.
Talk by Jesus Labarta.

Hundreds of papers on cache. WHY?
Cause no information in hardware about the software/problem needs.

### Present
- Runtime-aware architures.
Application -> Runtime -> Hardware.
- Superscalar vision at Multicore level.

### Future
New Golden age.

- Domain-specific L and architectures.
- Open software and open hardware. Low barriers.
- Security. !! Speculation. Need to undo predictions

HW-SW codesign. Neural Networks. Pruning. Compression.
Non-volatile mermories.
NVM cheaper than RAM.

Quantum computing??? So many promises...

### Machine Learning
Applied to hardware design. To software design.
To optimize archtiectures, programs...

In Europe we are not so good at computers.
Compared to US, China, Japan.
ARM was result of EU projects.
But ARM has been sold to Softbank!
But we should have our own processors.

BSC working since 2011 on ARM for supercomputer.
Software stack making ready for when performance .

Need the Linux project for the CPU!
Open Source hardware.
RISC-V.
Exascale supercomputing initiative.
"Join us!". Hiring 30 people.
7nm initial target.

How to do it?
Dan Brown Origin written about MareNostrum.
Next one will go into Sagrada Familia.
3 euros extra ticket to visit.


## Energy Efficient Approach in ML Architectures
July 18 - July 19.
Uri Wester.

Worked at

- National Semiconductor
- Intel. 20 years.
- Technium. Israel. System Architecture.

Intel was trying to leave x86, move to RISC.
But changing ISA does not sell.
And Intel was already in the strongest market position.

## Introduction
Sailing basics, and strategy

Critical phase. Sailing upwind. Tacking. 
45 degrees against the wind for big boats.
Easy when wind is stable.
But if wind is turning, can use entire different angle.
Have to predict. If and how wind will change.
Based on past data.
Like knowledge of local environment. Typically wind turns eastwards

Same conditions. Same boats.
Boat1 leading.
Boat2 lagging.
What is Boat2 strategy. Do different than Boat1. Otherwise will continue to be behind!
Boat1 should copy the moves of Boat2. Then will maintain the lead.

Memory controller on die.
Multicore.
Northbridge integration. 
Intel had it ready. Release when AMD.

If you are behind. Don't follow. Do something different.

25th American Cup. First time non-American boat won.

## 
Existing Machine Learning problems in CPU architecture.
Branch prediction
Cache eviction.
Instruction prefetch.

## Purpose of lecture

- Understand environment and background for accelerators in CPUs.
- Exposure to NN hardware architecture.
- Initiate out-of-box-thinking re energy-efficient
- Create passion for drive next step in NN.

Need passion to continue in face of failures.

## Resources
One of best resources.

- Neural netwok Hardware tutorial. V. Sze and J. Emer
- Efficient 

## Outline
- Computing environment changes.
- Killer applications
- Trend towards accelerators. Non-von-Neuman architecture
- Opportunities in

Moores law.
Not a law. A prediction about human ability. Not much about physics! 
Every 18-36 months doubling number of transistors.
New Intel CEO in 2000. Changed the slow. From 36 month to 24 month.
Intel got stuck on 10nm.
TMSC reached 7nm.
NOW. End of Moores law.

## Performance History

Improvements due to

1. Process technology. Smaller transistors
Higher frequency. 30 Mhz. 3 Ghz. 100x improvement.
More transistors. Cache
2. Processor architecture. 30X impact

Process techn improvements are halting.
Architecture has to take over!


Stalling in number of transitors.
Stalling in frequency (since 2005).
Stalling in power. Cooling issues.
Easy gains in architecture.
Branch prediction. Superscalar. +20% each.
Today a good improvement is 1%.

Die size.
Typical. 100 mm2 - 250 mm2.
Quality assurance.
Data transportation.
1 fab. 10 billion USD.
Larger die = more fabrication.


### Dennard scaling
Power reduction at constant die size with more transistors.

Early scaling. Per generation

- 1.4x frequency gain.
- 0.75x voltage.
- 0.7x capacitance.
- 2x transitors.
=> 1.1X power.
Basically constant.
Rest 10% covered by microarchitecture improvements

Now. Last 10 years.

- 1.15x frequency
- 0.95x voltage
- 0.7x capacitance
=> power 1.45x

STOPPED.


Market expectation is
2x performance improvement year over year.
Cannot deliver this using existing mechanisms!


### Energy
Rough numbers on 45 nm.

8bit add. 0.03 pJ
32 bit add. 0.10 pJ
8bit mult. 0.2 pJ

16 bit FP add. 0.4 pJ
16 bit FP mult. 1.0 jP

8 kB cache. 10 pJ
1 M ache. 100 pJ.
DRAM. 2000 pJ. 

Energy use of computation is dominated by data access.
DRAM is very expensive.
1/1000 instructions hit DRAM => 2x the energy.
Should reduce access.

Eliminate DRAM it entirely?
Memristor motivation.


Even just with minimum.
icache, register, control, operation. 
only 1% is used for the operation!
Why still like this?
von Neumann.
General-purpose => Flexibile. But not energy efficient. 


## Amdahls Law

When you speed up something (a part of the system),
look at the whole system.
What is the overall gain.


## Performance calculation

Analytical model.
Not enough for full production.
Good for getting and testing intuition.

CPI_i. Ideal CPU.
CPI = CPI_i + overhead
overhead = sum(rj * Pj)


## Heterogenous computing

Each program is using the hardware diffently.
System design implications.

Multi-core. Immediate. Symmetric (homogenous).

Special purpose hardware. 10-1000x potential.

Gain Bandwidth Product
tradeoff gain/bandwidth.
Can use multiple amplifiers.

Idea applied to compute.

Performance/power vs application range.
Combine different application specific accelerators.

Asymmetrical multiprocessing.
Ex. 1 big core for serial, N small parallel ones.

Usually a performance versus efficiency tradeoff.

## MultiAmdahl

Different applications running serially.
How to split the resource to optimize overall runtime.
Resource=die area.
Solution. Lagrange multiplier.

Case study.
Matmul. FFT-16. FFT-1024. Black-Scholer. + 10% general purpose CPU.
As die area budget goes up, more area percentage goes to general purpose (unaccelerated, bottleneck).
As power buget reduces, part of budget used for general purpose also goes down.

## Big data characteristics

Funnel. Lots of data in. Not so much data out.
Read-once.
Simple operation.


What is the killer app?
Andy Grove.
Give me a killer apps that cannot run (satisfactory) on existing products.
For many years there was nothing for general-purpose CPUs.
Most applications ran just fine on CPU.
But now we have Machine Learning.
Lots of data in. Lots of computation. Simple outputs.
CPUs too slow.

Basic ML element. Weighted sum.
In CNN operation is only dependend on some inputs.

Energy efficiency areas in NN.

- Pruning connections.
- Quantization.
- Compact filters.
- Operation size.
- Efficient computation.


Even with specialized operations.
Data access dominates.
Want read-once!

Dedicated architectures for DNN

- Power efficiency. ops/watt
- Area efficiency. cost
- Memory supply. Bandwidth
- Model size. 
- Diversity of networks, high rate of change.

Need to efficiency, while having broad enough applications.

Hardware,software co-design.

NN output is statistical.
Can approximate.
Can predict without checking whether we were right (unlike branching in deterministic CPU).

TOPS/watt. Tera operations per second per watt.
Can be translated to PicoJoule per operation.

Spatial locality in input can be done in paper.
"Spatial correclationa and prediciton in Convolutional Neural Network" U. Weisser 

Try to map successful concepts from GP CPU into NN accelerators.

- Prediction
- Read-once
- Pipeline

Memory supply.
Putting multipliers is easy. Feeding them is hard.

Keep weight on die. Keep intermediate data on die.
CNN is pipeline-able.
Read-once or write-once strategy?

Halo. NN accelerator company.
Can use MultiAmdal approach to determine on-die memory per layer.

? weight are rarely changing.
? many inputs are easy to classify. Only need some input data, some computations

Charactesticis of audio classification 

Audio -> Time-frequency transformation.
30x30 T-F inputs for convolutions.
Few layers. 3-10.
System limits. Processing power. Microphone power. Radio power.
For 1mW scale.

Dilated conv can work well.

Special-purpose ML hardware for feasible?


## Practical session

Lagrange multipliers

### Roofline model

Used by Google for TPU.
Intel for VTune

Easy to understand visual performance mode.
Improving paralell softare and hardware
Show hardare limitations for given software
Show potential of optimizations

CPU. Computation. GFLOPS/s
Mem. Communicaton. GB/s
Cache. Locality.

FLOP/byte. Arithmetic Intensity
Can be calculated or measured.

Can see easily if we are bandwidth or compute bound.
Whether to expect gains for different strategy. 


Cache miss reasons

- Compulsory. Cache was cold
- Capacity. NOt enough space
- Conflict. 



Energy efficient Neural Networks.

## Being Human with Algoritihms
July 20.
Gerhard Schrimpf.

## Turing Leture
July 20.
Silvio Micali.

## EU programmes
July 23.
Francesca Arcara.

## Inter-disiplinary Research & Diversity
Challenges and Foundations to HPC success.
Natasa Milic-Frayling.
July 24.

## Industry session
July 24.

- Lenovo
- Fujitsu
- Intel

## Closing session
July 24.
