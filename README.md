# GPU Password Cracker (Brute Force using PyTorch)

## Overview
This project demonstrates how to use PyTorch with GPU acceleration in Google Colab to brute-force crack a 4-character lowercase password. It highlights the use of GPU parallel processing to efficiently generate and compare all possible password combinations.

## Technologies Used
- Python 3
- PyTorch
- Google Colab (with GPU runtime enabled)
- CUDA-enabled GPU

## How It Works
The notebook generates all possible 4-letter lowercase passwords by creating a Cartesian product of the letters 'a' to 'z' using PyTorch tensors. This massive search space (26^4 = 456,976 combinations) is processed in parallel on the GPU. Each candidate password is compared with the target password, and the matching password is printed once found.

## Project Structure

gpu-password-cracker/
├── gpu_password_cracker.ipynb # Google Colab notebook with the brute force code
├── output.txt # Sample output from running the notebook
├── README.md # This file
└── run_instructions.md # Step-by-step guide to run the notebook in Colab


## Sample Output

When running the notebook in Google Colab with a GPU runtime, you should see output similar to:

Using device: cuda
Password found: cuda


## How to Run

1. Open Google Colab: https://colab.research.google.com
2. Upload the file `gpu_password_cracker.ipynb`.
3. Go to `Runtime` > `Change runtime type`.
4. Select:
   - Runtime type: Python 3
   - Hardware accelerator: GPU
5. Run all the cells in the notebook.
6. Observe the output showing the device used and the found password.

## Notes

- This project is designed to run on GPUs compatible with CUDA.
- The current implementation only supports 4-character lowercase passwords (a-z).
- Expanding to longer passwords or including more character types will increase computational complexity exponentially.
- Google Colab provides free access to GPUs but with limited session durations and availability.

