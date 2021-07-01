---
title: Trasformazioni (DirectComposition)
description: In questo argomento viene illustrato il supporto di Microsoft DirectComposition per le trasformazioni affine (lineari) bidimensionali (2D) e vengono descritti i tipi di trasformazioni supportati da DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118656"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="7cf69-103">Trasformazioni (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="7cf69-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="7cf69-104">Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="7cf69-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="7cf69-105">Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="7cf69-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="7cf69-106">In questo argomento viene illustrato il supporto di Microsoft DirectComposition per le trasformazioni affine (lineari) bidimensionali (2D) e vengono descritti i tipi di trasformazioni supportati da DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="7cf69-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="7cf69-107">DirectComposition supporta anche trasformazioni prospettica 3D, ma poiché richiedono la creazione di una bitmap intermedia, DirectComposition le considera effetti anziché trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="7cf69-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="7cf69-108">Per informazioni sugli effetti di trasformazione prospettica 3D, vedere [Effetti.](effects.md)</span><span class="sxs-lookup"><span data-stu-id="7cf69-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="7cf69-109">Questo argomento include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cf69-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="7cf69-110">Che cos'è una trasformazione DirectComposition 2D?</span><span class="sxs-lookup"><span data-stu-id="7cf69-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="7cf69-111">Spazio delle coordinate 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="7cf69-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="7cf69-112">Supporto per trasformazioni 2D affine</span><span class="sxs-lookup"><span data-stu-id="7cf69-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="7cf69-113">Trasformazioni matrix 2D</span><span class="sxs-lookup"><span data-stu-id="7cf69-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="7cf69-114">Gruppi di trasformazioni</span><span class="sxs-lookup"><span data-stu-id="7cf69-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="7cf69-115">Animazione Transform</span><span class="sxs-lookup"><span data-stu-id="7cf69-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="7cf69-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cf69-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="7cf69-117">Che cos'è una trasformazione DirectComposition 2D?</span><span class="sxs-lookup"><span data-stu-id="7cf69-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="7cf69-118">Una trasformazione 2D consente di modificare la posizione, le dimensioni o la natura di un oggetto visivo in due dimensioni spostando l'oggetto visivo in un'altra posizione (traslazione), rendendolo più grande o più piccolo (ridimensionamento), ruotando (rotazione) o distorcendo la forma (inclinazione).</span><span class="sxs-lookup"><span data-stu-id="7cf69-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="7cf69-119">Una trasformazione 2D viene ottenuta tramite il mapping dei punti di un oggetto visivo da una posizione a un'altra all'interno dello stesso spazio delle coordinate o da uno spazio delle coordinate a un altro.</span><span class="sxs-lookup"><span data-stu-id="7cf69-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="7cf69-120">Questo mapping è descritto da una tabella di valori denominata matrice di trasformazione, definita come raccolta di tre righe con tre colonne di valori a virgola mobile, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7cf69-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="7cf69-121">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="7cf69-122">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="7cf69-123">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="7cf69-124">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="7cf69-125">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="7cf69-126">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="7cf69-127">0,0</span><span class="sxs-lookup"><span data-stu-id="7cf69-127">0.0</span></span><br/>
        <span data-ttu-id="7cf69-128">0,0</span><span class="sxs-lookup"><span data-stu-id="7cf69-128">0.0</span></span><br/>
        <span data-ttu-id="7cf69-129">1.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="7cf69-130">La matrice di trasformazione per le trasformazioni 2D affine è una matrice 3 per 2 che omette la terza colonna dalla matrice di trasformazione precedente.</span><span class="sxs-lookup"><span data-stu-id="7cf69-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="7cf69-131">Nella tabella seguente viene illustrato il layout di questa matrice.</span><span class="sxs-lookup"><span data-stu-id="7cf69-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="7cf69-132">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="7cf69-133">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="7cf69-134">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="7cf69-135">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="7cf69-136">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="7cf69-137">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="7cf69-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="7cf69-138">DirectComposition non esegue alcuna elaborazione speciale quando si applicano trasformazioni 2D a contenuto stereo.</span><span class="sxs-lookup"><span data-stu-id="7cf69-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="7cf69-139">Ciò significa che il contenuto 3D potrebbe apparire distorto quando vi viene applicata una trasformazione 2D.</span><span class="sxs-lookup"><span data-stu-id="7cf69-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="7cf69-140">Spazio delle coordinate 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="7cf69-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="7cf69-141">DirectComposition usa uno spazio delle coordinate 2D mancino; ciò significa che i valori positivi dell'asse x aumentano verso destra e i valori positivi dell'asse y aumentano verso il basso.</span><span class="sxs-lookup"><span data-stu-id="7cf69-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="7cf69-142">Gli oggetti visivi vengono posizionati in relazione all'origine, ovvero il punto in cui si intersecano l'asse x e l'asse y (0, 0), come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7cf69-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![l'asse x e l'asse y di uno spazio delle coordinate a sinistra](images/coordinatespace.png)

<span data-ttu-id="7cf69-144">Modificando i valori in una matrice di trasformazione 3 per 2, è possibile ruotare, ridimensionare, inclinare e traslare un oggetto in due dimensioni.</span><span class="sxs-lookup"><span data-stu-id="7cf69-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="7cf69-145">Ad esempio, se si imposta OffsetX su 100 e OffsetY su 200, si sposta l'oggetto a destra di 100 pixel e verso il basso di 200 pixel.</span><span class="sxs-lookup"><span data-stu-id="7cf69-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="7cf69-146">Supporto per trasformazioni 2D affine</span><span class="sxs-lookup"><span data-stu-id="7cf69-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="7cf69-147">La tabella seguente descrive i tipi di trasformazioni 2D affine supportate da DirectComposition ed elenca le interfacce che è possibile usare per eseguire i vari tipi di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="7cf69-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="7cf69-148">Trasformazione/interfaccia</span><span class="sxs-lookup"><span data-stu-id="7cf69-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="7cf69-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf69-149">Description</span></span>                                                                                              | <span data-ttu-id="7cf69-150">Illustrazione</span><span class="sxs-lookup"><span data-stu-id="7cf69-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf69-151">Ruotare la nuova riga [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ 2D\]</span><span class="sxs-lookup"><span data-stu-id="7cf69-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="7cf69-152">ruota un oggetto visivo in base all'angolo specificato intorno al punto centrale specificato.</span><span class="sxs-lookup"><span data-stu-id="7cf69-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![illustrazione di un quadrato ruotato di 45 gradi in senso orario intorno al centro del quadrato originale](images/rotate.png)               |
| <span data-ttu-id="7cf69-154">Scala 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="7cf69-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="7cf69-155">Ridimensiona un oggetto visivo in base al fattore specificato in base al punto centrale specificato.</span><span class="sxs-lookup"><span data-stu-id="7cf69-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![illustrazione di un quadrato ridimensionato del 130%](images/scale.png)                                                                  |
| <span data-ttu-id="7cf69-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="7cf69-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="7cf69-158">inclina un oggetto visivo in base all'angolo specificato lungo l'asse x e l'asse y e intorno al punto centrale specificato.</span><span class="sxs-lookup"><span data-stu-id="7cf69-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![illustrazione di un quadrato a inclinazione di 30 gradi in senso antiorario rispetto all'asse y](images/skew.png)                                   |
| <span data-ttu-id="7cf69-160">Convert 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="7cf69-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="7cf69-161">modificare la posizione di un oggetto visivo nella direzione dell'asse x e dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="7cf69-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![illustrazione di un quadrato spostato di 20 unità lungo l'asse x positivo e di 10 unità lungo l'asse y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="7cf69-163">Trasformazioni matrix 2D</span><span class="sxs-lookup"><span data-stu-id="7cf69-163">Matrix 2D transforms</span></span>

<span data-ttu-id="7cf69-164">[**L'interfaccia IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) consente di definire una matrice di trasformazione 2D affine 3 per 2 e applicarla a un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="7cf69-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="7cf69-165">Questa interfaccia è utile se è necessario applicare un tipo di trasformazione 2D affine che non è disponibile tramite le altre interfacce di trasformazione DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="7cf69-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="7cf69-166">Per definire la matrice, compilare una struttura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passarla al [**metodo IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)</span><span class="sxs-lookup"><span data-stu-id="7cf69-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="7cf69-167">Gruppi di trasformazioni</span><span class="sxs-lookup"><span data-stu-id="7cf69-167">Transform Groups</span></span>

<span data-ttu-id="7cf69-168">È possibile usare i gruppi di trasformazioni per combinare più trasformazioni in una sola.</span><span class="sxs-lookup"><span data-stu-id="7cf69-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="7cf69-169">Un gruppo di trasformazioni definisce una raccolta di oggetti transform le cui matrici vengono moltiplicate insieme nell'ordine in cui sono specificate nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="7cf69-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="7cf69-170">La matrice di trasformazione risultante viene quindi applicata all'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="7cf69-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="7cf69-171">Un gruppo di trasformazioni produce lo stesso risultato dell'applicazione separata di ogni trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7cf69-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="7cf69-172">Tenere presente che l'ordine degli oggetti di trasformazione in un gruppo di trasformazioni è importante.</span><span class="sxs-lookup"><span data-stu-id="7cf69-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="7cf69-173">Ad esempio, se un oggetto visivo viene prima ruotato, quindi ridimensionato e quindi convertito, il risultato è diverso da se l'oggetto visivo viene prima convertito, quindi ruotato e quindi ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="7cf69-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="7cf69-174">DirectComposition applica sempre le trasformazioni a un oggetto visivo nell'ordine in cui sono specificate nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="7cf69-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="7cf69-175">Per creare un gruppo di trasformazioni, creare prima di tutto gli oggetti di trasformazione da includere nel gruppo e quindi passare una matrice di puntatori all'oggetto transform al [**metodo IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup)</span><span class="sxs-lookup"><span data-stu-id="7cf69-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="7cf69-176">Dopo aver creato un gruppo di trasformazioni, non è possibile aggiungere o rimuovere oggetti di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7cf69-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="7cf69-177">Tuttavia, è possibile modificare le proprietà dei singoli oggetti transform nella raccolta e le modifiche verranno riflesse nella matrice di trasformazione risultante.</span><span class="sxs-lookup"><span data-stu-id="7cf69-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="7cf69-178">Animazione Transform</span><span class="sxs-lookup"><span data-stu-id="7cf69-178">Transform animation</span></span>

<span data-ttu-id="7cf69-179">È possibile animare le proprietà di una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7cf69-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="7cf69-180">Quando una proprietà viene animata, DirectComposition modifica il valore della proprietà nel tempo, anziché tutti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="7cf69-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="7cf69-181">Ciò è particolarmente utile quando si creano transizioni.</span><span class="sxs-lookup"><span data-stu-id="7cf69-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="7cf69-182">Per altre informazioni, vedere [Animazione.](animation.md)</span><span class="sxs-lookup"><span data-stu-id="7cf69-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cf69-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cf69-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cf69-184">Concetti relativi a DirectComposition</span><span class="sxs-lookup"><span data-stu-id="7cf69-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
