## Theory
**Introduction:**  
**Small scale fading** characterizes the fluctuation of signal (strength) over a spatial distance of fraction of wavelength.

The fluctuation is also observed in both time and frequency domain at a gain location.

The variation of signal (strength) at the receiver is due to random interference between the different copies of the transmitted signal. The interference is sometimes constructive and sometimes destructive. The multiple copies of the transmitted signal are generated due to scattering, reflection and diffraction due to obstacle present in the path of radio signal between the Tx and Rx movement of the Tx and Rx or the obstacle cause time domain variation of the signal (strength) and the phenomenon is called Doppler effect. Since each path of the radio wave may exhibit difference doppler its cumulative effect results in spread of the carrier/ frequency content of the signal and hence is also known as Doppler spread.

If v is the maximum velocity (m/s) then the maximum Doppler shift is given by

$$f_m = v/c \cdot f_c$$

*(Note: The original HTML formula was likely missing the $f_c$ term)*

Where,

* `c = velocity light = 3 \times 10^8 m/s.`
* `$f_c$ = carrier frequency.`

Coherence time is defined as interval in time over which the signal remains correlated. It is defined as

$$T_c = \frac{9}{16\pi f_m} (s)$$

If symbol duration `$T_s \ll T_c$` it experience slow fading while if `$T_s > T_c$` it experience fast fading. The enveloped level crossing rate is defined as the rate at which the signal envelope crosses a specified level R in the positive (or negative) going direction.

It requires the joint pdf `$(p(\alpha, \dot{\alpha}))$` of the enveloped level `$\alpha = |r|$` and enveloped slope `$\dot{\alpha} = |\dot{r}|$`

$$L_R = \sqrt{2\pi(k+1)} f_m \rho e^{-k-(k+1)\rho^2} I_0(2 \rho \sqrt{k(k+1)})$$
$$\rho = R / \sqrt{\Omega_p} = R / R_{rms}$$

`$R_{rms} = \sqrt{\Omega_p}$` is the enveloped level

Rayleigh fading (k=0) and isotropic scattering
$$L_R = \sqrt{2\pi} f_m \rho e^{-\rho^2}$$

---

**Level Crossing Rate For Selection Combining**

$$L_r = f_m \frac{\sqrt{\pi} M \gamma}{\sqrt{\sigma}} \exp(-\frac{\gamma^2}{2\sigma}) [1 - \exp(-\frac{\gamma^2}{2\sigma})]^{M-1}$$

Where,

* `$f_m$` is the Maximum doppler frequency.
* `$\sigma$` is the r.m.s value of the received signal voltage.
* `$\gamma$` is the threshold voltage.
* M = No. of channels

---

**Level Crossing Rate for MRC Combining**

$$L_r = 0.5 f_m \left[ \frac{\sqrt{2\pi}(\gamma/\sqrt{M^2+M})^{M-1/2}}{(M-1)!} \right] \exp\left(-\frac{\gamma}{\sqrt{M^2+M}}\right)$$

---

**Average enveloped fade duration**

The average duration the enveloped remains below a specified level R.

$$t = \frac{1}{N_R} P_r[r \le R]$$

**Average fade duration For Selection Combining**

$$ADF = \frac{\sqrt{\rho} \cdot \exp(\gamma^2/(2\sigma) - 1)}{\sqrt{2\pi} f_d M_{\gamma}}$$

For Rayleigh distribution fading

$$P_r[r \le R] = \int_0^R P_r(dr) = 1 - \exp(-\rho^2)$$

$$\bar{t} = \frac{e^{\rho^2}-1}{\rho f_m \sqrt{2\pi}}$$

In case of flat fading the plot of signal enveloped of transmitting 'r' is given as

$$p(r) = \frac{r}{\sigma^2} \exp\left(-\frac{r^2}{2\sigma^2}\right) \quad (0 \le r \le \infty)$$
$$= 0 \quad (r < 0)$$

Where,

* `$\sigma$` is the r.m.s value of the received voltage signal before detection.
* `$\sigma^2$` is the time average power of the received signal before enveloped detection.

Probability of outage is defined as

$$P(R) = P_r(r \le R) = \int_0^R p(r)dr = 1 - \exp\left(-\frac{R^2}{2\sigma^2}\right)$$

The mean value `$r_{mean}$` of rayleigh distribution is given by

$$r_{mean} = E[r] = \int_0^\infty r p(r) dr = \sigma \sqrt{\pi/2} = 1.2533\sigma$$

$$\sigma_r^2 = E[r^2] - E^2[r] = \int_0^\infty r^2 p(r) dr - \frac{\sigma^2 \pi}{2}$$
$$= \sigma^2 (2 - \pi/2) = 0.4292\sigma^2$$
 <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3.2.2/es5/tex-mml-chtml.js"></script>    
 
