---
description: La parte di Direct3D che inserisce la geometria attraverso la pipeline di geometria della funzione fissa è il motore di trasformazione.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Trasformazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401339"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="597c9-103">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="597c9-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="597c9-104">La parte di Direct3D che inserisce la geometria attraverso la pipeline di geometria della funzione fissa è il motore di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="597c9-105">Individua il modello e il visualizzatore nel mondo, proietta i vertici per la visualizzazione sullo schermo e taglia i vertici nel viewport.</span><span class="sxs-lookup"><span data-stu-id="597c9-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="597c9-106">Il motore di trasformazione esegue anche calcoli di illuminazione per determinare i componenti speculari e speculari in ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="597c9-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="597c9-107">La pipeline Geometry accetta i vertici come input.</span><span class="sxs-lookup"><span data-stu-id="597c9-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="597c9-108">Il motore di trasformazione applica le trasformazioni del mondo, della visualizzazione e della proiezione ai vertici, ne ritaglia il risultato e passa tutti gli elementi al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="597c9-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="597c9-109">All'inizio della pipeline, i vertici di un modello vengono dichiarati in relazione a un sistema di coordinate locale.</span><span class="sxs-lookup"><span data-stu-id="597c9-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="597c9-110">Si tratta di un'origine locale e di un orientamento.</span><span class="sxs-lookup"><span data-stu-id="597c9-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="597c9-111">Questo orientamento delle coordinate viene spesso definito spazio del modello e le singole coordinate sono denominate coordinate del modello.</span><span class="sxs-lookup"><span data-stu-id="597c9-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="597c9-112">La prima fase della pipeline Geometry trasforma i vertici di un modello dal sistema di coordinate locale a un sistema di coordinate usato da tutti gli oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="597c9-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="597c9-113">Il processo di riorientamento dei vertici è denominato trasformazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="597c9-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="597c9-114">Questo nuovo orientamento viene comunemente definito spazio globale e ogni vertice nello spazio globale viene dichiarato usando le coordinate internazionali.</span><span class="sxs-lookup"><span data-stu-id="597c9-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="597c9-115">Nella fase successiva i vertici che descrivono il mondo 3D sono orientati rispetto alla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="597c9-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="597c9-116">In altre termini, l'applicazione sceglie un punto di visualizzazione per la scena e le coordinate dello spazio globale vengono rilocate e ruotate intorno alla visualizzazione della fotocamera, trasformando lo spazio mondiale nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="597c9-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="597c9-117">Si tratta della trasformazione visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-117">This is the view transform.</span></span>

<span data-ttu-id="597c9-118">La fase successiva è la trasformazione di proiezione.</span><span class="sxs-lookup"><span data-stu-id="597c9-118">The next stage is the projection transform.</span></span> <span data-ttu-id="597c9-119">In questa parte della pipeline gli oggetti vengono in genere ridimensionati in relazione alla distanza dal visualizzatore per dare l'illusione di profondità a una scena. gli oggetti Close vengono creati per apparire più grandi degli oggetti distanti e così via.</span><span class="sxs-lookup"><span data-stu-id="597c9-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="597c9-120">Per semplicità, questa documentazione si riferisce allo spazio in cui si trovano i vertici dopo la trasformazione della proiezione come spazio di proiezione.</span><span class="sxs-lookup"><span data-stu-id="597c9-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="597c9-121">Alcuni libri grafici potrebbero riferirsi allo spazio di proiezione come spazio omogeneo post-prospettiva.</span><span class="sxs-lookup"><span data-stu-id="597c9-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="597c9-122">Non tutte le trasformazioni di proiezione ridimensionano le dimensioni degli oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="597c9-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="597c9-123">Una proiezione come questa viene talvolta denominata proiezione affine o ortogonale.</span><span class="sxs-lookup"><span data-stu-id="597c9-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="597c9-124">Nella parte finale della pipeline, tutti i vertici che non saranno visibili sullo schermo vengono rimossi, in modo che il rasterizzatore non imprenda il tempo necessario per calcolare i colori e l'ombreggiatura per un elemento che non verrà mai visualizzato.</span><span class="sxs-lookup"><span data-stu-id="597c9-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="597c9-125">Questo processo è detto ritaglio.</span><span class="sxs-lookup"><span data-stu-id="597c9-125">This process is called clipping.</span></span> <span data-ttu-id="597c9-126">Dopo il ritaglio, i vertici rimanenti vengono ridimensionati in base ai parametri del viewport e convertiti in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="597c9-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="597c9-127">I vertici risultanti, visualizzati sullo schermo quando la scena è rasterizzata, esistono nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="597c9-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="597c9-128">Le trasformazioni vengono utilizzate per convertire la geometria dell'oggetto da uno spazio delle coordinate a un altro.</span><span class="sxs-lookup"><span data-stu-id="597c9-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="597c9-129">Direct3D usa matrici per eseguire trasformazioni 3D.</span><span class="sxs-lookup"><span data-stu-id="597c9-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="597c9-130">Questa sezione illustra in che modo le matrici creano trasformazioni 3D, descrive alcuni usi comuni per le trasformazioni e illustra come combinare le matrici per produrre una singola matrice che include più trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="597c9-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="597c9-131">[Trasformazione globale (Direct3D 9)](world-transform.md) -conversione dallo spazio del modello allo spazio globale</span><span class="sxs-lookup"><span data-stu-id="597c9-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="597c9-132">[Visualizzazione della trasformazione (Direct3D 9)](view-transform.md) : conversione dallo spazio globale allo spazio di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="597c9-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="597c9-133">[Trasformazione proiezione (Direct3D 9)](projection-transform.md) -conversione dallo spazio di visualizzazione allo spazio di proiezione</span><span class="sxs-lookup"><span data-stu-id="597c9-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="597c9-134">Trasformazioni con matrice</span><span class="sxs-lookup"><span data-stu-id="597c9-134">Matrix Transforms</span></span>

<span data-ttu-id="597c9-135">Nelle applicazioni che funzionano con la grafica 3D, è possibile utilizzare trasformazioni geometriche per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="597c9-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="597c9-136">Esprimere la posizione di un oggetto in relazione a un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="597c9-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="597c9-137">Ruotare e ridimensionare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="597c9-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="597c9-138">Modificare le posizioni, le direzioni e le prospettive di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="597c9-139">È possibile trasformare qualsiasi punto (x, y, z) in un altro punto (x ', y ', z ') usando una matrice 4x4, come illustrato nella seguente equazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![equazione di trasformazione di qualsiasi punto in un altro punto](images/matmult.png)

<span data-ttu-id="597c9-141">Eseguire le equazioni seguenti in (x, y, z) e nella matrice per produrre il punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="597c9-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![equazioni per il nuovo punto](images/matexpnd.png)

<span data-ttu-id="597c9-143">Le trasformazioni più comuni sono la traslazione, la rotazione e il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="597c9-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="597c9-144">È possibile combinare le matrici che producono questi effetti in un'unica matrice per calcolare diverse trasformazioni contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="597c9-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="597c9-145">Ad esempio, è possibile compilare una singola matrice per tradurre e ruotare una serie di punti.</span><span class="sxs-lookup"><span data-stu-id="597c9-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="597c9-146">Le matrici sono scritte nell'ordine delle colonne di riga.</span><span class="sxs-lookup"><span data-stu-id="597c9-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="597c9-147">Una matrice che consente di ridimensionare uniformemente i vertici lungo ogni asse, nota come scalabilità uniforme, viene rappresentata dalla matrice seguente usando la notazione matematica.</span><span class="sxs-lookup"><span data-stu-id="597c9-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![equazione di una matrice per la scalabilità uniforme](images/matrix.png)

<span data-ttu-id="597c9-149">In C++, Direct3D dichiara le matrici come matrice bidimensionale, usando la struttura [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="597c9-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="597c9-150">Nell'esempio seguente viene illustrato come inizializzare una struttura **D3DMATRIX** per fungere da matrice di scala uniforme.</span><span class="sxs-lookup"><span data-stu-id="597c9-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="597c9-151">Traduci</span><span class="sxs-lookup"><span data-stu-id="597c9-151">Translate</span></span>

<span data-ttu-id="597c9-152">L'equazione seguente converte il punto (x, y, z) in un nuovo punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="597c9-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![equazione di una matrice di traslazione per un nuovo punto](images/transl8.png)

<span data-ttu-id="597c9-154">È possibile creare manualmente una matrice di traslazione in C++.</span><span class="sxs-lookup"><span data-stu-id="597c9-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="597c9-155">Nell'esempio seguente viene illustrato il codice sorgente per una funzione che crea una matrice per tradurre i vertici.</span><span class="sxs-lookup"><span data-stu-id="597c9-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="597c9-156">Per praticità, la libreria dell'utilità D3DX fornisce la funzione [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .</span><span class="sxs-lookup"><span data-stu-id="597c9-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="597c9-157">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="597c9-157">Scale</span></span>

<span data-ttu-id="597c9-158">L'equazione seguente consente di ridimensionare il punto (x, y, z) in base ai valori arbitrari nelle direzioni x, y e z a un nuovo punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="597c9-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![equazione di una matrice di scala per un nuovo punto](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="597c9-160">Ruota</span><span class="sxs-lookup"><span data-stu-id="597c9-160">Rotate</span></span>

<span data-ttu-id="597c9-161">Le trasformazioni descritte di seguito sono per i sistemi di coordinate a sinistra, quindi possono essere diverse dalle matrici di trasformazione visualizzate altrove.</span><span class="sxs-lookup"><span data-stu-id="597c9-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="597c9-162">L'equazione seguente ruota il punto (x, y, z) intorno all'asse x, producendo un nuovo punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="597c9-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![equazione di una matrice di rotazione x per un nuovo punto](images/matxrot.png)

<span data-ttu-id="597c9-164">L'equazione seguente ruota il punto intorno all'asse y.</span><span class="sxs-lookup"><span data-stu-id="597c9-164">The following equation rotates the point around the y-axis.</span></span>

![equazione di una matrice di rotazione y per un nuovo punto](images/matyrot.png)

<span data-ttu-id="597c9-166">L'equazione seguente ruota il punto intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="597c9-166">The following equation rotates the point around the z-axis.</span></span>

![equazione di una matrice di rotazione z per un nuovo punto](images/matzrot.png)

<span data-ttu-id="597c9-168">In queste matrici di esempio, la lettera greca theta sta per l'angolo di rotazione, in radianti.</span><span class="sxs-lookup"><span data-stu-id="597c9-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="597c9-169">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="597c9-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="597c9-170">In un'applicazione C++, usare le funzioni [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)e [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fornite dalla libreria di utilità D3DX per creare matrici di rotazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="597c9-171">Di seguito è riportato il codice per la funzione **D3DXMatrixRotationX** .</span><span class="sxs-lookup"><span data-stu-id="597c9-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="597c9-172">Concatenazione di matrici</span><span class="sxs-lookup"><span data-stu-id="597c9-172">Concatenating Matrices</span></span>

<span data-ttu-id="597c9-173">Un vantaggio dell'uso delle matrici è che è possibile combinare gli effetti di due o più matrici moltiplicando questi ultimi.</span><span class="sxs-lookup"><span data-stu-id="597c9-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="597c9-174">Ciò significa che, per ruotare un modello e quindi convertirlo in una determinata posizione, non è necessario applicare due matrici.</span><span class="sxs-lookup"><span data-stu-id="597c9-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="597c9-175">Si moltiplicano invece le matrici di rotazione e traslazione per produrre una matrice composita che contiene tutti gli effetti.</span><span class="sxs-lookup"><span data-stu-id="597c9-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="597c9-176">Questo processo, denominato concatenazione di matrici, può essere scritto con la seguente equazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![equazione della concatenazione di matrici](images/matrxcat.png)

<span data-ttu-id="597c9-178">In questa equazione C è la matrice composta da creare e M ₁ tramite MN sono le singole matrici.</span><span class="sxs-lookup"><span data-stu-id="597c9-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="597c9-179">Nella maggior parte dei casi, vengono concatenate solo due o tre matrici, ma non esiste alcun limite.</span><span class="sxs-lookup"><span data-stu-id="597c9-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="597c9-180">Utilizzare la funzione [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) per eseguire la moltiplicazione di matrici.</span><span class="sxs-lookup"><span data-stu-id="597c9-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="597c9-181">L'ordine in cui viene eseguita la moltiplicazione della matrice è fondamentale.</span><span class="sxs-lookup"><span data-stu-id="597c9-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="597c9-182">La formula precedente riflette la regola da sinistra a destra della concatenazione di matrici.</span><span class="sxs-lookup"><span data-stu-id="597c9-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="597c9-183">Ovvero gli effetti visibili delle matrici utilizzate per creare una matrice composita vengono eseguiti nell'ordine da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="597c9-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="597c9-184">Nell'esempio seguente viene illustrata una tipica matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="597c9-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="597c9-185">Si supponga di creare la matrice globale per uno stereotipo di un disco volante.</span><span class="sxs-lookup"><span data-stu-id="597c9-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="597c9-186">È probabile che si voglia ruotare il disco volante intorno al centro, ovvero l'asse y dello spazio del modello, e tradurlo in un'altra posizione nella scena.</span><span class="sxs-lookup"><span data-stu-id="597c9-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="597c9-187">Per ottenere questo risultato, creare prima di tutto una matrice di rotazione, quindi moltiplicarla per una matrice di traslazione, come illustrato nella seguente equazione.</span><span class="sxs-lookup"><span data-stu-id="597c9-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![equazione di rotazione basata su una matrice di rotazione e una matrice di traslazione](images/wrldexpl.png)

<span data-ttu-id="597c9-189">In questa formula, R<sub>y</sub> è una matrice per la rotazione sull'asse y e T<sub>w</sub> è una traduzione in una posizione in coordinate internazionali.</span><span class="sxs-lookup"><span data-stu-id="597c9-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="597c9-190">L'ordine in cui si moltiplicano le matrici è importante perché, diversamente dalla moltiplicazione di due valori scalari, la moltiplicazione di matrici non è commutativa.</span><span class="sxs-lookup"><span data-stu-id="597c9-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="597c9-191">La moltiplicazione delle matrici nell'ordine opposto ha l'effetto visivo di tradurre il disco volante nella posizione dello spazio globale e quindi di ruotarlo intorno all'origine globale.</span><span class="sxs-lookup"><span data-stu-id="597c9-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="597c9-192">Indipendentemente dal tipo di matrice che si sta creando, tenere presente la regola da sinistra a destra per assicurarsi di ottenere gli effetti previsti.</span><span class="sxs-lookup"><span data-stu-id="597c9-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="597c9-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="597c9-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="597c9-194">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="597c9-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



