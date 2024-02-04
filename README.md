# iQuHack-2024 [B]Alde's Gate
Team repo for iQuHack 2024 (IBM Challenge)
### Members:
- D. Aldebaran "Alde" Jimenez-Leal
- Deron Smoot
- Kalysha Melendez Hernandez
- An Nguyen
- Dean Hu
### Link to the IBM challenge:

  - The code begins by installing the necessary libraries like `rdkit`, `metapub`, and `torch` using `pip` commands.
  - Then, it imports these libraries and initializes parameters like the keyword to be searched (`"melanoma"`), the number of articles to retrieve, and sets the `pmid` for the first 3 articles.
  - It uses the `PubMedFetcher` from the `metapub` library to obtain the articles' information like title, abstract, author, year, and journal.
  - Each article's information is stored in a dictionary and later converted to a Pandas DataFrame for ease of manipulation.


2. **Quantum Circuit Initialization:**
  - The code defines a `QuantumCircuit` class that provides an interface for quantum circuit interaction.
  - The circuit is defined with 4 qubits, using the Qiskit library.
  - It applies Hadamard gates to all qubits, a rotation gate parameterized by `theta`, and measures all qubits.


3. **Hybrid Function Definition:**
  - The `HybridFunction` class is defined as a subclass of `Function` from `torch.autograd`.
  - It serves as a bridge between classical and quantum computation.
  - In the forward pass, it executes the quantum circuit with the given inputs and computes the expectation value of the `Z` operator.
  - In the backward pass, it calculates the gradient by computing the expectation values of shifted inputs.


4. **Hybrid Module:**
  - This class extends `nn.Module` from `torch` and uses the `HybridFunction` as its forward pass to combine the classical and quantum components.
  - It takes the input and passes it through the quantum circuit to compute the expectation value.


5. **Data Preprocessing:**
  - Sample fingerprints are generated, and only the data points corresponding to labels 0 and 1 are chosen.
  - The data is split into training and testing sets, and a DataLoader is created for the training data, allowing easy batching and shuffling during training.


6. **Data Visualization:**
  - Some samples of the training data are visualized using a loop that iterates over the DataLoader.
  - It prints the images and their corresponding targets.

    Blood-based diagnostics like circulating tumor DNA (ctDNA) and circulating tumor cells (CTCs) analysis show promise for earlier cancer detection. Even localized cancers shed detectable biomarkers into the bloodstream. Thus, ctDNA and CTC analysis could enable screening and early diagnosis, rather than only indicating late-stage incurable cancer. However, sensitivity must improve while avoiding false positives that could undermine population screening. With optimization, at-risk individuals could undergo serial monitoring of ctDNA or CTCs as a less invasive alternative to screenings like mammograms or colonoscopies. Quantum computing could accelerate this optimization and analysis by allowing more rapid processing of multidimensional data. A quantum neural network modeled on cancer cell recurrence frequencies could both detect cancer and remove cancerous cells from the blood before returning it to the patient. This quantum approach analyzes more data from fewer samples than classical neural networks. By combining rapid quantum analysis of ctDNA/CTCs with quantum-enabled sorting of blood, cancer could be detected and treated earlier, improving patient outcomes. Accessing oncology data repositories like the Broad Institute could provide case studies to develop and validate these quantum computing approaches for melanoma and other cancers. 



We implemented the metpub directory to a Python analysis in the IBM computing software. which can give us access to direct information and data from the Broad Institute. We made sure to add only relevant information about melanoma cancer. This allowed us to train the deep learning algorithm on cutting-edge clinical research.

This demonstrates that quantum machine learning approaches can enable ultrasensitive and accurate analysis of ctDNA for non-invasive cancer screening. The quantum networks leveraged superposition and parallelism to recognize minute signals in sparse data. This has promising implications for clinical cancer diagnosis using liquid biopsies and warrants further research.

![alt text](https://github.com/coderalde/iQuHack-2024-B-Alde-s-Gate/blob/main/theta_graph.png)

