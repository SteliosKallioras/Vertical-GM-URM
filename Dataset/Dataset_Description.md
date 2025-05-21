# Vertical-GM-URM: Vertical Ground Motion Effects on URM Structures

## Dataset Description

This folder contains processed numerical data from the nonlinear time-history analyses (NLTHA) of the case-study unreinforced masonry (URM) building, subjected to:
- horizontal ground motion components only, and  
- combined horizontal and vertical components.

Eight data files are provided in `.mat` format, each corresponding to one of the analysis sets defined in Table 2 of the paper:

- `Set-A-1.mat`  
- `Set-A-2.mat`  
- `Set-B-1.mat`  
- `Set-B-2.mat`  
- `Set-C-1.mat`  
- `Set-C-2.mat`  
- `Set-C-3.mat`  
- `Set-C-4.mat`

Each file includes:

1. **Two data matrices** containing the maximum displacement demands:
   - One for **slender pier walls** (i.e., *Windows* wall)  
   - One for **squat pier walls** (i.e., *Doors* wall)  
   Displacements are expressed in **mm**.  
   NaN values indicate collapse, either due to crashing of the numerical analysis procedure or when the drift ratio demand exceeds **4%**, as defined in the paper.  
   Matrix columns are structured as follows:
     - Column 1: Demand under H1 only  
     - Column 2: Demand under H2 only  
     - Column 3: Demand under combined H1 + V  
     - Column 4: Demand under combined H2 + V

2. **A matrix of ground motion record IDs** (83 rows × 4 columns), listing the applied record identifiers.  
   Each row corresponds to one ground motion pair (H1, H2), analysed both with and without the vertical component.  
   The order of the rows matches that of the displacement demand matrices.

For detailed descriptions of each analysis set, refer to:  
[`../TremuriModels/Model_Variations.md`](../TremuriModels/Model_Variations.md)
