---
layout: project
type: project
image: img/cotton/cotton-square.png
title: "Complex Numbers Calculator"
date: 2024
published: true
labels:
  - Lisp
  - GitHub
summary: "A Complex class made in my Program Structure class that represents complex numbers and performs mathematical operations."
---

<img class="img-fluid" src="../projects/images/complex-num.png">



<hr>

<pre style="background-color: black; color: white; padding: 10px;">
  <code>
 /**
   * ADDS the current Complex number to another
   * @param addComplex   the Complex object to be added to the current object
   * @return a new Complex object that represents the sum of the two complex numbers  
   */
  Complex add(const Complex &addComplex) const {
    // follows formula (a + bi) + (c + di) = (a + c) + (b + d)i
    double newReal = real + addComplex.real;
    double newImaginary = imaginary + addComplex.imaginary;

    // return a new object with above sums as parameters
    return Complex(newReal, newImaginary);
  }

  /**
   * SUBTRACTS another Complex object from the current one
   * @param subtractComplex   the Complex object to be subtracted from the current object
   * @return a new Complex object that represents the difference of the two complex numbers
   */
  Complex subtract(const Complex &subtractComplex) const {
    // follows formula (a + bi) - (c + di) = (a - c) + (b - d)i
    double newReal = real - subtractComplex.real;
    double newImaginary = imaginary - subtractComplex.imaginary;

    // return a new object with above differences as parameters
    return Complex(newReal, newImaginary);
  }

  /**
   * MULTIPLIES the current Complex object by another
   * @param multiplyComplex   the Complex object to multiply with the current object
   * @return a new Complex object that represents the product of the two complex numbers
   */
  Complex multiply(const Complex &multiplyComplex) const {
    // follows formula (a + bi) * (c + di) = (a*c - b*d) + (b*c + a*d)i
    double newReal = real * multiplyComplex.real - imaginary * multiplyComplex.imaginary;
    double newImaginary = imaginary * multiplyComplex.real + real * multiplyComplex.imaginary;

    // return a new object with above products as parameters
    return Complex(newReal, newImaginary);
  }

  /**
   * DIVIDES the current Complex object by another
   * @param divideComplex   the Complex object to be divided by the current object
   * @return a new Complex object that represents the quotient of the two complex numbers
   */
  Complex divide(const Complex &divideComplex) const {
    // follows formula (a + bi) / (c + di) = ((a*c + b*d)/(c*c + d*d)) + ((b*c - a*d)/(c*c + d*d))i
    double newReal = (real * divideComplex.real + imaginary * divideComplex.imaginary) / (divideComplex.real * divideComplex.real + divideComplex.imaginary * divideComplex.imaginary);
    double newImaginary = (imaginary * divideComplex.real - real * divideComplex.imaginary) / (divideComplex.real * divideComplex.real + divideComplex.imaginary * divideComplex.imaginary);

    // return a new object with above quotients as parameters
    return Complex(newReal, newImaginary);
  }
</code></pre>

<hr>

Source: <a href="https://github.com/jogarces/ics-313-text-game"><i class="large github icon "></i>jogarces/ics-313-text-game</a>
