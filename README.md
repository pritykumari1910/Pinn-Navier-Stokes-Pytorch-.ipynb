# 🌪️ Physics-Informed Neural Network (PINN) — 2D Navier–Stokes Solver

This project implements a **Physics-Informed Neural Network (PINN)** in **PyTorch** to solve the **2D incompressible Navier–Stokes equations** using the **Taylor–Green vortex** analytical solution for validation.

---

## 🧠 Overview

Traditional Computational Fluid Dynamics (CFD) solvers rely on discretization and heavy computation.  
A **PINN** learns the underlying **partial differential equations (PDEs)** directly — enforcing **physics constraints** (e.g., momentum & continuity) in the loss function.

This project shows how neural networks can learn **fluid dynamics** governed by:
\[
\\begin{cases}
u_t + u u_x + v u_y = -p_x + \\nu (u_{xx} + u_{yy}) \\\\
v_t + u v_x + v v_y = -p_y + \\nu (v_{xx} + v_{yy}) \\\\
u_x + v_y = 0
\\end{cases}
\]

---

## ⚙️ Features

✅ Solves 2D Navier–Stokes using **PyTorch autograd**  
✅ Uses **Taylor–Green vortex** as an analytical reference  
✅ Includes **periodic boundary conditions**  
✅ Physics-based loss: momentum + continuity + BC + IC  
✅ Visualizes predicted velocity & pressure fields  
✅ GPU compatible (CUDA)

---



## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/pinn-navier-stokes.git
cd pinn-navier-stokes




2️⃣ Install Requirements
pip install torch numpy matplotlib



3️⃣ Run the Script

python pinn_navier_stokes_pytorch.py




During training, you’ll see loss values for:

PDE residuals

Initial conditions

Boundary conditions

and final plots comparing predicted vs exact solutions for velocity and pressure.




🧮 Model Architecture

Input: (x, y, t)

Output: (u, v, p)

4–6 hidden layers × 64 neurons each

Activation: tanh

Optimizers: Adam + LBFGS hybrid training


<img width="734" height="199" alt="image" src="https://github.com/user-attachments/assets/0f58fea4-a64a-4884-b94d-5bf1ea04483c" />


<img width="855" height="392" alt="image" src="https://github.com/user-attachments/assets/07c07b33-69db-4866-b6cc-6fd4e29ed006" />
	
	
🧪 Theory Reference

Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations. Journal of Computational Physics, 378, 686–707.

🧰 Tech Stack

Python 3.10+

PyTorch

NumPy

Matplotlib

🏁 Future Work

Extend to 3D Navier–Stokes

Add turbulence modeling

Use domain decomposition (DeepONet)

Integrate with experimental fluid data



🪐 License

MIT License © 2025 — Free to use for research and learning purposes.
