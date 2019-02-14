# Math54

---
title: Math 54 Presentation | Ardel Bontilao, James Casia, and Kent Makibulan
---
# Hyperbolic Functions 
> By: Ardel Anton Bontilao, James Gabriel Casia, and Kent Leo Makibulan [color=skyblue]
> 
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.3/Chart.bundle.js"></script>

<div>
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("myChart").getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero:true
                }
            }]
        }
    }
});
</script>
</div>

### **1. Prove:  $\DeclareMathOperator{\sech}{sech}1-\tanh^2 x= \sech^2x$**

Solution:

\begin{align*}
\DeclareMathOperator{\sech}{sech}
1-\tanh^2 x &= \sech^2x \\\\
1 - \left(\frac{e^x-e^{-x}}{e^x+e^{-x}}\right)^2 &= \sech^2{x} \\\\
1 - \frac{(e^x-e^{-x})^2}{(e^x-e^{-x})^2} &= \sech^2x \\\\
1 - \frac{e^{2x}+e^{-2x}-2}{e^{2x}+e^{-2x}+2} &= \sech^2x \\\\
\frac{(e^{2x}+e^{-2x}+2)-(e^{2x}+e^{-2x}-2)}{e^{2x}+e^{-2x}+2} &= \sech^2x \\\\
\frac{4}{e^{2x}+e^{-2x}+2} &= \sech^2x \\\\
\frac{2^2}{(e^x+e^{-x})^2} &= \sech^2x \\\\
\left(\frac{2}{e^x+e^{-x}}\right)^2 &= \sech^2x \\\\
\sech^2x &= \sech^2x \\\\
\end{align*}

### **2. Prove:  $\sinh{(x+y)} = \sinh{x} \cosh{y} + \cosh{x}\sinh{y}$**

Solution:

\begin{align*}
\sinh{(x+y)} &= \sinh{x} \cosh{y} + \cosh{x}\sinh{y} \\\\
\sinh{(x+y)} &= \left(\frac{e^x-e^{-x}}{2}\right)\cdot\left(\frac{e^y+e^{-y}}{2}\right)+\left(\frac{e^x+e^{-x}}{2}\right)\cdot\left(\frac{e^y-e^{-y}}{2}\right) \\\\
\sinh{(x+y)} &= \left(\frac{e^{x+y}+e^{x-y}-e^{-x+y}-e^{-x-y}}{4}\right) + \left(\frac{e^{x+y}-e^{x-y}+e^{-x+y}-e^{-x-y}}{4}\right) \\\\
\sinh{(x+y)} &= \frac{2\left(e^{x+y}-e^{-x-y}\right)}{4}\\\\
\sinh{(x+y)} &= \left(\frac{e^{x+y}-e^{-(x+y)}}{2}\right) \\\\
\sinh{(x+y)} &= \sinh{(x+y)} \\\\
\end{align*}

<!-- **Problems**

kent 7 22 44 69
shane 13 33 49
james 19 43 65 -->
 
### **3. Evaluate: $\int \sinh^4 x \cosh x \ \mathrm{dx}$** ###


Solution:


 $$ \text{let u} =\sinh x \\ \text{du} = \cosh x \ \mathrm{dx}$$

\begin{align*} \\
y &= \int \sinh^4 x \cosh x \ \mathrm{dx}\\
y &= \int u^4 \mathrm{du}\\
y&= \frac{u^{4+1}}{4+1} + c\\
y &= \frac{u^5} {5}+c\\ \\
&\text{substituting u with $\sinh x$} \\ \\
y &=\frac {sinh^5{x}}{5} + c
\end{align*}



### **4.Evaluate: $\int{\coth^2{3x}\ \mathrm{dx}}$**

Solution:

\begin{align*}
\text{let} \ u &= 3x\\\\
du &= 3\mathrm{dx}\\\\
&= \frac{1}{3}\int{\coth^2{u}\ \mathrm{du}} \\\\
&=\frac{1}{3}\int{\left(\text{csch}^2(u) + 1\right) \mathrm{du}} \\\\
&=\frac{1}{3}\int{\text{csch}^2(u)\ \mathrm{du}} + \frac{1}{3}\int{1\ \mathrm{du}} \\\\
&= -\frac{1}{3}\ \coth{(u)} + \frac{u}{3} + C \\\\
& \text{ substituting} \ u \  \text{back} \\\\
&= x - \frac{1}{3} \coth{(3x)} + C \\\\
\end{align*}

### **5. This particular problem ☄️ ⚛️:**
 A particle is moving on a line according to the equation of motion 
 
 $$s = e^{-t/2}(3\sinh t + 4 \cosh t)$$
where $s$ centimeters is the directed distance of the particle from the origin at $t$ seconds. If $v$ centimeters per second and $a$ centimeters per second per second are the velocity and acceleration, respectively, of the particle at $t$ seconds,
- (a) express $v$ and $a$ as functions of $t$, 
\begin{align*}
v &= \frac{ds}{dt}\\
a &= \frac{dv}{dt}
\end{align*}
- (b) Show that a is the sum of two numbers, one of which is proportional to $s$ and the other proportional to $v$.

<div></div>




### **5. Find the derivatives:** ###
\begin{align*} 
\text{(a)    }f(x) = \cosh^{-1}\frac{1}{3}x\\
\text{(b)    } F(x) = \tanh^{-1} x^3\\ 
 \end{align*}

Solution: 

\begin{align*}
\\
\text{(a)     }Dx(f(x)) &= Dx(\cosh^{-1}\frac{1}{3}x)\\
Dx(f(x)) &= 
\end{align*}



### **6. Find the derivatives:** ###
\begin{align*}
\text{(a)    }f(x) = \sinh x^2\\
\text{(b)    }f(x) = \sech^2 4w\\
\end{align*}

Solution:
\begin{align*}
\text{(a)    }Dx(f(x)) &= D (\sinh x^2)
\\Dx(f(x)) &= \cosh x D x^\
\\Dx(f(x)) &= \cosh x \cdot 2x^{2-1}\frac{dx}{dx}
\\Dx(f(x)) &= 2x \cosh x^2
\\\\
\text{(b)    }Dx(f(x)) &= D (\sech^2 4w), \text{ let }u \ \text{=} \sech4w\\
\text{       }Dx(f(x)) &= 2 (u)^{2-1} D(u)
\\Dx(f(x)) &= 2 sech 4w (-sech 4w\cdot{}tanh4w\cdot{}4)
\\Dx(f(x)) &= -8sech^24w\cdot{}tanh4w
\end{align*}

### **7. Determine the exact function value:**

\begin{align*}
\text{(a) }cosh^{-1}\ 1 &= \ ?
\\\text{we know that} \ y = cosh^{-1} \ x <=> x=cosh \ y 
\end{align*}

### **8. Find the derivative of the function:**
\begin{align*}
\text{(a)    }g(x) &= \tanh^{-1}(\sin{3x}) \\
\text{(b)    }F(x) &= \coth^{-1} (3 \sin{x})4w\\\\
\end{align*}

\begin{align*}
\text{(a)   } g\prime(x) &= \frac{d}{dx}\left(\tanh^{-1}(\sin{3x})\right) \\\\
\text{let } u &= \sin{3x} \\\\
\end{align*}
















 
