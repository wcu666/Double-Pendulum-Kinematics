# 🌀 Double Pendulum Kinematics Simulation

> **National Chung Cheng University (CCU), Department of Physics**  
> *General Physics (I) Final Project*  
> **Author:** CHANG-YU, WU

An interactive, web-based physics simulation engine that models the chaotic dynamics of a classic double pendulum system using **4th-Order Runge-Kutta (RK4)** numerical integration.

---

## 🌟 Key Features

* **⚡ High-Precision Numerical Engine**: Built with a 4th-Order Runge-Kutta (RK4) solver ($\Delta t = 0.004\text{ s}$) to accurately simulate complex non-linear dynamics and chaos.
* **📊 Multi-View Analytical Charts**: Real-time plotting driven by `Chart.js`:
  * **Energy Conservation Analysis**: Live tracking of Kinetic Energy ($T$), Potential Energy ($V$), and Total Energy ($E$).
  * **Kinematic Time-Series**: Angular displacement ($\theta(t)$) and angular velocity ($\omega(t)$).
  * **Phase Space Trajectory**: Phase space dynamics ($\omega_1 \text{ vs. } \theta_1$ and $\omega_2 \text{ vs. } \theta_2$) revealing chaotic attractor structures.
* **🎛️ Live Parameter Control Panel**:
  * Adjust masses ($m_1, m_2$) and rod lengths ($L_1, L_2$) on the fly.
  * Set initial angular positions ($\theta_1, \theta_2$) from $0^\circ$ to $360^\circ$.
  * Adjustable analytical time window and visual trail length.
* **🎨 Academic-Grade UI Design**: Styled with standard academic aesthetics (serif typography, neutral canvas grid, color-coded components).

---

## 📐 Physics & Mathematical Background

### 1. Equations of Motion
The double pendulum system is derived via **Lagrangian Mechanics** ($L = T - V$). The non-linear coupled second-order differential equations governing the angular accelerations $\ddot{\theta}_1$ and $\ddot{\theta}_2$ are:

$$\ddot{\theta}_1 = \frac{m_2 g \sin\theta_2 \cos(\theta_1 - \theta_2) - m_2 \sin(\theta_1 - \theta_2) [L_1 \dot{\theta}_1^2 \cos(\theta_1 - \theta_2) + L_2 \dot{\theta}_2^2] - (m_1 + m_2) g \sin\theta_1}{L_1 [m_1 + m_2 \sin^2(\theta_1 - \theta_2)]}$$

$$\ddot{\theta}_2 = \frac{(m_1 + m_2) [L_1 \dot{\theta}_1^2 \sin(\theta_1 - \theta_2) - g \sin\theta_2 + g \sin\theta_1 \cos(\theta_1 - \theta_2)] + m_2 L_2 \dot{\theta}_2^2 \sin(\theta_1 - \theta_2) \cos(\theta_1 - \theta_2)}{L_2 [m_1 + m_2 \sin^2(\theta_1 - \theta_2)]}$$

### 2. Numerical Integration (RK4)
The state vector $\mathbf{y} = [\theta_1, \omega_1, \theta_2, \omega_2]^T$ is updated at each step using 4th-Order Runge-Kutta integration:

$$\mathbf{y}_{n+1} = \mathbf{y}_n + \frac{\Delta t}{6}(k_1 + 2k_2 + 2k_3 + k_4)$$

---

## 🛠️ Tech Stack

* **Language**: Vanilla JavaScript (ES6+), HTML5, CSS3
* **Rendering**: HTML5 Canvas API (2D Context)
* **Data Visualization**: [Chart.js](https://www.chartjs.org/) v4.x
* **Fonts**: Times New Roman / Modern Serif for academic typography

---

## 🚀 Getting Started

### Option 1: Direct Run (Local)
1. Clone this repository:
   ```bash
   git clone [https://github.com/wcu666/YOUR_REPO_NAME.git](https://github.com/wcu666/YOUR_REPO_NAME.git)
