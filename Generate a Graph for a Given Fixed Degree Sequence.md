# Ex. No: 17A - Generate a Graph for a Given Fixed Degree Sequence

## AIM:
To write a Python program to generate a graph for a given **fixed degree sequence**.

## ALGORITHM:

**Step 1**: Start the program.

**Step 2**: Check if the sum of the degree sequence is even.  
> (A necessary condition for the sequence to be graphical.)

- If not even, print an error message and exit the program.

**Step 3**: Use the **Havel-Hakimi algorithm** to determine whether a simple graph can be constructed from the sequence, and to generate the graph.

**Step 4**: If the graph is successfully created, **visualize it** using a graph drawing function (e.g., `networkx.draw()`).

**Step 5**: End the program.

## PYTHON PROGRAM

```

#Reg.no 212222060280
#Name Trisha S

def printMat(degseq, n):
	mat = [[0] * n for i in range(n)]
	for i in range(n):
		for j in range(i + 1, n):
			if (degseq[i] > 0 and degseq[j] > 0):
				degseq[i] -= 1
				degseq[j] -= 1
				mat[i][j] = 1
				mat[j][i] = 1
	print("      ", end ="")
	for i in range(n):
		print(" ", "(", i, ")", end ="")
	print()
	print()
	for i in range(n):
		print("  ", "(", i, ")", end = " ")
		for j in range(n):
			print("  ", mat[i][j], end = " ")
		print()
degseq=[]
for i in range(0, 5):
    ele = int(input())
    degseq.append(ele)
n = len(degseq)
printMat(degseq, n)


```

## OUTPUT
<img width="1201" height="271" alt="Screenshot 2025-11-10 180911" src="https://github.com/user-attachments/assets/d31f893c-3491-4a5a-b0ab-8e610e00a3b8" />

```

## RESULT
Thus the Python program to generate a graph for a given **fixed degree sequence** is executed successfully.
