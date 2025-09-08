# Compute_the_list_of_publications
Compute the list of publications for a third-cycle thesis based on students publications in DiVA

# Aim
The aim is to facilite the creation of a list of publications for a third-cycle thesis. The idea is to get information about the user from the fordiva.json file, fetch the user's publications from DiVA, get information about the publications from the references.bib file in the thesis., and then compute a potential list of publications by looking for which of the entries in the references.bib file are in the user's publications. Matching is done first with strong identifieers (such as DOIs) and the fuzz matching of the titles, ... .

An example of output is:
```
\begin{ListOfPapers}
\item \label{paper:A} {Calculation of $\bar{E}_{\beta}$, $\Gamma$ and $\Delta_{i}$ for $^{99m}$Tc}\cite{Noz_1975}
\item \label{paper:B} Coherent {File} {Distribution} {Protocol}\cite{ioannidis_coherent_1991}
\item \label{paper:C} Resource {Monitoring} in a {Network} {Embedded} {Cloud}: {An} {Extension} to {OSPF}-{TE}\cite{roozbeh_resource_2013}
\item \label{paper:D} A {New} {Automated} {Way} to {Measure} {Polyethylene} {Wear} in {THA} {Using} a {High} {Resolution} {CT} {Scanner}: {Method} and {Analysis}\cite{maguire_jr_new_2014}
\item \label{paper:E} The nearest replica can be farther than you think\cite{bogdanov_nearest_2015}
\item \label{paper:F} Do {Small}-{Mass} {Neutrinos} {Participate} in {Gauge} {Transformations}?\cite{kim_small-mass_2016}
\item \label{paper:G} Make the {Most} out of {Last} {Level} {Cache} in {Intel} {Processors}\cite{farshin_make_2019}
\item \label{paper:H} PacketMill: toward per-Core {100-Gbps} networking\cite{10.1145/3445814.3446724}
\item \label{paper:I} Packet Order Matters! Improving Application Performance by Deliberately Delaying Packets\cite{Ghasemirahni_2022}
\item \label{paper:J} {FMM-Head}: Enhancing Autoencoder-based {ECG} anomaly detection with prior knowledge\cite{verardo2023fmmheadenhancingautoencoderbasedecg} (preprint)
\item \label{paper:K} A Fake Publication for testing\cite{FakePub2025}
\end{ListOfPapers}
\begin{ListOfPatents}
\item \label{patent:A} Authenticatable graphical bar codes\cite{US7107453B2}
\item \label{patent:B} Methods and devices for controlling memory handling\cite{US12111768B2}
\end{ListOfPatents}
\begin{ListOfArtifacts}
\item \label{artifact:A} {PacketMill: Toward Per-Core 100-Gbps Networking - Artifact for ASPLOS'21}\cite{10.5281/zenodo.4435970}
\end{ListOfArtifacts}
\begin{ListOfPosters}
\item \label{poster:A} MobiCom poster : wireless LAN access points as queuing systems: performance analysis and service time\cite{Khatib2003}
\end{ListOfPosters}
\begin{ListOfPatentApplications}
\item \label{patentapplication:A} Location requests by a network device\cite{patentapplication2002}
\item \label{patentapplication:B} Memory allocation in a hierarchical memory system\cite{patentapplication2019}
\end{ListOfPatentApplications}
\begin{ListOfReports}
\item \label{report:A} Dynamic PET visualization of bone remodeling using NaF-18\cite{Lee2015}
\end{ListOfReports}
%%%%%%%%%
% place holders for lists of publications _not_ included in thesis
\begin{ListOfPapers}
\end{ListOfPapers}
\begin{ListOfPatents}
\end{ListOfPatents}
\begin{ListOfArtifacts}
\end{ListOfArtifacts}
\begin{ListOfPosters}
\end{ListOfPosters}
\begin{ListOfPatentApplications}
\end{ListOfPatentApplications}
\begin{ListOfReports}
\end{ListOfReports}
\begin{ListOfDatasets}
\end{ListOfDatasets}
```

The user can now move items from the first part (before the '%%%%%%%%%') to the appropriate entires in the lower part (i.e., after the '%%%%%%%%%'. The user can add the text that they want to make a file that they can import into their thesis as the list of publicatyions.

Note that the first part is going to be the list of publications in a compilation thesis.

# sample files
references.bib a sample bib file
fordiva.json a sample fordiva.json file

## Note
Note that for the purposes of testing the user's local ID and first and last names are hardcoded in the notebook and this cell should be removed before running with your own files.

## Usage
A student should save their fordiva.json from the compilation of the thesis and save their references.bib file into this directory and then run the botebook.
