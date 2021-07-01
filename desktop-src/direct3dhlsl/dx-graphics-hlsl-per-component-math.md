---
title: Per-Component operazioni matematiche
description: Con HLSL è possibile programmare shader a livello di algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c8c9eeea1072c53915588ac0099998e76c0452a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119596"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="1187e-103">Per-Component operazioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1187e-103">Per-Component Math Operations</span></span>

<span data-ttu-id="1187e-104">Con HLSL è possibile programmare shader a livello di algoritmo.</span><span class="sxs-lookup"><span data-stu-id="1187e-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="1187e-105">Per comprendere il linguaggio, è necessario sapere come dichiarare variabili e funzioni, usare funzioni intrinseche, definire tipi di dati personalizzati e usare la semantica per connettere argomenti shader ad altri shader e alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1187e-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="1187e-106">Dopo aver appreso come creare shader in HLSL, è necessario acquisire informazioni sulle chiamate API in modo da poter compilare uno shader per hardware specifico, inizializzare le costanti dello shader e inizializzare altri stati della pipeline, se necessario.</span><span class="sxs-lookup"><span data-stu-id="1187e-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="1187e-107">Tipo di vettore</span><span class="sxs-lookup"><span data-stu-id="1187e-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="1187e-108">Tipo di matrice</span><span class="sxs-lookup"><span data-stu-id="1187e-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="1187e-109">Ordinamento delle matrici</span><span class="sxs-lookup"><span data-stu-id="1187e-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="1187e-110">esempi</span><span class="sxs-lookup"><span data-stu-id="1187e-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="1187e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1187e-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="1187e-112">Tipo di vettore</span><span class="sxs-lookup"><span data-stu-id="1187e-112">The Vector Type</span></span>

<span data-ttu-id="1187e-113">Un vettore è una struttura di dati che contiene tra uno e quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="1187e-114">L'intero immediatamente successivo al tipo di dati è il numero di componenti nel vettore.</span><span class="sxs-lookup"><span data-stu-id="1187e-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="1187e-115">Gli inizializzatori possono anche essere inclusi nelle dichiarazioni.</span><span class="sxs-lookup"><span data-stu-id="1187e-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="1187e-116">In alternativa, il tipo di vettore può essere usato per creare le stesse dichiarazioni:</span><span class="sxs-lookup"><span data-stu-id="1187e-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="1187e-117">Il tipo di vettore usa parentesi angolari per specificare il tipo e il numero di componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="1187e-118">I vettori contengono fino a quattro componenti, ognuno dei quali è accessibile usando uno dei due set di denominazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="1187e-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="1187e-119">Posizione impostata: x,y,z,w</span><span class="sxs-lookup"><span data-stu-id="1187e-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="1187e-120">Set di colori: r,g,b,a</span><span class="sxs-lookup"><span data-stu-id="1187e-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="1187e-121">Entrambe queste istruzioni restituiscono il valore nel terzo componente.</span><span class="sxs-lookup"><span data-stu-id="1187e-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="1187e-122">I set di denominazione possono usare uno o più componenti, ma non possono essere misti.</span><span class="sxs-lookup"><span data-stu-id="1187e-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="1187e-123">La specifica di uno o più componenti vettoriali durante la lettura dei componenti è detta swizzling.</span><span class="sxs-lookup"><span data-stu-id="1187e-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="1187e-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1187e-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="1187e-125">La maschera controlla il numero di componenti scritti.</span><span class="sxs-lookup"><span data-stu-id="1187e-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="1187e-126">Le assegnazioni non possono essere scritte nello stesso componente più di una volta.</span><span class="sxs-lookup"><span data-stu-id="1187e-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="1187e-127">Il lato sinistro di questa istruzione non è quindi valido:</span><span class="sxs-lookup"><span data-stu-id="1187e-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="1187e-128">Inoltre, gli spazi dei nomi dei componenti non possono essere misti.</span><span class="sxs-lookup"><span data-stu-id="1187e-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="1187e-129">Si tratta di un componente non valido:</span><span class="sxs-lookup"><span data-stu-id="1187e-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="1187e-130">L'accesso a un vettore come scalare accederà al primo componente del vettore.</span><span class="sxs-lookup"><span data-stu-id="1187e-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="1187e-131">Le due istruzioni seguenti sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="1187e-132">Tipo di matrice</span><span class="sxs-lookup"><span data-stu-id="1187e-132">The Matrix Type</span></span>

<span data-ttu-id="1187e-133">Una matrice è una struttura di dati che contiene righe e colonne di dati.</span><span class="sxs-lookup"><span data-stu-id="1187e-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="1187e-134">I dati possono essere di qualsiasi tipo scalare, tuttavia, ogni elemento di una matrice è dello stesso tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="1187e-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="1187e-135">Il numero di righe e colonne viene specificato con la stringa riga per colonna aggiunta al tipo di dati .</span><span class="sxs-lookup"><span data-stu-id="1187e-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



<span data-ttu-id="1187e-136">Il numero massimo di righe o colonne è 4. il numero minimo è 1.</span><span class="sxs-lookup"><span data-stu-id="1187e-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="1187e-137">Una matrice può essere inizializzata quando viene dichiarata:</span><span class="sxs-lookup"><span data-stu-id="1187e-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="1187e-138">In caso contrario, il tipo di matrice può essere usato per creare le stesse dichiarazioni:</span><span class="sxs-lookup"><span data-stu-id="1187e-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="1187e-139">Il tipo matrice usa le parentesi angolari per specificare il tipo, il numero di righe e il numero di colonne.</span><span class="sxs-lookup"><span data-stu-id="1187e-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="1187e-140">In questo esempio viene creata una matrice a virgola mobile, con due righe e due colonne.</span><span class="sxs-lookup"><span data-stu-id="1187e-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="1187e-141">È possibile usare qualsiasi tipo di dati scalare.</span><span class="sxs-lookup"><span data-stu-id="1187e-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="1187e-142">Questa dichiarazione definisce una matrice di valori float (numeri a virgola mobile a 32 bit) con due righe e tre colonne:</span><span class="sxs-lookup"><span data-stu-id="1187e-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="1187e-143">Una matrice contiene valori organizzati in righe e colonne, a cui è possibile accedere usando l'operatore di struttura "." seguito da uno dei due set di denominazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="1187e-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="1187e-144">Posizione della colonna di riga in base zero:</span><span class="sxs-lookup"><span data-stu-id="1187e-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="1187e-145">\_m00, \_ m01, \_ m02, \_ m03</span><span class="sxs-lookup"><span data-stu-id="1187e-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="1187e-146">\_m10, \_ m11, \_ m12, \_ m13</span><span class="sxs-lookup"><span data-stu-id="1187e-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="1187e-147">\_m20, \_ m21, \_ m22, \_ m23</span><span class="sxs-lookup"><span data-stu-id="1187e-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="1187e-148">\_m30, \_ m31, \_ m32, \_ m33</span><span class="sxs-lookup"><span data-stu-id="1187e-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="1187e-149">Posizione della colonna di riga in base uno:</span><span class="sxs-lookup"><span data-stu-id="1187e-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="1187e-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="1187e-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="1187e-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="1187e-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="1187e-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="1187e-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="1187e-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="1187e-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="1187e-154">Ogni set di denominazione inizia con un carattere di sottolineatura seguito dal numero di riga e dal numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="1187e-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="1187e-155">La convenzione in base zero include anche la lettera "m" prima del numero di riga e colonna.</span><span class="sxs-lookup"><span data-stu-id="1187e-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="1187e-156">Ecco un esempio che usa i due set di denominazione per accedere a una matrice:</span><span class="sxs-lookup"><span data-stu-id="1187e-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



<span data-ttu-id="1187e-157">Analogamente ai vettori, i set di denominazione possono usare uno o più componenti di entrambi i set di denominazione.</span><span class="sxs-lookup"><span data-stu-id="1187e-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



<span data-ttu-id="1187e-158">È anche possibile accedere a una matrice usando la notazione di accesso alla matrice, ovvero un set di indici in base zero.</span><span class="sxs-lookup"><span data-stu-id="1187e-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="1187e-159">Ogni indice è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="1187e-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="1187e-160">È possibile accedere a una matrice 4x4 con gli indici seguenti:</span><span class="sxs-lookup"><span data-stu-id="1187e-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="1187e-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1187e-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="1187e-162">\[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1187e-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="1187e-163">\[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1187e-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="1187e-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1187e-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="1187e-165">Di seguito è riportato un esempio di accesso a una matrice:</span><span class="sxs-lookup"><span data-stu-id="1187e-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="1187e-166">Si noti che l'operatore di struttura "." non viene usato per accedere a una matrice.</span><span class="sxs-lookup"><span data-stu-id="1187e-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="1187e-167">La notazione di accesso alle matrici non può usare lo swizzling per leggere più di un componente.</span><span class="sxs-lookup"><span data-stu-id="1187e-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="1187e-168">Tuttavia, l'accesso alle matrici può leggere un vettore a più componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="1187e-169">Come per i vettori, la lettura di più componenti della matrice è detta swizzling.</span><span class="sxs-lookup"><span data-stu-id="1187e-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="1187e-170">È possibile assegnare più componenti, presupponendo che sia usato solo uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1187e-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="1187e-171">Queste sono tutte assegnazioni valide:</span><span class="sxs-lookup"><span data-stu-id="1187e-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="1187e-172">La maschera controlla il numero di componenti scritti.</span><span class="sxs-lookup"><span data-stu-id="1187e-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="1187e-173">Le assegnazioni non possono essere scritte nello stesso componente più di una volta.</span><span class="sxs-lookup"><span data-stu-id="1187e-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="1187e-174">Il lato sinistro di questa istruzione non è quindi valido:</span><span class="sxs-lookup"><span data-stu-id="1187e-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="1187e-175">Inoltre, gli spazi dei nomi dei componenti non possono essere misti.</span><span class="sxs-lookup"><span data-stu-id="1187e-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="1187e-176">Si tratta di un componente non valido:</span><span class="sxs-lookup"><span data-stu-id="1187e-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="1187e-177">Ordinamento delle matrici</span><span class="sxs-lookup"><span data-stu-id="1187e-177">Matrix Ordering</span></span>

<span data-ttu-id="1187e-178">L'ordine di tabulazione della matrice per i parametri uniformi è impostato su column-major per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1187e-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="1187e-179">Ciò significa che ogni colonna della matrice viene archiviata in un singolo registro costante.</span><span class="sxs-lookup"><span data-stu-id="1187e-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="1187e-180">D'altra parte, una matrice row-major racchiude ogni riga della matrice in un singolo registro costante.</span><span class="sxs-lookup"><span data-stu-id="1187e-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="1187e-181">La creazione di una matrice può essere modificata con la **\# direttiva pragmapack \_ matrix** o con la parola chiave **row \_ major** o **column \_ major.**</span><span class="sxs-lookup"><span data-stu-id="1187e-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="1187e-182">I dati in una matrice vengono caricati nei registri costanti dello shader prima dell'esecuzione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="1187e-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="1187e-183">Esistono due opzioni per la modalità di lettura dei dati della matrice: nell'ordine delle righe principali o nell'ordine delle colonne principali.</span><span class="sxs-lookup"><span data-stu-id="1187e-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="1187e-184">L'ordine delle colonne principali indica che ogni colonna della matrice verrà archiviata in un singolo registro costante e l'ordine delle righe principali indica che ogni riga della matrice verrà archiviata in un unico registro costante.</span><span class="sxs-lookup"><span data-stu-id="1187e-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="1187e-185">Si tratta di una considerazione importante per il numero di registri costanti usati per una matrice.</span><span class="sxs-lookup"><span data-stu-id="1187e-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="1187e-186">Una matrice principale di riga è strutturata come la seguente:</span><span class="sxs-lookup"><span data-stu-id="1187e-186">A row-major matrix is laid out like the following:</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="1187e-187">11</span><span class="sxs-lookup"><span data-stu-id="1187e-187">11</span></span><br/>
        <span data-ttu-id="1187e-188">21</span><span class="sxs-lookup"><span data-stu-id="1187e-188">21</span></span><br/>
        <span data-ttu-id="1187e-189">31</span><span class="sxs-lookup"><span data-stu-id="1187e-189">31</span></span><br/>
        <span data-ttu-id="1187e-190">41</span><span class="sxs-lookup"><span data-stu-id="1187e-190">41</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-191">12</span><span class="sxs-lookup"><span data-stu-id="1187e-191">12</span></span><br/>
        <span data-ttu-id="1187e-192">22</span><span class="sxs-lookup"><span data-stu-id="1187e-192">22</span></span><br/>
        <span data-ttu-id="1187e-193">32</span><span class="sxs-lookup"><span data-stu-id="1187e-193">32</span></span><br/>
        <span data-ttu-id="1187e-194">42</span><span class="sxs-lookup"><span data-stu-id="1187e-194">42</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-195">13</span><span class="sxs-lookup"><span data-stu-id="1187e-195">13</span></span><br/>
        <span data-ttu-id="1187e-196">23</span><span class="sxs-lookup"><span data-stu-id="1187e-196">23</span></span><br/>
        <span data-ttu-id="1187e-197">33</span><span class="sxs-lookup"><span data-stu-id="1187e-197">33</span></span><br/>
        <span data-ttu-id="1187e-198">43</span><span class="sxs-lookup"><span data-stu-id="1187e-198">43</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-199">14</span><span class="sxs-lookup"><span data-stu-id="1187e-199">14</span></span><br/>
        <span data-ttu-id="1187e-200">24</span><span class="sxs-lookup"><span data-stu-id="1187e-200">24</span></span><br/>
        <span data-ttu-id="1187e-201">34</span><span class="sxs-lookup"><span data-stu-id="1187e-201">34</span></span><br/>
        <span data-ttu-id="1187e-202">44</span><span class="sxs-lookup"><span data-stu-id="1187e-202">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="1187e-203">Una matrice di colonne principali è strutturata come segue:</span><span class="sxs-lookup"><span data-stu-id="1187e-203">A column-major matrix is laid out like the following:</span></span>


:::row:::
    :::column:::
        <span data-ttu-id="1187e-204">11</span><span class="sxs-lookup"><span data-stu-id="1187e-204">11</span></span><br/>
        <span data-ttu-id="1187e-205">12</span><span class="sxs-lookup"><span data-stu-id="1187e-205">12</span></span><br/>
        <span data-ttu-id="1187e-206">13</span><span class="sxs-lookup"><span data-stu-id="1187e-206">13</span></span><br/>
        <span data-ttu-id="1187e-207">14</span><span class="sxs-lookup"><span data-stu-id="1187e-207">14</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-208">21</span><span class="sxs-lookup"><span data-stu-id="1187e-208">21</span></span><br/>
        <span data-ttu-id="1187e-209">22</span><span class="sxs-lookup"><span data-stu-id="1187e-209">22</span></span><br/>
        <span data-ttu-id="1187e-210">23</span><span class="sxs-lookup"><span data-stu-id="1187e-210">23</span></span><br/>
        <span data-ttu-id="1187e-211">24</span><span class="sxs-lookup"><span data-stu-id="1187e-211">24</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-212">31</span><span class="sxs-lookup"><span data-stu-id="1187e-212">31</span></span><br/>
        <span data-ttu-id="1187e-213">32</span><span class="sxs-lookup"><span data-stu-id="1187e-213">32</span></span><br/>
        <span data-ttu-id="1187e-214">33</span><span class="sxs-lookup"><span data-stu-id="1187e-214">33</span></span><br/>
        <span data-ttu-id="1187e-215">34</span><span class="sxs-lookup"><span data-stu-id="1187e-215">34</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1187e-216">14</span><span class="sxs-lookup"><span data-stu-id="1187e-216">14</span></span><br/>
        <span data-ttu-id="1187e-217">24</span><span class="sxs-lookup"><span data-stu-id="1187e-217">24</span></span><br/>
        <span data-ttu-id="1187e-218">34</span><span class="sxs-lookup"><span data-stu-id="1187e-218">34</span></span><br/>
        <span data-ttu-id="1187e-219">44</span><span class="sxs-lookup"><span data-stu-id="1187e-219">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="1187e-220">L'ordinamento delle matrici row-major e column-major determina l'ordine in cui i componenti della matrice vengono letti dagli input dello shader.</span><span class="sxs-lookup"><span data-stu-id="1187e-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="1187e-221">Dopo che i dati sono stati scritti in registri costanti, l'ordine della matrice non ha alcun effetto sul modo in cui i dati vengono usati o accessibili dal codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="1187e-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="1187e-222">Inoltre, le matrici dichiarate in un corpo dello shader non vengono suddivise in registri costanti.</span><span class="sxs-lookup"><span data-stu-id="1187e-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="1187e-223">L'ordine di tabulazione delle righe principale e della colonna non influisce sull'ordine di creazione dei costruttori( che segue sempre l'ordinamento principale delle righe).</span><span class="sxs-lookup"><span data-stu-id="1187e-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="1187e-224">L'ordine dei dati in una matrice può essere dichiarato in fase di compilazione oppure il compilatore ordinerà i dati in fase di esecuzione per un uso più efficiente.</span><span class="sxs-lookup"><span data-stu-id="1187e-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="1187e-225">Esempio</span><span class="sxs-lookup"><span data-stu-id="1187e-225">Examples</span></span>

<span data-ttu-id="1187e-226">HLSL usa due tipi speciali, un tipo vettore e un tipo matrice per semplificare la programmazione della grafica 2D e 3D.</span><span class="sxs-lookup"><span data-stu-id="1187e-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="1187e-227">Ognuno di questi tipi contiene più di un componente. un vettore contiene fino a quattro componenti e una matrice contiene fino a 16 componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="1187e-228">Quando vettori e matrici vengono usati nelle equazioni HLSL standard, i calcoli matematici eseguiti sono progettati per funzionare in base al componente.</span><span class="sxs-lookup"><span data-stu-id="1187e-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="1187e-229">Ad esempio, HLSL implementa questa moltiplicazione:</span><span class="sxs-lookup"><span data-stu-id="1187e-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="1187e-230">come moltiplicazione di quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-230">as a four-component multiply.</span></span> <span data-ttu-id="1187e-231">Il risultato è quattro scalari:</span><span class="sxs-lookup"><span data-stu-id="1187e-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="1187e-232">Si tratta di quattro moltiplicazioni in cui ogni risultato viene archiviato in un componente separato di v.</span><span class="sxs-lookup"><span data-stu-id="1187e-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="1187e-233">Questa operazione è detta moltiplicazione di quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="1187e-233">This is called a four-component multiply.</span></span> <span data-ttu-id="1187e-234">HLSL usa operazioni matematiche dei componenti che rendono molto efficiente la scrittura di shader.</span><span class="sxs-lookup"><span data-stu-id="1187e-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="1187e-235">Questo è molto diverso da una moltiplicazione che viene in genere implementata come prodotto punto che genera un singolo scalare:</span><span class="sxs-lookup"><span data-stu-id="1187e-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="1187e-236">Una matrice usa anche operazioni per componente in HLSL:</span><span class="sxs-lookup"><span data-stu-id="1187e-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="1187e-237">Il risultato è una moltiplicazione per componente delle due matrici (a differenza di una moltiplicazione standard di matrice 3x3).</span><span class="sxs-lookup"><span data-stu-id="1187e-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="1187e-238">La moltiplicazione di una matrice per componente restituisce questo primo termine:</span><span class="sxs-lookup"><span data-stu-id="1187e-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="1187e-239">Questo è diverso da una moltiplicazione di matrice 3x3 che restituisce questo primo termine:</span><span class="sxs-lookup"><span data-stu-id="1187e-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="1187e-240">Le versioni in overload della funzione intrinseca multiply gestiscono i casi in cui un operando è un vettore e l'altro operando è una matrice.</span><span class="sxs-lookup"><span data-stu-id="1187e-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="1187e-241">Ad esempio: \* vettore vettore, \* matrice vettoriale, \* vettore matrice e matrice \* matrice.</span><span class="sxs-lookup"><span data-stu-id="1187e-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="1187e-242">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1187e-242">For instance:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="1187e-243">produce lo stesso risultato di:</span><span class="sxs-lookup"><span data-stu-id="1187e-243">produces the same result as:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="1187e-244">Questo esempio esegue il cast del vettore pos a un vettore di colonna usando il cast (float1x4).</span><span class="sxs-lookup"><span data-stu-id="1187e-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="1187e-245">La modifica di un vettore tramite cast o lo scambio dell'ordine degli argomenti forniti per la moltiplicazione equivale a trasporre la matrice.</span><span class="sxs-lookup"><span data-stu-id="1187e-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="1187e-246">La conversione cast automatica fa in modo che le funzioni intrinseche multiply e dot restituiranno gli stessi risultati usati qui:</span><span class="sxs-lookup"><span data-stu-id="1187e-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="1187e-247">Questo risultato della moltiplicazione è un vettore 1x4 \* 4x1 = 1x1.</span><span class="sxs-lookup"><span data-stu-id="1187e-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="1187e-248">Equivale a un prodotto punto:</span><span class="sxs-lookup"><span data-stu-id="1187e-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="1187e-249">che restituisce un singolo valore scalare.</span><span class="sxs-lookup"><span data-stu-id="1187e-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1187e-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1187e-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1187e-251">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1187e-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




