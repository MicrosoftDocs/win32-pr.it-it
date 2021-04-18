---
title: Trasformazioni di matrici di appendice
description: Questo argomento fornisce una panoramica matematica delle trasformazioni matrici per la grafica 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104567869"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="926fc-103">Appendice: trasformazioni matrice</span><span class="sxs-lookup"><span data-stu-id="926fc-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="926fc-104">Questo argomento fornisce una panoramica matematica delle trasformazioni matrici per la grafica 2D.</span><span class="sxs-lookup"><span data-stu-id="926fc-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="926fc-105">Tuttavia, non è necessario conoscerne la matematica per usare le trasformazioni in Direct2D.</span><span class="sxs-lookup"><span data-stu-id="926fc-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="926fc-106">Leggere questo argomento se si è interessati alla matematica; in caso contrario, è possibile ignorare questo argomento.</span><span class="sxs-lookup"><span data-stu-id="926fc-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="926fc-107">Introduzione alle matrici</span><span class="sxs-lookup"><span data-stu-id="926fc-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="926fc-108">Operazioni Matrix</span><span class="sxs-lookup"><span data-stu-id="926fc-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="926fc-109">Trasformazioni affini</span><span class="sxs-lookup"><span data-stu-id="926fc-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="926fc-110">Trasformazione conversione</span><span class="sxs-lookup"><span data-stu-id="926fc-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="926fc-111">Ridimensionamento della trasformazione</span><span class="sxs-lookup"><span data-stu-id="926fc-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="926fc-112">Rotazione intorno all'origine</span><span class="sxs-lookup"><span data-stu-id="926fc-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="926fc-113">Rotazione intorno a un punto arbitrario</span><span class="sxs-lookup"><span data-stu-id="926fc-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="926fc-114">Trasformazione inclinazione</span><span class="sxs-lookup"><span data-stu-id="926fc-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="926fc-115">Rappresentazione di trasformazioni in Direct2D</span><span class="sxs-lookup"><span data-stu-id="926fc-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="926fc-116">Avanti</span><span class="sxs-lookup"><span data-stu-id="926fc-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="926fc-117">Introduzione alle matrici</span><span class="sxs-lookup"><span data-stu-id="926fc-117">Introduction to Matrices</span></span>

<span data-ttu-id="926fc-118">Una matrice è una matrice rettangolare di numeri reali.</span><span class="sxs-lookup"><span data-stu-id="926fc-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="926fc-119">L' *ordine* della matrice è il numero di righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="926fc-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="926fc-120">Se, ad esempio, la matrice include 3 righe e 2 colonne, l'ordine è 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="926fc-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="926fc-121">Le matrici vengono in genere visualizzate con gli elementi della matrice racchiusi tra parentesi quadre:</span><span class="sxs-lookup"><span data-stu-id="926fc-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![matrice 3 x 2.](images/matrix01.png)

<span data-ttu-id="926fc-123">Notation: una matrice viene designata da una lettera maiuscola.</span><span class="sxs-lookup"><span data-stu-id="926fc-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="926fc-124">Gli elementi sono designati da lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="926fc-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="926fc-125">Gli indici indicano il numero di riga e colonna di un elemento.</span><span class="sxs-lookup"><span data-stu-id="926fc-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="926fc-126">Ad esempio, un *IJ* è l'elemento nella riga volto della e la colonna j'th della matrice a.</span><span class="sxs-lookup"><span data-stu-id="926fc-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="926fc-127">Nel diagramma seguente viene illustrata una matrice i × j con i singoli elementi in ogni cella della matrice.</span><span class="sxs-lookup"><span data-stu-id="926fc-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![matrice con le colonne i Rows e j.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="926fc-129">Operazioni Matrix</span><span class="sxs-lookup"><span data-stu-id="926fc-129">Matrix Operations</span></span>

<span data-ttu-id="926fc-130">In questa sezione vengono descritte le operazioni di base definite nelle matrici.</span><span class="sxs-lookup"><span data-stu-id="926fc-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="926fc-131">*Aggiunta*.</span><span class="sxs-lookup"><span data-stu-id="926fc-131">*Addition*.</span></span> <span data-ttu-id="926fc-132">La somma A + B di due matrici viene ottenuta aggiungendo gli elementi corrispondenti di A e B:</span><span class="sxs-lookup"><span data-stu-id="926fc-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="926fc-133">A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="926fc-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="926fc-134">*Moltiplicazione scalare*.</span><span class="sxs-lookup"><span data-stu-id="926fc-134">*Scalar multiplication*.</span></span> <span data-ttu-id="926fc-135">Questa operazione Moltiplica una matrice per un numero reale.</span><span class="sxs-lookup"><span data-stu-id="926fc-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="926fc-136">Dato un numero reale *k*, il prodotto scalare ka viene ottenuto moltiplicando ogni elemento di a per *k*.</span><span class="sxs-lookup"><span data-stu-id="926fc-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="926fc-137">kA = k \[ a *IJ* \]  =  \[ k × a *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="926fc-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="926fc-138">*Moltiplicazione di matrici*.</span><span class="sxs-lookup"><span data-stu-id="926fc-138">*Matrix multiplication*.</span></span> <span data-ttu-id="926fc-139">Date due matrici A e B con Order (m × n) e (n × p), il prodotto C = A × B è una matrice con Order (m × p), definita come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="926fc-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Mostra una formula per la moltiplicazione di matrici.](images/matrix02.png)

<span data-ttu-id="926fc-141">oppure, in modo equivalente:</span><span class="sxs-lookup"><span data-stu-id="926fc-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="926fc-142">c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="926fc-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="926fc-143">Ovvero per calcolare ogni elemento c *IJ*, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="926fc-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="926fc-144">Prendere la riga volto della di un oggetto e la colonna j'th di B.</span><span class="sxs-lookup"><span data-stu-id="926fc-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="926fc-145">Moltiplica ogni coppia di elementi nella riga e nella colonna: la prima voce di riga dalla prima voce di colonna, la seconda voce di riga per la seconda voce di colonna e così via.</span><span class="sxs-lookup"><span data-stu-id="926fc-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="926fc-146">Sommare il risultato.</span><span class="sxs-lookup"><span data-stu-id="926fc-146">Sum the result.</span></span>

<span data-ttu-id="926fc-147">Di seguito è riportato un esempio di moltiplicazione di una matrice (2 × 2) per una matrice (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="926fc-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![moltiplicazione di matrici.](images/matrix03.png)

<span data-ttu-id="926fc-149">La moltiplicazione di matrici non è commutativa.</span><span class="sxs-lookup"><span data-stu-id="926fc-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="926fc-150">Ovvero, A × B ≠ B × A. Inoltre, dalla definizione segue che non tutte le coppie di matrici possono essere moltiplicate.</span><span class="sxs-lookup"><span data-stu-id="926fc-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="926fc-151">Il numero di colonne nella matrice di sinistra deve essere uguale al numero di righe della matrice a destra.</span><span class="sxs-lookup"><span data-stu-id="926fc-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="926fc-152">In caso contrario, l'operatore × non è definito.</span><span class="sxs-lookup"><span data-stu-id="926fc-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="926fc-153">*Identificare la matrice*.</span><span class="sxs-lookup"><span data-stu-id="926fc-153">*Identify matrix*.</span></span> <span data-ttu-id="926fc-154">Una matrice di identità, designata come, è una matrice quadrata definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="926fc-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="926fc-155">I *IJ* = 1 se *i*  =  *j* o 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="926fc-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="926fc-156">In altre parole, una matrice di identità contiene 1 per ogni elemento in cui il numero di riga è uguale al numero di colonna e zero per tutti gli altri elementi.</span><span class="sxs-lookup"><span data-stu-id="926fc-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="926fc-157">Ecco ad esempio la matrice di identità 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="926fc-157">For example, here is the 3 × 3 identity matrix.</span></span>

![matrice di identità.](images/matrix04.png)

<span data-ttu-id="926fc-159">Le seguenti corrispondenze vengono mantenute per qualsiasi matrice M.</span><span class="sxs-lookup"><span data-stu-id="926fc-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="926fc-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="926fc-160">M x I = M</span></span>  
<span data-ttu-id="926fc-161">I x M = M</span><span class="sxs-lookup"><span data-stu-id="926fc-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="926fc-162">Trasformazioni affini</span><span class="sxs-lookup"><span data-stu-id="926fc-162">Affine Transforms</span></span>

<span data-ttu-id="926fc-163">Una *trasformazione affine* è un'operazione matematica che esegue il mapping di uno spazio delle coordinate a un altro.</span><span class="sxs-lookup"><span data-stu-id="926fc-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="926fc-164">In altre parole, esegue il mapping di un set di punti a un altro set di punti.</span><span class="sxs-lookup"><span data-stu-id="926fc-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="926fc-165">Le trasformazioni affini includono alcune funzionalità che le rendono utili nella grafica del computer.</span><span class="sxs-lookup"><span data-stu-id="926fc-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="926fc-166">Le trasformazioni affini mantengono *collinearità*.</span><span class="sxs-lookup"><span data-stu-id="926fc-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="926fc-167">Se tre o più punti rientrino in una riga, formano comunque una riga dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="926fc-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="926fc-168">Le linee rette rimangono diritte.</span><span class="sxs-lookup"><span data-stu-id="926fc-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="926fc-169">La composizione di due trasformazioni affini è una trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="926fc-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="926fc-170">Le trasformazioni affini per lo spazio 2D hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-170">Affine transforms for 2-D space have the following form.</span></span>

![Mostra una trasformazione affine per lo spazio 2D.](images/matrix05.png)

<span data-ttu-id="926fc-172">Se si applica la definizione della moltiplicazione di matrici fornita in precedenza, è possibile indicare che il prodotto di due trasformazioni affini è un'altra trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="926fc-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="926fc-173">Per trasformare un punto 2D utilizzando una trasformazione affine, il punto viene rappresentato come una matrice 1 × 3.</span><span class="sxs-lookup"><span data-stu-id="926fc-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="926fc-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="926fc-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="926fc-175">I primi due elementi contengono le coordinate x e y del punto.</span><span class="sxs-lookup"><span data-stu-id="926fc-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="926fc-176">1 viene inserito nel terzo elemento per far funzionare correttamente la matematica.</span><span class="sxs-lookup"><span data-stu-id="926fc-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="926fc-177">Per applicare la trasformazione, moltiplicare le due matrici come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="926fc-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="926fc-178">P ' = P × M</span><span class="sxs-lookup"><span data-stu-id="926fc-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="926fc-179">In questo modo si espande il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-179">This expands to the following.</span></span>

![trasformazione affine.](images/matrix06.png)

<span data-ttu-id="926fc-181">dove</span><span class="sxs-lookup"><span data-stu-id="926fc-181">where</span></span>

<dl> <span data-ttu-id="926fc-182">x ' = ax + CY + e</span><span class="sxs-lookup"><span data-stu-id="926fc-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="926fc-183">y ' = BX + DY + f</span><span class="sxs-lookup"><span data-stu-id="926fc-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="926fc-184">Per ottenere il punto trasformato, prendere i primi due elementi della matrice P.</span><span class="sxs-lookup"><span data-stu-id="926fc-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="926fc-185">p = (x ', y ') = (AX + CY + e, BX + DY + f)</span><span class="sxs-lookup"><span data-stu-id="926fc-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="926fc-186">Una matrice da 1 × *n* viene chiamata *vettore di riga*.</span><span class="sxs-lookup"><span data-stu-id="926fc-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="926fc-187">Direct2D e Direct3D utilizzano entrambi vettori di riga per rappresentare punti nello spazio 2D o 3D.</span><span class="sxs-lookup"><span data-stu-id="926fc-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="926fc-188">È possibile ottenere un risultato equivalente usando un vettore di colonna (*n* × 1) e trasponendo la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="926fc-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="926fc-189">La maggior parte dei testi grafici usa il formato vettoriale di colonna.</span><span class="sxs-lookup"><span data-stu-id="926fc-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="926fc-190">In questo argomento viene presentato il formato vettoriale di riga per coerenza con Direct2D e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="926fc-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="926fc-191">Le varie sezioni successive derivano le trasformazioni di base.</span><span class="sxs-lookup"><span data-stu-id="926fc-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="926fc-192">Trasformazione conversione</span><span class="sxs-lookup"><span data-stu-id="926fc-192">Translation Transform</span></span>

<span data-ttu-id="926fc-193">Il formato della matrice di trasformazione della traduzione è il seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-193">The translation transform matrix has the following form.</span></span>

![trasformazione conversione.](images/matrix07.png)

<span data-ttu-id="926fc-195">L'inserimento di un punto *P* in questa equazione produce:</span><span class="sxs-lookup"><span data-stu-id="926fc-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="926fc-196">P ' = (*x*  +  *DX*, *y*  +  *dy*)</span><span class="sxs-lookup"><span data-stu-id="926fc-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="926fc-197">che corrisponde al punto (x, y) tradotto da *dx* nell'asse x e *dy* nell'asse y.</span><span class="sxs-lookup"><span data-stu-id="926fc-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![diagramma che mostra la conversione di due punti.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="926fc-199">Ridimensionamento della trasformazione</span><span class="sxs-lookup"><span data-stu-id="926fc-199">Scaling Transform</span></span>

<span data-ttu-id="926fc-200">Il formato della matrice di trasformazione di ridimensionamento è il seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-200">The scaling transform matrix has the following form.</span></span>

![ridimensionamento della trasformazione.](images/matrix09.png)

<span data-ttu-id="926fc-202">L'inserimento di un punto *P* in questa equazione produce:</span><span class="sxs-lookup"><span data-stu-id="926fc-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="926fc-203">P ' = (*x* ∙ *DX*, *y* ∙ *dy*)</span><span class="sxs-lookup"><span data-stu-id="926fc-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="926fc-204">che corrisponde al punto (x, y) ridimensionato da *dx* e *dy*.</span><span class="sxs-lookup"><span data-stu-id="926fc-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![diagramma che mostra il ridimensionamento di due punti.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="926fc-206">Rotazione intorno all'origine</span><span class="sxs-lookup"><span data-stu-id="926fc-206">Rotation Around the Origin</span></span>

<span data-ttu-id="926fc-207">La matrice per ruotare un punto intorno all'origine ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Mostra una formula per una trasformazione di rotazione.](images/matrix11.png)

<span data-ttu-id="926fc-209">Il punto trasformato è:</span><span class="sxs-lookup"><span data-stu-id="926fc-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="926fc-210">P ' = (*x* CosΘ – ysinΘ, *x* sinθ + *y* cosΘ)</span><span class="sxs-lookup"><span data-stu-id="926fc-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="926fc-211">Prova.</span><span class="sxs-lookup"><span data-stu-id="926fc-211">Proof.</span></span> <span data-ttu-id="926fc-212">Per mostrare che P ' rappresenta una rotazione, prendere in considerazione il diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![diagramma che mostra la rotazione intorno all'origine.](images/graphics24.png)

<span data-ttu-id="926fc-214">Si consideri quanto segue:</span><span class="sxs-lookup"><span data-stu-id="926fc-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="926fc-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="926fc-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="926fc-216">Punto originale da trasformare.</span><span class="sxs-lookup"><span data-stu-id="926fc-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="926fc-217">Φ</span><span class="sxs-lookup"><span data-stu-id="926fc-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="926fc-218">Angolo formato dalla riga (0, 0) a P.</span><span class="sxs-lookup"><span data-stu-id="926fc-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="926fc-219">Θ</span><span class="sxs-lookup"><span data-stu-id="926fc-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="926fc-220">Angolo in base al quale ruotare (x, y) sull'origine.</span><span class="sxs-lookup"><span data-stu-id="926fc-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="926fc-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')</span><span class="sxs-lookup"><span data-stu-id="926fc-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="926fc-222">Punto trasformato.</span><span class="sxs-lookup"><span data-stu-id="926fc-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="926fc-223"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="926fc-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="926fc-224">Lunghezza della riga (da 0, 0) a P. Anche il raggio del cerchio di rotazione.</span><span class="sxs-lookup"><span data-stu-id="926fc-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="926fc-225">Questo diagramma usa il sistema di coordinate standard usato in geometria, in cui l'asse y positivo punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="926fc-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="926fc-226">Direct2D utilizza il sistema di coordinate di Windows, in cui l'asse y positivo punta verso il basso.</span><span class="sxs-lookup"><span data-stu-id="926fc-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="926fc-227">L'angolo tra l'asse x e la riga (0, 0) a P ' è Φ + Θ.</span><span class="sxs-lookup"><span data-stu-id="926fc-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="926fc-228">Le seguenti identità contengono:</span><span class="sxs-lookup"><span data-stu-id="926fc-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="926fc-229">x = cosΦ R</span><span class="sxs-lookup"><span data-stu-id="926fc-229">x = R cosΦ</span></span>  
<span data-ttu-id="926fc-230">y = R sinΦ</span><span class="sxs-lookup"><span data-stu-id="926fc-230">y = R sinΦ</span></span>  
<span data-ttu-id="926fc-231">x ' = R cos (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="926fc-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="926fc-232">y ' = peccato R (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="926fc-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="926fc-233">A questo punto, risolvere per x "e y" in termini di Θ.</span><span class="sxs-lookup"><span data-stu-id="926fc-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="926fc-234">Per le formule di addizione trigonometrica:</span><span class="sxs-lookup"><span data-stu-id="926fc-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="926fc-235">x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ-RsinΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="926fc-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="926fc-236">y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="926fc-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="926fc-237">Sostituendo, si ottengono:</span><span class="sxs-lookup"><span data-stu-id="926fc-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="926fc-238">x ' = xcosΘ – ysinΘ</span><span class="sxs-lookup"><span data-stu-id="926fc-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="926fc-239">y ' = xsinΘ + ycosΘ</span><span class="sxs-lookup"><span data-stu-id="926fc-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="926fc-240">che corrisponde al punto di trasformazione P ' illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="926fc-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="926fc-241">Rotazione intorno a un punto arbitrario</span><span class="sxs-lookup"><span data-stu-id="926fc-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="926fc-242">Per ruotare intorno a un punto (x, y) diverso dall'origine, viene utilizzata la matrice seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![trasformazione di rotazione.](images/matrix13.png)

<span data-ttu-id="926fc-244">È possibile derivare questa matrice prendendo il punto (x, y) come origine.</span><span class="sxs-lookup"><span data-stu-id="926fc-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![diagramma che mostra la rotazione intorno a un punto.](images/graphics25.png)

<span data-ttu-id="926fc-246">Let (x1, Y1) è il punto risultante dalla rotazione del punto (x0, y0) intorno al punto (x, y).</span><span class="sxs-lookup"><span data-stu-id="926fc-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="926fc-247">È possibile derivare X1 come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="926fc-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="926fc-248">X1 = (x0 – x) cosΘ – (y0-y) sinΘ + x</span><span class="sxs-lookup"><span data-stu-id="926fc-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="926fc-249">X1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span><span class="sxs-lookup"><span data-stu-id="926fc-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="926fc-250">A questo punto, ricollegare questa equazione alla matrice di trasformazione, usando la formula X1 = aX0 + cy0 + e riportata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="926fc-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="926fc-251">Utilizzare la stessa procedura per derivare Y1.</span><span class="sxs-lookup"><span data-stu-id="926fc-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="926fc-252">Trasformazione inclinazione</span><span class="sxs-lookup"><span data-stu-id="926fc-252">Skew Transform</span></span>

<span data-ttu-id="926fc-253">La trasformazione asimmetria viene definita da quattro parametri:</span><span class="sxs-lookup"><span data-stu-id="926fc-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="926fc-254">Θ: la quantità di inclinazione lungo l'asse x, misurata come un angolo dall'asse y.</span><span class="sxs-lookup"><span data-stu-id="926fc-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="926fc-255">Φ: la quantità da inclinare lungo l'asse y, misurata come un angolo dall'asse x.</span><span class="sxs-lookup"><span data-stu-id="926fc-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="926fc-256">(*px*, *py*): coordinate x e y del punto in cui viene eseguita l'asimmetria.</span><span class="sxs-lookup"><span data-stu-id="926fc-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="926fc-257">La trasformazione inclinazione utilizza la matrice seguente.</span><span class="sxs-lookup"><span data-stu-id="926fc-257">The skew transform uses the following matrix.</span></span>

![trasformazione asimmetria.](images/matrix14.png)

<span data-ttu-id="926fc-259">Il punto trasformato è:</span><span class="sxs-lookup"><span data-stu-id="926fc-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="926fc-260">P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ</span><span class="sxs-lookup"><span data-stu-id="926fc-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="926fc-261">o equivalente:</span><span class="sxs-lookup"><span data-stu-id="926fc-261">or equivalently:</span></span>

<dl> <span data-ttu-id="926fc-262">P ' = (*x* + (*y* - *py*) tanΘ, *y* + (*x* - *px*) tanΦ)</span><span class="sxs-lookup"><span data-stu-id="926fc-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="926fc-263">Per verificare il funzionamento di questa trasformazione, considerare ogni singolo componente.</span><span class="sxs-lookup"><span data-stu-id="926fc-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="926fc-264">Il parametro Θ sposta ogni punto della direzione x di un importo uguale a tanΘ.</span><span class="sxs-lookup"><span data-stu-id="926fc-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="926fc-265">Nel diagramma seguente viene illustrata la relazione tra Θ e l'inclinazione dell'asse x.</span><span class="sxs-lookup"><span data-stu-id="926fc-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Diagramma che mostra l'inclinazione lungo l'asse x.](images/graphics26.png)

<span data-ttu-id="926fc-267">Di seguito è illustrata la stessa asimmetria applicata a un rettangolo:</span><span class="sxs-lookup"><span data-stu-id="926fc-267">Here is the same skew applied to a rectangle:</span></span>

![Diagramma che mostra l'inclinazione lungo l'asse x quando viene applicato a un rettangolo.](images/graphics27.png)

<span data-ttu-id="926fc-269">Il parametro Φ ha lo stesso effetto, ma lungo l'asse y:</span><span class="sxs-lookup"><span data-stu-id="926fc-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Diagramma che mostra l'inclinazione lungo l'asse y.](images/graphics28.png)

<span data-ttu-id="926fc-271">Il diagramma seguente mostra l'inclinazione dell'asse y applicata a un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="926fc-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Diagramma che mostra la distorsione lungo l'asse y quando viene applicato a un rettangolo.](images/graphics29.png)

<span data-ttu-id="926fc-273">Infine, i parametri *px* e *py* spostano il punto centrale per la distorsione lungo gli assi x e y.</span><span class="sxs-lookup"><span data-stu-id="926fc-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="926fc-274">Rappresentazione di trasformazioni in Direct2D</span><span class="sxs-lookup"><span data-stu-id="926fc-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="926fc-275">Tutte le trasformazioni Direct2D sono trasformazioni affini.</span><span class="sxs-lookup"><span data-stu-id="926fc-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="926fc-276">Direct2D non supporta le trasformazioni non affini.</span><span class="sxs-lookup"><span data-stu-id="926fc-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="926fc-277">Le trasformazioni sono rappresentate dalla struttura [**d2d1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) .</span><span class="sxs-lookup"><span data-stu-id="926fc-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="926fc-278">Questa struttura definisce una matrice di 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="926fc-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="926fc-279">Poiché la terza colonna di una trasformazione affine è sempre la stessa ( \[ 0, 0, 1 \] ) e perché Direct2D non supporta le trasformazioni non affini, non è necessario specificare l'intera matrice 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="926fc-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="926fc-280">Internamente, Direct2D USA 3 × 3 matrici per calcolare le trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="926fc-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="926fc-281">I membri della [**matrice d2d1 \_ \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) sono denominati in base alla posizione di indice: il membro **\_ 11** è elemento (1,1), il **\_ 12** membro è elemento (1,2) e così via.</span><span class="sxs-lookup"><span data-stu-id="926fc-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="926fc-282">Sebbene sia possibile inizializzare direttamente i membri della struttura, è consigliabile usare la classe [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="926fc-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="926fc-283">Questa classe eredita **d2d1 \_ Matrix \_ 3x2 \_ F** e fornisce metodi helper per la creazione di una delle trasformazioni affini di base.</span><span class="sxs-lookup"><span data-stu-id="926fc-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="926fc-284">La classe definisce anche [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la composizione di due o più trasformazioni, come descritto in [applicazione di trasformazioni in Direct2D](applying-transforms-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="926fc-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="926fc-285">Prossima</span><span class="sxs-lookup"><span data-stu-id="926fc-285">Next</span></span>

[<span data-ttu-id="926fc-286">Modulo 4. Input utente</span><span class="sxs-lookup"><span data-stu-id="926fc-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 