Download Link: https://assignmentchef.com/product/solved-stat-547-homework2
<br>
<ol>

 <li>For <strong>f </strong>= [<em>f</em><sub>1</sub><em>,f</em><sub>2</sub>]<em>, </em><strong>g </strong>= [<em>g</em><sub>1</sub><em>,g</em><sub>2</sub>] : [0<em>,</em>1] → R<sup>2 </sup>with <em>f<sub>j</sub></em>, <em>g<sub>j </sub></em>∈ <em>L</em><sup>2</sup>[0<em>,</em>1], define an inner product</li>

</ol>

This inner product allows us to define an FPCA for a bivariate stochastic process <strong>X</strong>(<em>t</em>) = [<em>X</em><sub>1</sub>(<em>t</em>)<em>,X</em><sub>2</sub>(<em>t</em>)], <em>t </em>∈ [0<em>,</em>1], as described in Section 8.5 of Ramsay and Silverman (2005) (attached). Implement this FPCA in code, and apply it to analyze the gait cycle data fda::gait.

<ol start="2">

 <li>Simulate a sample of <em>n </em>= 20 realizations from (1) a Gaussian process, and (b) a nonGaussian process. Display the simulated processes.</li>

 <li>Implement an FPCA for the yeast data (available under the Misc section of the Class Notebook). Describe the first few modes of variation, and discuss whether the variation in the dataset is properly summarized by the first few eigenfunctions using FPCA.</li>

 <li>Let <em>X</em><sub>1</sub><em>,…,X<sub>n </sub></em>be independent realizations of an <em>L</em><sup>2 </sup>stochastic process <em>X </em>on T = [0<em>,</em>1]. Let (<em>λ</em>ˆ<em><sub>k</sub>,φ</em>ˆ<em><sub>ik</sub></em>) be the <em>k</em>th eigenvalue–eigenfunction pair of the sample covariance function</li>

</ol>

<em>G</em>ˆ. Let . Show that

(a) <em>Z<sub>k </sub></em>= 0 for <em>k </em>= 1<em>,…,n </em>− 1;

; .

<ol start="5">

 <li>Let <em>x</em><sub>1</sub><em>,…,x<sub>n </sub></em>be <em>n </em>linearly independent (nonrandom) functions in a Hilbert space H. ) has rank <em>n </em>− 1.</li>

 <li>(Reproducing Kernel Hilbert Space) Let <em>K </em>: [0<em>,</em>1]×[0<em>,</em>1] → R be a continuous function (Mercer’s kernel). Define</li>

</ol>

<em>,</em>

1

where the (<em>λ<sub>j</sub>,e<sub>j</sub></em>) are the eigenvalue and eigenfunction pairs of the covariance operator

<em>K </em>associated with <em>K</em>. For  and , define inner product

<em>.</em>

Then H<em>K </em>is a Hilbert space with this norm.

<ul>

 <li>Show that), where the sum converges absolutely.</li>

 <li>Show that <em>K</em>(·<em>,t</em>) ∈ H<em>K </em>for <em>t </em>∈ [0<em>,</em>1].</li>

 <li>Show that h<em>K</em>(·<em>,t</em>)<em>,f</em>i<em>K </em>= <em>f</em>(<em>t</em>) for <em>t </em>∈ [0<em>,</em>1]. This means the evaluation functional <em>δ<sub>t </sub></em>: H<em>K </em>→ R, <em>δ<sub>t</sub></em>(<em>f</em>) = <em>f</em>(<em>t</em>) is a continuous linear functional.</li>

</ul>

(Remark: A Hilbert space of functions in which point evaluation is a continuous linear functional is called a Reproducing Kernel Hilbert Space (RKHS). )

2

<strong>from Ramsay and Silverman 2005 Functional Data Analysis Second Edition</strong>

166              8. Principal components analysis for functional data

Figure 8.7. The solid curve in each panel is the mean acceleration in height in cm/year<sup>2 </sup>for girls in the Zurich growth study. Each principal component is plotted in terms of its effect when added (+) and subtracted (−) from the mean curve.

marker events. Full details of this process can be found in Ramsay, Bock and Gasser (1995). The curves are for 112 girls who took part in the Zurich growth study (Falkner, 1960).

Figure 8.7 shows the first three eigenfunctions or harmonics plotted as perturbations of the mean function. Essentially, the first principal component reflects a general variation in the amplitude of the variation in acceleration that is spread across the entire curve, but is particularly marked during the pubertal growth spurt lasting from 10 to 16 years of age. The second component indicates variation in the size of acceleration only from ages 4 to 6, and the third component, of great interest to growth researchers, shows a variation in intensity of acceleration in the prepubertal period around ages 5 to 9 years.

<h1>                  8.5     Bivariate and multivariate PCA</h1>

We often wish to study the simultaneous variation of more than one function. The hip and knee angles described in Chapter 1 are an example; to understand the total system, we want to know how hip and knee angles vary jointly. Similarly, the handwriting data require the study of the simultaneous variation of the X and Y coordinates; there would be little point in studying one coordinate at a time. In both these cases, the two variables being considered are measured relative to the same argument, time in both cases. Furthermore, they are measuring quantities in the same units (degrees in the first case and cm in the second). The discussion in this section is particularly aimed towards problems of this kind.


