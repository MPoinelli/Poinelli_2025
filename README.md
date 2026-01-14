## Welcome!

MITgcm model code to reproduce the results of Poinelli et al., 2025 Nature Geoscience and Poinelli et al., 2025 JAMES. 

The model output consisting of 10 TB of data including daily, weekly and monthly output for a nominal time frame of 01-Jan-2010 to 01-Nov-2010.
Model output is available on the Jet Propulsion Laboratory’s Physical Oceanography Distributed Active Archive Center (PODAAC) with the [ECCO-drive](https://ecco.jpl.nasa.gov/drive/files/ECCO2/High_res_PIG/ASE_Poinelli2025) (registration is required).

If you use this code or model output, please cite te appropriate publication:
- Poinelli, M., Siegelman, L. & Nakayama, Y. Ocean submesoscales as drivers of submarine melting within Antarctic ice cavities. Nat. Geosci. 18, 1209–1215 (2025). [[link]](https://doi.org/10.1038/s41561-025-01831-z)
- Poinelli, M., Siegelman, L., Nakayama, Y., Rignot, E., Seroussi, H., Fenty, I., & Larour, E. (2025). Small-scale, high-frequency ice, and ocean processes in the Amundsen Sea Embayment, West Antarctica. Journal of Advances in Modeling Earth Systems, 17, e2025MS005098. [[link]](https://doi.org/10.1029/2025MS005098)

If you have questions, please do not hesitate to send [me](mpoinell@uci.edu) an email.

## Code, input and output description
This repository includes three source code folders, three input folders and three run folders categorized by model resolution:

- `code_200m`: Amundsen Sea Embayment simulation at 200 m resolution, MITgcm code
- `code_500m`: Amundsen Sea Embayment simulation at 500 m resolution, MITgcm code
- `code_1km`:  Amundsen Sea Embayment simulation at 200 m resolution, MITgcm code

- `input_200m`: Amundsen Sea Embayment simulation at 200 m resolution, MITgcm input files
- `input_500m`: Amundsen Sea Embayment simulation at 500 m resolution, MITgcm input files
- `input_1km`:  Amundsen Sea Embayment simulation at 200 m resolution, MITgcm input files

Model output are provided only in the ECCO drive and consists of daily, weekly, monthly averages.
Output is stored in `set` binary files, and the content of each `set` can be found in the appropriate `input/data.diagnostics`

 - `run_200m`: Amundsen Sea Embayment simulation at 200 m resolution, MITgcm model output (only in the ECCO drive, not github) 

Note that run_200m is divided into two folders (`run_b` and `run_c`). The difference is the time-step which in `run_b` is 10s from 01-Jan-2010 to 15-Jun-2010 and in `run_c` is 5s from 16-Jun-2010 to 01-Nov-2010. Timestamps are reflecting this changes. 
To convert timestamps to nominal date use this [gist](https://gist.github.com/MPoinelli/ef5b6c32444465f58c7caef068a41aaa).

- `run_500m`: Amundsen Sea Embayment simulation at 500 m resolution, MITgcm model output (only in the ECCO drive, not github)
- `run_1km`:  Amundsen Sea Embayment simulation at 200 m resolution, MITgcm model output (only in the ECCO drive, not github)


<figure align="center">
  <img
    src="https://github.com/user-attachments/assets/4b5f01bb-490a-46e9-8bc6-1b290df7826d"
    alt="Figure 1"
    width="600"
  />
  <figcaption>
    <strong>Figure 1.</strong> Fig. 1 from Poinelli et al. 2025, JAMES.
  </figcaption>
</figure>



## To build MITgcm
Please follow instructions listed [here](https://mitgcm.readthedocs.io/en/latest/getting_started/getting_started.html)

Note that model results and code are based on MITgcm checkpoint68r referenced here:
- Campin, J.M., Heimbach, P., Losch, M. et al. (2023). MITgcm/MITgcm: ckeckpoint68r (Version checkpoint68r). Zenodo. [[link]](https://doi.org/10.5281/zenodo.8208482)
