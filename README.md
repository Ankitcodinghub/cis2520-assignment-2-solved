# cis2520-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CIS2520 Assignment 2 Solved](https://www.ankitcodinghub.com/product/cis2520-assignment-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115168&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CIS2520  Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Changes highlighted in yellow

Summary and Purpose

For this assignment, you will be writing a collection of C functions that operate like arrays. You will use these to understand the underlying properties of arrays, their strengths and weaknesses.

Deliverables

You will be submitting:

1) A file called array.h that contains your function prototypes (see below).

2) A file called array.c that contains your function definitions.

3) A makefile that contains the instructions to compile your code.

Structures for your assignment

You will be working with variables having the following structure which you must declare in your header file.

struct Array

{

unsigned int width; unsigned int nel; unsigned int capacity; void *data;

};

This structure represents an array data structure (our first, and one of the simplest data structures used in this course). The elements of the Array structure are as follows: width represents the size in bytes of each element in the array, nel represents the number of elements currently in the array, capacity represents the total number of elements that can be stored in the array, and data is a pointer to the contents of the array.

Additionally, you will be using the following structure to measure the performance of your code and count the number of memory read, memory write, malloc and free operations.

struct Performance

{ unsigned int reads; unsigned int writes; unsigned int mallocs; unsigned int frees;

};

Basic function prototypes and descriptions for your assignment

struct Performance *newPerformance();

This function will allocate sufficient memory for a Performance structure, set reads, writes, mallocs, and frees to zero (yes, I realize there is technically one malloc in this function) and return the address of the structure. Your function should print an error message to the standard error stream and exit if the malloc function fails.

struct Array *newArray( struct Performance *performance, unsigned int width, unsigned int capacity );

void readItem( struct Performance *performance, struct Array *array, unsigned int index, void *dest );

If index is greater than or equal to array-&gt;nel this function should print an error message to the standard error stream and exit. Otherwise, this function will copy array-&gt;width bytes from the memory address array-&gt;data offset by the index (multiplied by array-&gt;width) to the memory address given by dest. In addition, it should add one to performance-&gt;reads.

void writeItem( struct Performance *performance, struct Array *array, unsigned int index, void *src );

If index exceeds array-&gt;nel or exceeds or equals array-&gt;capacity this function should print an error message to the standard error stream and exit. Otherwise, this function will copy array-&gt;width bytes from the memory address given by src to the memory address array&gt;data offset by the index (multiplied by array-&gt;width). If index exactly equals array-&gt;nel, array-&gt;nel should be incremented by one. In addition, it should add one to performance-

&gt;writes.

void contract( struct Performance *performance, struct Array *array );

If array-&gt;nel==0 this function should print an error message to the standard error stream and exit. Otherwise, it should decrement array-&gt;nel by one.

void freeArray( struct Performance *performance, struct Array *array );

This function will free both array-&gt;data and the array structure itself. And it will increment performance-&gt;frees by one (yes, one).

Derived function prototypes and descriptions for your assignment

The following functions must be implemented by calling the basic functions above (not by interacting with data of the Array structure directly). Error handling will be done by the basic functions.

void appendItem( struct Performance *performance, struct Array *array, void *src );

This function will add an element to the end of the array (i.e. at position array-&gt;nel). It will do this by calling the writeItem function (above).

void insertItem( struct Performance *performance, struct Array *array, unsigned int index, void *src );

This function will use readItem and writeItem calls to move all the elements in the array at the position given by index and higher, one position further back and then write the given data at index in the array.

void prependItem( struct Performance *performance, struct Array *array, void *src );

This function will use insertItem to insert data at position 0.

void deleteItem( struct Performance *performance, struct Array *array, unsigned int index );

This function will use readItem and writeItem calls to move all the elements in the array at the position given by index+1 and higher, one position forward, and then use the contract function to remove the duplicate last entry.

The Last 20%

The above, constitutes 80% of the assignment. If you complete it, you can get a grade up to

80% (Good). The rest of the assignment is more challenging and will allow you to get a grade of 80-90% (Excellent) or 90-100% (Outstanding). Make sure you complete the first part well, before proceeding to the following additional part.

Write the following functions:

int findItem( struct Performance *performance, struct Array *array, int

(*compar)(const void *, const void *), void *target );

This function will retrieve elements from array using readItem (above) starting with the first element in the array and proceeding incrementally. For each element it will apply the compar function to target and the retrieved element. If the compar function returns 0 (indicating a match), this function should return the index of the matching element. If they compar function returns a non-zero value (indicating a mismatch) it should proceed with the next element. If they function processes the entire array without finding a match, it should return a value of -1.

int searchItem( struct Performance *performance, struct Array *array, int

(*compar)(const void *, const void *), void *target );

This function will retrieve elements from array using readItem (above) starting with the middle element in the array rounded down (i.e. if there are 10 elements indexed 0 to 9, it will start with element 4). For each element it will apply the compar function to target and the retrieved element. If the compar function returns 0 (indicating a match), this function should return the index of the matching element. If the compar function returns a value of less than zero (indicating the retrieved element precedes the target) it should repeat the search on all higher indexed elements. If the compar function returns a value of greater than zero (indicating the retrieved element comes after the target) it should repeat the search on all lower indexed elements. If they function processes the final element without finding a match, it should return a value of -1. (This is a binary search.)

You can write additional helper functions as necessary to make sure your code is modular, readable, and easy to modify.

Header File

Testing

You are responsible for testing your code to make sure that it works as required. The

CourseLink web-site will contain some test programs to get you started. However, we will use a different set of test programs to grade your code, so you need to make sure that your code performs according to the instructions above by writing more test code.

Your assignment will be tested on the standard SoCS Virtualbox VM

(http://socs.uoguelph.ca/SoCSVM.zip) which will be run using the Oracle Virtualbox software

(https://www.virtualbox.org/wiki/Downloads). If you are developing in a different environment, you will need to allow yourself enough time to test and debug your code on the target machine. We will NOT test your code on YOUR machine/environment.

Full instructions for using the SoCS Virtualbox VM can be found at: https://wiki.socs.uoguelph.ca/students/socsvm.

Your program must free all the memory that it allocates and not allocate an excess of memory.

Makefile

You will create a makefile that supports the following targets:

all: this target should generate array.o.

clean: this target should delete all .o files.

array.o: this target should create the object file, array.o, by compiling the array.c file.

All compilations and linking must be done with the -Wall -pedantic -std=c99 flags and compile and link without any warnings or errors.

Git

Also, do your own work, do not hire someone to do the work for you.

Grading Rubric

newPerformance 1 newArray 1 readItem 2 writeItem 2 contract 2 freeArray 1 appendItem 2 insertItem 2 prependItem 2 deleteItem 2 style 2 makefile 2

findItem 2 searchItem 2

Total 25

Ask Questions

The instructions above are intended to be as complete and clear as possible. However, it is YOUR responsibility to resolve any ambiguities or confusion about the instructions by asking questions in class, via the discussion forums, or by e-mailing the course e-mail.
