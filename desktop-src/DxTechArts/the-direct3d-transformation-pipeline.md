---
title: Pipeline di trasformazione Direct3D
description: Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D mediante la manipolazione diretta delle matrici Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "103885890"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="dff4a-103">Pipeline di trasformazione Direct3D</span><span class="sxs-lookup"><span data-stu-id="dff4a-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="dff4a-104">Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D mediante la manipolazione diretta delle matrici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dff4a-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="dff4a-105">Overview</span><span class="sxs-lookup"><span data-stu-id="dff4a-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="dff4a-106">Pipeline di trasformazione</span><span class="sxs-lookup"><span data-stu-id="dff4a-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="dff4a-107">Suggerimenti sull'utilizzo</span><span class="sxs-lookup"><span data-stu-id="dff4a-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="dff4a-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="dff4a-108">Overview</span></span>

<span data-ttu-id="dff4a-109">Direct3D usa tre trasformazioni per modificare le coordinate del modello 3D in coordinate pixel (spazio dello schermo).</span><span class="sxs-lookup"><span data-stu-id="dff4a-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="dff4a-110">Queste trasformazioni sono trasformazione globale, trasformazione visualizzazione e trasformazione proiezione.</span><span class="sxs-lookup"><span data-stu-id="dff4a-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="dff4a-111">La trasformazione globale controlla il modo in cui le coordinate del modello vengono trasformate in coordinate internazionali.</span><span class="sxs-lookup"><span data-stu-id="dff4a-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="dff4a-112">La trasformazione mondiale può includere traduzioni, rotazioni e scalabilità, ma non si applica alle luci.</span><span class="sxs-lookup"><span data-stu-id="dff4a-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="dff4a-113">Per altre informazioni sull'uso delle trasformazioni internazionali, vedere [trasformazione globale](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="dff4a-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="dff4a-114">Visualizza trasformazione consente di controllare la transizione dalle coordinate internazionali allo "spazio della fotocamera", determinando la posizione della fotocamera nel mondo.</span><span class="sxs-lookup"><span data-stu-id="dff4a-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="dff4a-115">Per un esempio di utilizzo delle trasformazioni di visualizzazione, vedere [visualizzazione della trasformazione](/windows/desktop/direct3d9/view-transform).</span><span class="sxs-lookup"><span data-stu-id="dff4a-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="dff4a-116">La trasformazione proiezione modifica la geometria dallo spazio della fotocamera in "spazio di ritaglio" e applica la distorsione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="dff4a-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="dff4a-117">Il termine "spazio di ritaglio" indica il modo in cui la geometria viene ritagliata nel volume di visualizzazione durante questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="dff4a-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="dff4a-118">Per un esempio di utilizzo delle trasformazioni di proiezione, vedere [trasformazione proiezione](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="dff4a-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="dff4a-119">Infine, la geometria nello spazio di ritaglio viene trasformata in coordinate pixel (spazio dello schermo).</span><span class="sxs-lookup"><span data-stu-id="dff4a-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="dff4a-120">Questa trasformazione è controllata dalle impostazioni del viewport.</span><span class="sxs-lookup"><span data-stu-id="dff4a-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="dff4a-121">Il ritaglio e la trasformazione dei vertici devono avvenire nello spazio omogeneo (semplicemente put, nello spazio in cui il sistema di coordinate include un quarto elemento), ma il risultato finale per la maggior parte delle applicazioni deve essere costituito da coordinate tridimensionali (3D) non omogenee definite nello "spazio dello schermo".</span><span class="sxs-lookup"><span data-stu-id="dff4a-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="dff4a-122">Ciò significa che sia i vertici di input che il volume di ritaglio devono essere convertiti in uno spazio omogeneo per eseguire il ritaglio e quindi convertiti di nuovo nello spazio non omogeneo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="dff4a-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="dff4a-123">Le tre trasformazioni Direct3D-mondo, visualizzazione e trasformazione proiezione-sono definite dalle matrici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dff4a-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="dff4a-124">Una matrice Direct3D è una matrice omogenea 4x4 definita da una struttura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) .</span><span class="sxs-lookup"><span data-stu-id="dff4a-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="dff4a-125">Sebbene le matrici Direct3D non siano oggetti standard, non sono rappresentate da un'interfaccia COM. è possibile crearle e impostarle esattamente come qualsiasi altro oggetto Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dff4a-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="dff4a-126">Per ulteriori informazioni sulle matrici Direct3D, vedere [trasformazioni](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="dff4a-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="dff4a-127">Pipeline di trasformazione</span><span class="sxs-lookup"><span data-stu-id="dff4a-127">The Transformation Pipeline</span></span>

<span data-ttu-id="dff4a-128">Se un vertice nella coordinata del modello viene fornito da PM = (XM, YM, ZM, 1), le trasformazioni mostrate nella figura seguente vengono applicate alle coordinate della schermata di calcolo PS = (XS, Ys, ZS, WS).</span><span class="sxs-lookup"><span data-stu-id="dff4a-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![spazio del modello per la trasformazione dello spazio dello schermo](images/d3dxfrm61.gif)

<span data-ttu-id="dff4a-130">Di seguito sono riportate le descrizioni delle fasi illustrate nella figura precedente:</span><span class="sxs-lookup"><span data-stu-id="dff4a-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="dff4a-131">MWorld della matrice mondiale trasforma i vertici dallo spazio del modello allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="dff4a-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="dff4a-132">Questa matrice è impostata da:</span><span class="sxs-lookup"><span data-stu-id="dff4a-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="dff4a-133">Nell'implementazione di Direct3D si presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="dff4a-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="dff4a-134">Non viene restituito alcun errore se l'utente specifica una matrice con un'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.</span><span class="sxs-lookup"><span data-stu-id="dff4a-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="dff4a-135">View Matrix mview trasforma i vertici dallo spazio globale allo spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="dff4a-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="dff4a-136">Questa matrice è impostata da:</span><span class="sxs-lookup"><span data-stu-id="dff4a-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="dff4a-137">Nell'implementazione di Direct3D si presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="dff4a-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="dff4a-138">Non viene restituito alcun errore se l'utente specifica una matrice con un'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.</span><span class="sxs-lookup"><span data-stu-id="dff4a-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="dff4a-139">La matrice di proiezione mproj trasforma i vertici dallo spazio della fotocamera allo spazio di proiezione.</span><span class="sxs-lookup"><span data-stu-id="dff4a-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="dff4a-140">Questa matrice è impostata da:</span><span class="sxs-lookup"><span data-stu-id="dff4a-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="dff4a-141">L'ultima colonna della matrice di proiezione deve essere (0, 0, 1, 0) o (0, 0, a,0) per gli effetti di nebbia e illuminazione corretti; (0, 0, 1, 0) il formato è preferibile.</span><span class="sxs-lookup"><span data-stu-id="dff4a-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="dff4a-142">Il volume di ritaglio per tutti i punti XP = (XP, YP, ZP, WP) nello spazio di proiezione è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="dff4a-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="dff4a-143">Tutti i punti che non soddisfano queste equazioni verranno ritagliati.</span><span class="sxs-lookup"><span data-stu-id="dff4a-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="dff4a-144">Se un volume di visualizzazione è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="dff4a-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="dff4a-145">SW-Larghezza della finestra dello schermo nello spazio della fotocamera in prossimità del piano di ritaglio</span><span class="sxs-lookup"><span data-stu-id="dff4a-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="dff4a-146">Altezza della finestra dello schermo SH nello spazio della fotocamera vicino al piano di ritaglio</span><span class="sxs-lookup"><span data-stu-id="dff4a-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="dff4a-147">Zn-distanza dal piano di ritaglio vicino lungo gli assi Z nello spazio della fotocamera</span><span class="sxs-lookup"><span data-stu-id="dff4a-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="dff4a-148">ZF-distanza dal piano di ritaglio lungo lungo gli assi Z nello spazio della fotocamera</span><span class="sxs-lookup"><span data-stu-id="dff4a-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="dff4a-149">una matrice di proiezione prospettica potrebbe quindi essere scritta nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dff4a-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Mostra una matrice di proiezione prospettica.](images/d3dxfrm62.gif)

    <span data-ttu-id="dff4a-151">dove mij sono membri di mproj.</span><span class="sxs-lookup"><span data-stu-id="dff4a-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="dff4a-152">Per la proiezione ortogonale sono disponibili:</span><span class="sxs-lookup"><span data-stu-id="dff4a-152">For the orthogonal projection we have:</span></span>

    ![proiezione ortogonale](images/d3dxfrm63.gif)

    <span data-ttu-id="dff4a-154">Direct3D presuppone che la matrice di proiezione prospettica abbia il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dff4a-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![matrice di proiezione prospettica](images/d3dxfrm64.gif)

    <span data-ttu-id="dff4a-156">Se la matrice di proiezione prospettica non presenta questo formato, saranno presenti alcuni artefatti.</span><span class="sxs-lookup"><span data-stu-id="dff4a-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="dff4a-157">Ad esempio, la nebbia della tabella non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="dff4a-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="dff4a-158">Direct3D consente all'utente di modificare il volume di ritaglio come segue:</span><span class="sxs-lookup"><span data-stu-id="dff4a-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![modificare il volume di ritaglio](images/d3dxfrm65.gif)

    <span data-ttu-id="dff4a-160">Questa operazione può essere riscritta come segue:</span><span class="sxs-lookup"><span data-stu-id="dff4a-160">This can be rewritten as:</span></span>

    ![modificare il volume di clip riscritto](images/d3dxfrm66.gif)

    <span data-ttu-id="dff4a-162">dove:</span><span class="sxs-lookup"><span data-stu-id="dff4a-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="dff4a-163">Questa trasformazione può fornire maggiore precisione ed equivale a ridimensionare e spostare il volume di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="dff4a-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="dff4a-164">La matrice Mclip corrispondente è:</span><span class="sxs-lookup"><span data-stu-id="dff4a-164">The corresponding Mclip matrix is:</span></span>

    ![matrice mclip](images/d3dxfrm67.gif)

    <span data-ttu-id="dff4a-166">Un vertice viene trasformato da:</span><span class="sxs-lookup"><span data-stu-id="dff4a-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="dff4a-167">Se non si vuole ridimensionare il volume di ritaglio, è possibile impostare i parametri del viewport sui valori predefiniti:</span><span class="sxs-lookup"><span data-stu-id="dff4a-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="dff4a-168">La fase di ritaglio è facoltativa se l'utente specifica il \_ flag D3DDP DONOTCLIP in una chiamata DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="dff4a-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="dff4a-169">In questo caso, è possibile combinare tutte le matrici (incluso MVS).</span><span class="sxs-lookup"><span data-stu-id="dff4a-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="dff4a-170">La matrice di scala del viewport MVS ridimensiona le coordinate in modo che si trovino all'interno della finestra del viewport e capovolge l'asse Y da un verso il basso:</span><span class="sxs-lookup"><span data-stu-id="dff4a-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![MVS della matrice di scala del viewport](images/d3dxfrm68.gif)

    <span data-ttu-id="dff4a-172">dove:</span><span class="sxs-lookup"><span data-stu-id="dff4a-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="dff4a-173">Infine, le coordinate dello schermo vengono calcolate e passate al rasterizzatore:</span><span class="sxs-lookup"><span data-stu-id="dff4a-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![Coordinate dello schermo calcolate e passate al rasterizzatore](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="dff4a-175">Suggerimenti sull'utilizzo</span><span class="sxs-lookup"><span data-stu-id="dff4a-175">Usage Tips</span></span>

<span data-ttu-id="dff4a-176">Ecco alcuni suggerimenti su come usare la pipeline di trasformazione Direct3D:</span><span class="sxs-lookup"><span data-stu-id="dff4a-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="dff4a-177">L'ultima colonna delle matrici World e View deve essere (0, 0, 0, 1) o l'illuminazione non sarà corretta.</span><span class="sxs-lookup"><span data-stu-id="dff4a-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="dff4a-178">Impostare i parametri del viewport per compilare una matrice Identity Mclip, a meno che non si conosca esattamente ciò che è necessario per.</span><span class="sxs-lookup"><span data-stu-id="dff4a-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 