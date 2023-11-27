# SUTD 5G dataset

## Data Description
We have a private 5G network testbed deployment on the Singapore University of Technology and Design (SUTD) campus.
Based on the 5G tested deployment on campus, we conducted a walk test to measure the network matrices. The mobile network
testing tools used are Keysight Technologies’ Nemo Handy and Nemo Analyze. The Nemo Handy is software installed in a
Samsung Galaxy S22 Ultra to capture data. Nemo Analyze is software installed on a PC to manage the measurement data. 

<img width="843" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/78230a43-dbd0-4aff-80f7-7b8adcdd20e6">

Deployment of RRUs at SUTD campus

The mobile network testing tool used is capable of measuring large array of data. In this study, we focus on some of the
matrices including Time, NR-ARFCN, PCI, SS RSRP serving beam, SS RSRQ serving beam, SS SINR serving beam, PDSCH MCS index for codeword 0, PUSCH MCS index for codeword 0, PDSCH PRBs, PUSCH PRBs, App. rate DL, C-RNTI. The sampling rate for the data
is about 2 samples per second (2 Hz).

| Matrices                        | Details                                                      |
| ------------------------------- |:------------------------------------------------------------:|
| Time                            | Absolute time with millisecond resolution                    |
| NR-ARFCN                        | Absolute radio-frequency channel number                      |
| PCI                             | Physical Cell ID                                             |
| RSRP                            | SS RSRP serving beam                                         |
| RSRQ                            | SS RSRQ serving beam                                         |
| SINR                            | SS SINR serving beam                                         |
| PDSCH MCS index for codeword 0  | Physical Downlink Shared Channel Modulation Coding Scheme    |
| PUSCH MCS index for codeword 0  | Physical Uplink Shared Channel Modulation Coding Scheme      |
| PDSCH PRBs                      | Physical Downlink Shared Channel Physical Resource Block     |
| PUSCH PRBs                      | Physical Uplink Shared Channel Physical Resource Block       |
| App. rate DL                    | iperf3 downlink throughput                                   |
| C-RNTI                          | Cell Radio Network Temporary Identifier                      |

## Tags and labels

| Labels                        | Details                                                                                                |
| ------------------------------- |:----------------------------------------------------------------------------------------------------:|
| Corridor_tag                    | Corridor_tag: tag 0 inner corridor with better signal, tag 1 outer corridor with worse signal.       |
| lab_anom                        | Label for anomaly: defined manually, label 0 no anomaly, label 1 anamoly                             |
| lab_bs                          | Label for black spot: label 0, UE connected; label 1, UE disconnected                                |
| lab_inf                         | Label for interference: label 0, no interference; label 1, interference from other PCI               |
| lab_1rr                         | Label for 1 RRU: 0 2 RRUs are on, 1                                                                  |
| Label                           | SS SINR serving beam                                                                                 |

## Scenarios

Measurements were taken for the 5G testbed according to the following conditions:
1) All RRUs active at level 4: Level with bad signal coverage
2) All RRUs active at level 5: Scenario with indoor Cell
3) All RRUs active at level 6: Scenario with good signal coverage
4) Only one active RRU on at level 6: Measurement for a single RRU

The Table below describes the measurement data collected for each scenarios.


| Scenarios                          | Duration      | #Samples  |
| ---------------------------------- |:-------------:| ---------:|
| Level 4, 2 outdoor RRUs active     | 24min 58s     | 2327      |
| Level 5, 2 outdoor RRUs active     | 19min 19s     | 2031      |
| Level 6, 2 outdoor RRUs active     | 19min 9s      | 2156      |
| Level 6, only outdoor RRU 1 active | 18min 56s     | 2222      |

## DATA COLLECTION

We used a Samsung Galaxy S22 Ultra smartphone for the walk test. We capture the measurement using the indoor mode, where
we capture the measurements based on an indoor floor plan rather than using GPS coordinates. We walked the area for 3
rounds to capture 3 measurements for that area. The path was planned to be continuous to avoid pausing and restarting the
measurement for each round.

The 2 figures below illustrate the path taken for walk tests. First, in round 1, we walked the inner and outer corridor in
the order indicated in the  figure the ending point for round 1 is at the opposite end of the inner corridor. The ending point for
round 1 is the starting point for round 2 and the walk test for round 2 continues in the order shown in latter figure. The ending
point for round 2 is the starting point for round 3 and the walk test for round 3 follows the same path as round 1.

Walk Test: path taken for round 1 and round 3

<img width="657" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/39deeec8-ebaa-4fc0-ac5b-4fd8725e3d2a">

Walk Test: path taken for round 2

<img width="655" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/0e1e54c7-3f3e-407f-b66d-9ae41e399542">


## Sample Results

<img width="565" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/b3a5de24-6c01-478e-881c-ae0e62c60b2e">

Walk Test Result on indoor map: RSRP serving beam at level 4 with all RRUs on.

<img width="526" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/6c83f2c5-d412-4ce8-b25f-87474fab2e66">

Walk Test Result on indoor map: RSRP serving beam at level 5 with all RRUs on.

<img width="543" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/d7a232ae-5d41-40f5-9565-e194d6e43478">

Walk Test Result on indoor map: RSRP serving beam at level 6 with all RRUs on.

<img width="506" alt="image" src="https://github.com/FCCLab/sutd_5g_dataset_2023/assets/137033784/3779eca4-d2f9-483d-8573-b0f068deb6db">

Walk Test Result on indoor map: RSRP serving beam at level 6 with only RRU 1 on.






