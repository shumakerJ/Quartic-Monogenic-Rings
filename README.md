# **Quartic Monogenic Orders: Computational Tools**  

This repository contains code related to my research on **quartic monogenic orders**, focusing on algorithms for identifying monogenizations of quartic rings. The implementation is based on the algorithm by **István Gaál, Attila Pethő, and Michael Pohst** for finding generators of orders in quartic number fields.  

## **Features**  
- Computes all monogenizations of a quartic order defined by an irreducible monic polynomial.  
- Implements the cubic resolvent Thue equation method to find integer-valued triples representing monogenizers.  
- Outputs a dictionary pairing solutions of the Thue equations with monogenization representatives.  

## **Requirements**  
This code is written for **SageMath 10.5** and requires the following dependencies:  
- **SageMath** (https://www.sagemath.org/)  
- **Pari/GP** (https://pari.math.u-bordeaux.fr/)  
- **NumPy** (if applicable)  
- Other dependencies (list any additional ones)  

## **Usage**  
To run the code, open a SageMath notebook or script and execute:  
```python
# Example usage
#after running the "Run me first cell"
find_monogens([1,a1,a2,a3,a4])
```
Replace `[1,a1, a2, a3, a4]` with the coefficients of your quartic polynomial.  

## **Mathematical Background**  
This code is an **implementation of the algorithm** described in:  

- **István Gaál, Attila Pethő, and Michael Pohst**, *On the Resolution of Index Form Equations in Quartic Number Fields*, J. Number Theory, 1996. ([Link](https://www.sciencedirect.com/science/article/pii/S0022314X96900359))  

Given an **irreducible monic quartic polynomial** \( f(t) \), the algorithm finds all **monogenizations** of the associated order \( \mathbb{Z}[t]/(f(t)) \). A ring is **monogenic** if it is generated by a single element as a \( \mathbb{Z} \)-algebra.  

The algorithm first solves the **cubic resolvent Thue equation**. For each solution, it determines a corresponding **quartic Thue equation**, whose solutions, in turn, define integer triples \( (x, y, z) \) such that  
\[
c + x t + y t^2 + z t^3
\]  
is a **monogenizer** of the order. Each **monogenization** is represented uniquely in the output.  

## **Future Work**  
Planned improvements include:  
- Extending support to cubic orders.
- Improve preprocessing for thue equation solver.  
- **Removing the redundant** `1` **from the input representation.**  

## **Contributing**  
Contributions are welcome! If you have improvements or suggestions, feel free to submit a pull request or open an issue.  

---

Let me know if you'd like any other refinements!
