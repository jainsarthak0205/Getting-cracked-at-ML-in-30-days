

# Numpy

* Numpy - fast
* Lists are slow 
* Thats why we use numpy

### Why numpy is faster ?
> lets say we have a matrix 3x4 dim and we see that all values in the matrix are integer values  
now lets say if we have number "5" and the computer see it as 8 bits - 00000101  
this 5 is by default to be casted to int 32 which is 4 bytes  
* We can even specify if we want int16
>Where as in list uses a built in int type which consists of size of int value , object value , object type ,reference count(how many times that integers has been pointed at)  
size is 4 bytes while the other ares are 8 bytes  
Now this is a single integer in a list which takes 4 + 3 x 8 space and numpy takes oly around 4 bytes space

![img 1](imgsrc/Screenshot%202026-07-05%20103818.png)

#### Takeaway:
* Bcoz numpy uses less space and memory - Faster to read less bytes of memory
* When we are iterating thru each itemn in an numpy array we dont have to do typechecking each time ,so in python built-in list we can have different datatypes in same list bcoz of which at each iteration we have to do type checking for each index value but in numpy we dont need that 
#### Another Reason why numpy is faster (Contiguous Memory)
>Imagine that we have a array like structure and we can store information in its memory blocks  
Now when storing in List the , the memory blocks will be scattered around in the memory and then what the list contains is the pointers pointing towards those values  
Numpy arrays uses contiguous memory soo all memory blocks will be next to each other and all we have to store is where the "start of the memory" is and then "the total size" and the "type of memory block" but easier than pointer structure  

![img2](imgsrc/Screenshot%202026-07-05%20105354.png)

* Now first benefit is that are our CPUs have these SIMD (Single instruction Multiple data) vector processing units  
So like when we have to do the additon of lot of values instead of doing one addition at a time we can use this SIMD vector unit and basically perform and computations on all of these values once at a time
* Another Reason is that we more efficiently utilize our cache so we can quickly load our data efficiently

#### How Are list Diff from numpy

>So we can do Insertion , Deletion , appending , concatenation etc in List but we can do a lot more in "NUMPY"

Example : one thing we can do in numpy is scaler multiplication
![img3](imgsrc/Screenshot%202026-07-05%20105710.png)    

---  

---  
  
  

### Applications of Numpy

* MATLAB kind of things can be done but if we want more math function we can use ----- SCIPY lib

* Useful for plotting useing matplotlib 

* Backend for many Applications like (Pandas , Connect 4 , Digital Photography)

* Obviously Machine Learning :)  
Using tensors and all that 

---

# [Now proceed to 1.ipynb](1.ipynb)

