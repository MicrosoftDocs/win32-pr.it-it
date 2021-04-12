---
description: È possibile considerare la trasformazione proiezione come il controllo degli elementi interni della fotocamera; è analogo alla scelta di una lente per la fotocamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Trasformazione proiezione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225421"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="e31b2-103">Trasformazione proiezione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e31b2-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="e31b2-104">È possibile considerare la trasformazione proiezione come il controllo degli elementi interni della fotocamera; è analogo alla scelta di una lente per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="e31b2-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="e31b2-105">Questo è il più complesso dei tre tipi di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e31b2-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="e31b2-106">Questa discussione sulla trasformazione proiezione è organizzata negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="e31b2-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="e31b2-107">La matrice di proiezione è in genere una proiezione di scala e prospettiva.</span><span class="sxs-lookup"><span data-stu-id="e31b2-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="e31b2-108">La trasformazione proiezione converte il tronco di visualizzazione in una forma Cuboid.</span><span class="sxs-lookup"><span data-stu-id="e31b2-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="e31b2-109">Poiché la fine del tronco di visualizzazione è inferiore alla fine, questo ha l'effetto di espandere gli oggetti vicini alla fotocamera; Questo è il modo in cui la prospettiva viene applicata alla scena.</span><span class="sxs-lookup"><span data-stu-id="e31b2-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="e31b2-110">Nel [tronco di visualizzazione](viewports-and-clipping.md), la distanza tra la camera e l'origine dello spazio di trasformazione di visualizzazione è definita arbitrariamente come D, quindi la matrice di proiezione è simile alla figura seguente.</span><span class="sxs-lookup"><span data-stu-id="e31b2-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![illustrazione della matrice di proiezione](images/projmat1.png)

<span data-ttu-id="e31b2-112">La matrice di visualizzazione converte la fotocamera nell'origine traducendo in z Direction by-D. La matrice di traslazione è simile alla figura seguente.</span><span class="sxs-lookup"><span data-stu-id="e31b2-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![illustrazione della matrice di traslazione](images/projmat2.png)

<span data-ttu-id="e31b2-114">La moltiplicazione della matrice di traslazione da parte della matrice di proiezione (T \* P) fornisce la matrice di proiezione composita, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="e31b2-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![illustrazione della matrice di proiezione composita](images/projmat3.png)

<span data-ttu-id="e31b2-116">La trasformazione prospettiva converte un tronco di visualizzazione in un nuovo spazio delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="e31b2-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="e31b2-117">Si noti che tronco diventa Cuboid e anche che l'origine si sposta dall'angolo superiore destro della scena al centro, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e31b2-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![diagramma del modo in cui la trasformazione prospettiva modifica il tronco di visualizzazione in un nuovo spazio delle coordinate](images/cuboid.png)

<span data-ttu-id="e31b2-119">Nella trasformazione prospettiva i limiti delle direzioni x e y sono-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="e31b2-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="e31b2-120">I limiti della direzione z sono 0 per il piano anteriore e 1 per il piano posteriore.</span><span class="sxs-lookup"><span data-stu-id="e31b2-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="e31b2-121">Questa matrice converte e ridimensiona gli oggetti in base a una distanza specificata dalla fotocamera al piano di ritaglio vicino, ma non considera il campo di visualizzazione (FOV) e i valori z che produce per gli oggetti nella distanza possono essere quasi identici, rendendo difficili i confronti di profondità.</span><span class="sxs-lookup"><span data-stu-id="e31b2-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="e31b2-122">La matrice seguente risolve questi problemi e regola i vertici per tenere conto delle proporzioni del viewport, rendendola una scelta ottimale per la proiezione prospettica.</span><span class="sxs-lookup"><span data-stu-id="e31b2-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![illustrazione di una matrice per la proiezione prospettica](images/prjmatx1.png)

<span data-ttu-id="e31b2-124">In questa matrice, Zn è il valore z del piano di ritaglio vicino.</span><span class="sxs-lookup"><span data-stu-id="e31b2-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="e31b2-125">Le variabili w, h e Q hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="e31b2-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="e31b2-126">Si noti che FOV<sub>w</sub> e fovk rappresentano i campi di visualizzazione orizzontali e verticali del viewport, in radianti.</span><span class="sxs-lookup"><span data-stu-id="e31b2-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![equazioni del significato delle variabili](images/prjmatx2.png)

<span data-ttu-id="e31b2-128">Per l'applicazione, l'uso di angoli di campo per la visualizzazione per definire i coefficienti di ridimensionamento x e y potrebbe non essere così comodo come usare le dimensioni orizzontali e verticali del viewport (nello spazio della fotocamera).</span><span class="sxs-lookup"><span data-stu-id="e31b2-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="e31b2-129">Quando la matematica funziona, le due equazioni seguenti per w e h utilizzano le dimensioni del viewport e sono equivalenti alle equazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e31b2-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![equazioni dei significati delle variabili w e h](images/prjmatx3.png)

<span data-ttu-id="e31b2-131">In queste formule, Zn rappresenta la posizione del piano di ritaglio vicino e le variabili V<sub>w</sub> e VH rappresentano la larghezza e l'altezza del viewport, nello spazio fotocamera.</span><span class="sxs-lookup"><span data-stu-id="e31b2-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="e31b2-132">Per un'applicazione C++, queste due dimensioni corrispondono direttamente ai membri Width e Height della struttura [**D3DVIEWPORT9**](d3dviewport9.md) .</span><span class="sxs-lookup"><span data-stu-id="e31b2-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="e31b2-133">Indipendentemente dalla formula che si decide di usare, assicurarsi di impostare Zn sul valore più grande possibile, perché i valori z estremamente vicini alla fotocamera non variano molto.</span><span class="sxs-lookup"><span data-stu-id="e31b2-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="e31b2-134">In questo modo si semplificano i confronti con i buffer z a 16 bit piuttosto complicati.</span><span class="sxs-lookup"><span data-stu-id="e31b2-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="e31b2-135">Come per le trasformazioni World e View, è possibile chiamare il metodo [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la trasformazione di proiezione.</span><span class="sxs-lookup"><span data-stu-id="e31b2-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="e31b2-136">Impostazione di una matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="e31b2-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="e31b2-137">La funzione di esempio ProjectionMatrix seguente imposta i piani di ritaglio anteriore e posteriore, nonché il campo orizzontale e verticale degli angoli di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e31b2-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="e31b2-138">I campi della visualizzazione devono essere minori di pi greco radianti.</span><span class="sxs-lookup"><span data-stu-id="e31b2-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="e31b2-139">Dopo aver creato la matrice, impostarla con [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specificando la \_ proiezione D3DTS.</span><span class="sxs-lookup"><span data-stu-id="e31b2-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="e31b2-140">La libreria di utilità D3DX fornisce le funzioni seguenti che consentono di configurare la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="e31b2-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="e31b2-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="e31b2-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="e31b2-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="e31b2-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="e31b2-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="e31b2-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="e31b2-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="e31b2-147">Matrice di proiezione facile da W</span><span class="sxs-lookup"><span data-stu-id="e31b2-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="e31b2-148">Direct3D può usare il componente w di un vertice che è stato trasformato dalle matrici World, View e Projection per eseguire calcoli basati sulla profondità negli effetti di nebbia o di buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="e31b2-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="e31b2-149">I calcoli, ad esempio, richiedono che la matrice di proiezione normalizzare w sia equivalente allo spazio globale z.</span><span class="sxs-lookup"><span data-stu-id="e31b2-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="e31b2-150">In breve, se la matrice di proiezione include un coefficiente (3, 4) diverso da 1, è necessario ridimensionare tutti i coefficienti in base all'inverso del coefficiente (3,4) per creare una matrice corretta.</span><span class="sxs-lookup"><span data-stu-id="e31b2-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="e31b2-151">Se non si specifica una matrice conforme, gli effetti della nebbia e il buffer di profondità non vengono applicati correttamente.</span><span class="sxs-lookup"><span data-stu-id="e31b2-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="e31b2-152">Nella figura seguente è illustrata una matrice di proiezione non conforme e la stessa matrice è stata ridimensionata in modo da abilitare la nebbia relativa all'occhio.</span><span class="sxs-lookup"><span data-stu-id="e31b2-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![illustrazioni di una matrice di proiezione non conforme e una matrice con la nebbia relativa agli occhi](images/eyerlmx.png)

<span data-ttu-id="e31b2-154">Nelle matrici precedenti, si presuppone che tutte le variabili siano diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="e31b2-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="e31b2-155">Per altre informazioni sulla nebbia relativa agli occhi, vedere [profondità basata sull'occhio](pixel-fog.md)rispetto alla Z.</span><span class="sxs-lookup"><span data-stu-id="e31b2-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="e31b2-156">Per informazioni sul buffer di profondità basato su w, vedere [buffer di profondità (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="e31b2-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="e31b2-157">Direct3D usa la matrice di proiezione attualmente impostata nei calcoli di profondità basati su w.</span><span class="sxs-lookup"><span data-stu-id="e31b2-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="e31b2-158">Di conseguenza, le applicazioni devono impostare una matrice di proiezione conforme per ricevere le funzionalità basate su w desiderate, anche se non usano Direct3D per le trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="e31b2-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e31b2-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e31b2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e31b2-160">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="e31b2-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
