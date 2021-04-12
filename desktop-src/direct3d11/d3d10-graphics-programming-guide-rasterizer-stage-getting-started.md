---
title: Introduzione con la fase di rasterizzazione
description: In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multicampionamento, stato di rasterizzazione (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337582"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="33e8e-104">Introduzione con la fase di rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="33e8e-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="33e8e-105">In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="33e8e-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="33e8e-106">Imposta il viewport</span><span class="sxs-lookup"><span data-stu-id="33e8e-106">Set the Viewport</span></span>

<span data-ttu-id="33e8e-107">Un viewport esegue il mapping delle posizioni del vertice (nello spazio di ritaglio) nelle posizioni della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="33e8e-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="33e8e-108">Questo passaggio ridimensiona le posizioni 3D nello spazio 2D.</span><span class="sxs-lookup"><span data-stu-id="33e8e-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="33e8e-109">Una destinazione di rendering è orientata agli assi Y che puntano verso il basso; a tale scopo, è necessario che le coordinate Y vengano capovolte durante la scala del viewport.</span><span class="sxs-lookup"><span data-stu-id="33e8e-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="33e8e-110">Inoltre, gli extent x e y (intervallo dei valori x e y) vengono ridimensionati in modo da adattarsi alle dimensioni del viewport in base alle formule seguenti:</span><span class="sxs-lookup"><span data-stu-id="33e8e-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="33e8e-111">L'esercitazione 1 crea un viewport 640 × 480 usando il [**\_ viewport d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e chiamando [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span><span class="sxs-lookup"><span data-stu-id="33e8e-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="33e8e-112">La descrizione del viewport specifica le dimensioni del viewport, l'intervallo in base al quale eseguire il mapping della profondità (tramite *MinDepth* e *MaxDepth*) e la posizione della parte superiore sinistra del viewport.</span><span class="sxs-lookup"><span data-stu-id="33e8e-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="33e8e-113">*MinDepth* deve essere minore o uguale a *MaxDepth*; l'intervallo sia per *MinDepth* che per *MaxDepth* è compreso tra 0,0 e 1,0 inclusi.</span><span class="sxs-lookup"><span data-stu-id="33e8e-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="33e8e-114">È comune che il viewport esegua il mapping a una destinazione di rendering, ma non è necessario. Inoltre, il viewport non deve avere la stessa dimensione o la stessa posizione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="33e8e-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="33e8e-115">È possibile creare una matrice di viewport, ma solo uno può essere applicato a un output primitivo da Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="33e8e-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="33e8e-116">È possibile impostare un solo viewport come attivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="33e8e-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="33e8e-117">La pipeline usa un viewport predefinito (e un rettangolo a forbice, illustrato nella sezione successiva) durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="33e8e-118">Il valore predefinito è sempre il primo Viewport (o rettangolo a forbice) nella matrice.</span><span class="sxs-lookup"><span data-stu-id="33e8e-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="33e8e-119">Per eseguire una selezione per primitiva del viewport in Geometry shader, specificare la semantica ViewportArrayIndex sul componente di output GS appropriato nella dichiarazione della firma di output GS.</span><span class="sxs-lookup"><span data-stu-id="33e8e-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="33e8e-120">Il numero massimo di viewport (e rettangoli a forbice) che possono essere associati alla fase di rasterizzazione in qualsiasi momento è 16 (specificato dal **\_ viewport d3d11 \_ e il numero di \_ \_ oggetti SCISSORRECT \_ \_ per \_ pipeline**).</span><span class="sxs-lookup"><span data-stu-id="33e8e-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="33e8e-121">Impostare il rettangolo a forbice</span><span class="sxs-lookup"><span data-stu-id="33e8e-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="33e8e-122">Un rettangolo a forbice offre un'altra opportunità per ridurre il numero di pixel che verranno inviati alla fase di Unione dell'output.</span><span class="sxs-lookup"><span data-stu-id="33e8e-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="33e8e-123">I pixel esterni al rettangolo a forbice vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="33e8e-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="33e8e-124">Le dimensioni del rettangolo a forbice sono specificate in numeri interi.</span><span class="sxs-lookup"><span data-stu-id="33e8e-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="33e8e-125">Solo un rettangolo a forbice (basato su *ViewportArrayIndex* nella [semantica di valori di sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) può essere applicato a un triangolo durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="33e8e-126">Per abilitare il rettangolo a forbice, usare il membro *ScissorEnable* (in [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="33e8e-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="33e8e-127">Il rettangolo a forbice predefinito è un rettangolo vuoto; ovvero tutti i valori Rect sono pari a 0.</span><span class="sxs-lookup"><span data-stu-id="33e8e-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="33e8e-128">In altre parole, se non si configura il rettangolo a forbice e la forbice è abilitata, non verrà inviato alcun pixel alla fase di Unione dell'output.</span><span class="sxs-lookup"><span data-stu-id="33e8e-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="33e8e-129">La configurazione più comune consiste nell'inizializzare il rettangolo a forbice sulle dimensioni del viewport.</span><span class="sxs-lookup"><span data-stu-id="33e8e-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="33e8e-130">Per impostare una matrice di rettangoli Scissor sul dispositivo, chiamare [**sul ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**d3d11 \_ Rect**](d3d11-rect.md).</span><span class="sxs-lookup"><span data-stu-id="33e8e-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="33e8e-131">Questo metodo accetta due parametri: (1) il numero di rettangoli nella matrice e (2) una matrice di rettangoli.</span><span class="sxs-lookup"><span data-stu-id="33e8e-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="33e8e-132">La pipeline utilizza un indice rettangolare a forbice predefinito durante la rasterizzazione (il valore predefinito è un rettangolo di dimensioni zero con ritaglio disabilitato).</span><span class="sxs-lookup"><span data-stu-id="33e8e-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="33e8e-133">Per eseguire l'override di questa impostazione, specificare la \_ semantica SV ViewportArrayIndex per un componente di output GS nella dichiarazione della firma di output GS.</span><span class="sxs-lookup"><span data-stu-id="33e8e-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="33e8e-134">In questo modo la fase GS contrassegna questo componente di output GS come componente generato dal sistema con questa semantica.</span><span class="sxs-lookup"><span data-stu-id="33e8e-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="33e8e-135">La fase di rasterizzazione riconosce questa semantica e utilizzerà il parametro a cui è associato come indice del rettangolo a forbice per accedere alla matrice di rettangoli a forbice.</span><span class="sxs-lookup"><span data-stu-id="33e8e-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="33e8e-136">Non dimenticare di indicare alla fase di rasterizzazione di usare il rettangolo a forbice definito abilitando il valore *ScissorEnable* nella descrizione del rasterizzatore prima di creare l'oggetto di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="33e8e-137">Imposta lo stato di rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="33e8e-137">Set Rasterizer State</span></span>

<span data-ttu-id="33e8e-138">A partire da Direct3D 10, lo stato di rasterizzazione viene incapsulato in un oggetto di stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="33e8e-139">È possibile creare fino a 4096 oggetti di stato di rasterizzazione che possono quindi essere impostati sul dispositivo passando un handle all'oggetto stato.</span><span class="sxs-lookup"><span data-stu-id="33e8e-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="33e8e-140">Usare [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) per creare un oggetto stato di rasterizzazione da una descrizione del rasterizzatore (vedere [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="33e8e-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="33e8e-141">Questo set di Stati di esempio esegue probabilmente la configurazione del rasterizzatore più semplice:</span><span class="sxs-lookup"><span data-stu-id="33e8e-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="33e8e-142">Modalità di riempimento a tinta unita</span><span class="sxs-lookup"><span data-stu-id="33e8e-142">Solid fill mode</span></span>
-   <span data-ttu-id="33e8e-143">Eliminare o rimuovere i visi posteriori; presume l'ordine di avvolgimento in senso antiorario per le primitive</span><span class="sxs-lookup"><span data-stu-id="33e8e-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="33e8e-144">Disabilitare la distorsione di profondità ma abilitare il buffering di profondità e abilitare il rettangolo a forbice</span><span class="sxs-lookup"><span data-stu-id="33e8e-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="33e8e-145">Disattiva il campionamento multiplo e l'anti-aliasing della linea</span><span class="sxs-lookup"><span data-stu-id="33e8e-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="33e8e-146">Inoltre, le operazioni di rasterizzazione di base includono sempre gli elementi seguenti: ritaglio (alla visualizzazione tronco), divisione prospettica e scala del viewport.</span><span class="sxs-lookup"><span data-stu-id="33e8e-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="33e8e-147">Dopo aver creato l'oggetto stato di rasterizzazione, impostarlo sul dispositivo come segue:</span><span class="sxs-lookup"><span data-stu-id="33e8e-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="33e8e-148">Multicampionamento</span><span class="sxs-lookup"><span data-stu-id="33e8e-148">Multisampling</span></span>

<span data-ttu-id="33e8e-149">Il campionamento multiplo esegue il campionamento di alcuni o tutti i componenti di un'immagine a una risoluzione più elevata (seguita da sottocampionando alla risoluzione originale) per ridurre il formato di alias più visibile causato dalla creazione di bordi del poligono.</span><span class="sxs-lookup"><span data-stu-id="33e8e-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="33e8e-150">Sebbene il multicampionamento richieda esempi di sottopixel, la GPU moderna implementa il campionamento multiplo in modo che una pixel shader venga eseguita una volta per ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="33e8e-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="33e8e-151">Ciò garantisce un compromesso accettabile tra le prestazioni, soprattutto in un'applicazione con binding GPU, e l'anti-aliasing dell'immagine finale.</span><span class="sxs-lookup"><span data-stu-id="33e8e-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="33e8e-152">Per usare il campionamento multiplo, impostare il campo Enable nella [**Descrizione della rasterizzazione**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), creare una destinazione di rendering multicampionata e leggere la destinazione di rendering con uno shader per risolvere gli esempi in un singolo colore pixel oppure chiamare [**sul ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) per risolvere gli esempi usando la scheda video.</span><span class="sxs-lookup"><span data-stu-id="33e8e-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="33e8e-153">Lo scenario più comune consiste nel disegnare in una o più destinazioni di rendering multicampionate.</span><span class="sxs-lookup"><span data-stu-id="33e8e-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="33e8e-154">Il campionamento multiplo è indipendente dal fatto che venga utilizzata o meno una maschera di esempio, che sia abilitata la funzionalità [alfa per il code coverage](d3d10-graphics-programming-guide-blend-state.md) o le operazioni dello stencil, che vengono sempre eseguite per campione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="33e8e-155">I test di profondità sono interessati dal campionamento multiplo:</span><span class="sxs-lookup"><span data-stu-id="33e8e-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="33e8e-156">Quando è abilitato il campionamento multiplo, la profondità viene interpolata per esempio e il test di profondità/stencil viene eseguito per campione; il colore di output del pixel shader viene duplicato per tutti gli esempi che passano.</span><span class="sxs-lookup"><span data-stu-id="33e8e-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="33e8e-157">Se il pixel shader restituisce la profondità, il valore di profondità viene duplicato per tutti i campioni (sebbene questo scenario perda il vantaggio del campionamento multiplo).</span><span class="sxs-lookup"><span data-stu-id="33e8e-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="33e8e-158">Quando il campionamento multiplo è disabilitato, il test profondità/stencil viene ancora eseguito per campione, ma la profondità non è interpolata per campione.</span><span class="sxs-lookup"><span data-stu-id="33e8e-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="33e8e-159">Non esistono restrizioni per combinare il rendering multicampionato e non multicampionato all'interno di una singola destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="33e8e-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="33e8e-160">Se si Abilita il campionamento multiplo e si crea una destinazione di rendering non multicampionata, si produce lo stesso risultato di se il multicampionamento non è stato abilitato; il campionamento viene eseguito con un singolo campione per pixel.</span><span class="sxs-lookup"><span data-stu-id="33e8e-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33e8e-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33e8e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e8e-162">Fase Rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="33e8e-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 