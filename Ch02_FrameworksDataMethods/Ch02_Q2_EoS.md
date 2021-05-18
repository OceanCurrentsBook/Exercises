Take a look at the table below containing measurements of (in-situ) temperature and salinity in a deep part of the ocean. 

| Depth (m) | In-situ Temperature (<sup>o</sup>C) | Absolute Salinity |
| --------- | ------------------------ | ----------------- |
|         0 |                   18.909 |            32.574 |
|     -2000 |                    1.868 |            34.600 |
|     -4000 |                    1.456 |            34.679 |
|     -5460 |                    1.547 |            34.688 |

a) Write a python programme to check whether density increases with depth if a linear equation of state for temperature and salinity is taken. Use: 
ρ = ρ<sub>0</sub> (1−α<sub>T</sub>(T −T<sub>0</sub>) + β<sub>S</sub>(S−S<sub>0</sub>)) 
with a reference density ρ<sub>0</sub> = 1027 kg m<sup>-3</sup>, thermic expansion coefficient α<sub>T</sub> = 1.0·10<sup>−4</sup> K<sup>−1</sup>, and haline expansion coefficient β<sub>S</sub> = 7.0·10<sup>−4</sup>. T<sub>0</sub> and S<sub>0</sub> are the temperature and salinity at the surface respectively. 

b) Is the water column stable? Explain. 

As discussed in the book, the TEOS10 equations provide more accurate Equations of State. For Python, there is the gsw package. If you have installed python via anaconda, you can open the anaconda prompt and type `pip install gsw`. Restart jupyter.
Now you can import the gsw package with `import gsw`.

c) Use the `gsw.conversions.p_from_z()` function to convert the measurement depths to pressure (assuming the measurements were taken at a latitude of 20<sup>o</sup>N) and the `gsw.conversions.CT_from_t()` function to convert the in-situ temperature to Conservative Temperature. Finally, use the `gsw.density.rho()` function to compute the in-situ density. Use the `help()` function for instructions how to use these functions.

d) How do the Conservative temperatures differ from the in-situ temperatures? And how does the density computed form the gsw package differ from the density in the equation at a)?

e) Assume we have two different water parcels at -1500m depth. The characteristics of the parcels are T<sub>1</sub>=0<sup>o</sup>C, S<sub>1</sub>=33.5 g/kg, and T<sub>2</sub>=8.35<sup>o</sup>C, S<sub>2</sub>=35 g/kg (T: in-situ temperatures). Use the gsw package to determine the densities of the two parcels.
Now we will mix the two parcels to form a third parcel. Determine the density of the third parcel (you can assume that the volumes of the two parcels are equal). Locate the three parcels in a T-S-density diagram. What will happen with the third parcel? Does this behaviour depend on the proportions? What happens to the densities if we brought all parcels to the surface?
