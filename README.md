# MATRIX CALCULATOR

## Usage

`make all`, then `make run`.

## Matrices implementation:

	Matrices can be saved either as dense or sparse.
	Sparse matrix is matrix with more than half elements that are zeroes
	It is represented by map with key being element coordinate and value its value.

	Dense matrix is represented by 2D array.


## Calculator implements:

### Saving matrices to variables:

	Matrices can be assigned to random string variable and later accesed with its name.
	Example:
		scan a 3x3 - scans matrix with name a of dimensions 3x3 from stdin
		print a
		determinant a - prints determinant of matrix with name a
		c = 2 * a
		...
	They can be overwritten or deleted by command delete VAR or delete all, which deletes whole memory

### Matrix operations:

	Matrix addition, subtraction, multiplication
		If matrices have illegal dimensions, exception is thrown. 
		Example:
			c = a + b
			a = a * b

	Matrix multiplication with number
		Example:
			a = 8 * b

	Merge
		Two matrices can be merged together if they have correct dimensions, otherwise exception is thrown.
		They can be merged from side or from bottom. 
		Example:
		c = merge a b bottom  ->  ( 3x3 with 3x3  =  6x3 )

	Cut
		Matrix can be cut to requested dimension
		Input form is: CUT_FROM_H CUT_FROM_W CUT_NEW_H CUT_NEW_W
		Example:
			a = cut a 1 3 3 3

	Gauss Elimination
		Example:
			b = gem a


	Transposition
		Example:
			a = transpose a

	Inverse
		If matrix is not regular, program throws exception.
		Merges singular matrix with selected matrix and uses gauss elimination to find inverse matrix.
		Example:
			b = inverse c
	
	Determinant
		Uses gauss elimination to find determinant by multiplying elements on diagonal.
		Example:
			determinant d

	Rank

		Uses gauss elimination to find rank of matrix
		Example:
			rank c

### Exceptions:

	Program implements two types of exceptions:

		illegalDimensionException - when multiplying incompatibile matrices

		irregularException - when trying to find inverse matrix of irregular matrix, 
		or finding determinant of matrices with other than n x n dimensions



