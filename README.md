# UHF_RF_Front_End_Design
RF front-end designs for the UHF comms board at 401.4 MHz. Includes matching networks, LPF and BPF filters for TX/RX   paths, HFSS + Simsurf simulation results, schematic captures, and the final filter set integrated with the comms   transceiver chip. signal_chain.png shows on-board placement.

 # UHF Signal Chain & Filter Designs

  RF front-end design files for the UHF communication board operating at **401.4 MHz** — the band used for satellite
  telemetry and command links. The board carries the UHF comms transceiver chip and handles signal conditioning between
  the antenna ports and the chip through a chain of impedance-matching networks and filters.

  ## Signal Chain
  See `Implemented_xxxx_Circuit.png` for the block-level placement of each filter and matching stage on the board, between the
  antenna and the transceiver.

  ## Folder Map

  | Folder           | Purpose                                                  |
  |------------------|----------------------------------------------------------|
  | `LPF_UHF/`       | Low-pass filter — harmonic rejection on the TX path      |
  | `Match_1_lpf/`   | Matching network 1 + LPF stage                           |
  | `Match_2_lpf/`   | Matching network 2 + LPF stage                           |
  | `UHF_BPF/`       | Bandpass filter centered at 401.4 MHz                    |
  | `rx_path_match/` | Receive-path impedance matching to the transceiver chip  |

  Each subfolder contains schematic captures and S-parameter / Z-parameter plots from both ideal and Simsurf
  substrate-aware simulations.

  ## Top-Level Files
  - `RX_PATH_UHF.aedt` — full receive-path HFSS simulation
  - `tx_path_uhf.aedt` — full transmit-path HFSS simulation
  - `UHF_BPF.aedt` / `UHF_BPF.pdf` / `UHF_BPF_Simsurf.pdf` — BPF design and results
  - `Updates.pdf` — design iteration notes and review history

  ## Final Filters Used
  The filter and matching stages selected from these iterations were integrated into the final UHF board signal chain.
  Their placement is marked in `Implemented_xxxx_Circuit.png`.

  ## Tools
  - **ANSYS HFSS / Electronics Desktop** for EM simulation
  - **Simsurf** substrate models for realistic on-PCB performance
