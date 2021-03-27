---
title: Configurazione della funzionalità Depth-Stencil
description: In questa sezione vengono illustrati i passaggi per configurare il buffer di stencil Depth e lo stato depth-stencil per la fase di Unione dell'output.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728743"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="2e2f3-103">Configurazione della funzionalità Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="2e2f3-104">In questa sezione vengono illustrati i passaggi per configurare il buffer di stencil Depth e lo stato depth-stencil per la fase di Unione dell'output.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="2e2f3-105">Creare una risorsa Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="2e2f3-106">Crea stato Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="2e2f3-107">Associare i dati Depth-Stencil alla fase OM</span><span class="sxs-lookup"><span data-stu-id="2e2f3-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="2e2f3-108">Quando si è a conoscenza di come utilizzare il buffer di stencil Depth e lo stato di stencil Depth corrispondente, fare riferimento alle [tecniche di stencil avanzati](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="2e2f3-109">Creare una risorsa Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="2e2f3-110">Creare il buffer di stencil Depth usando una risorsa di trama.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="2e2f3-111">Crea stato Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="2e2f3-112">Lo stato depth-stencil indica alla fase di Unione dell'output come eseguire il [test di stencil di profondità](d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="2e2f3-113">Il test di stencil Depth determina se deve essere disegnato o meno un pixel specificato.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="2e2f3-114">DepthEnable e StencilEnable abilitano (e disabilitano) la profondità e il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="2e2f3-115">Impostare DepthEnable su **false** per disabilitare il test di profondità e impedire la scrittura nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="2e2f3-116">Impostare StencilEnable su **false** per disabilitare il test dello stencil e impedire la scrittura nel buffer dello stencil. quando DepthEnable è **false** e StencilEnable è **true**, il test di profondità passa sempre nell'operazione dello stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="2e2f3-117">DepthEnable influisce solo sulla fase di Unione dell'output. non influisce sul ritaglio, sulla distorsione della profondità o sul fissaggio dei valori prima che i dati vengano inseriti in un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="2e2f3-118">Associare i dati Depth-Stencil alla fase OM</span><span class="sxs-lookup"><span data-stu-id="2e2f3-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="2e2f3-119">Associare lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="2e2f3-120">Associare la risorsa stencil Depth utilizzando una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="2e2f3-121">Una matrice di visualizzazioni di destinazione di rendering può essere passata in [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), tuttavia tutte le visualizzazioni di destinazione di rendering corrisponderanno a una singola vista depth stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="2e2f3-122">La matrice di destinazione di rendering in Direct3D 11 è una funzionalità che consente a un'applicazione di eseguire il rendering simultaneamente su più destinazioni di rendering a livello primitivo.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="2e2f3-123">Le matrici di destinazione di rendering offrono prestazioni migliori rispetto all'impostazione individuale di destinazioni di rendering con più chiamate a **sul ID3D11DeviceContext:: OMSetRenderTargets** (essenzialmente il metodo utilizzato in Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="2e2f3-124">Le destinazioni di rendering devono essere tutte dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="2e2f3-125">Se viene usato l'anti-aliasing di multicampionamento, tutti gli obiettivi di rendering associati e i buffer di profondità devono avere gli stessi conteggi di esempio.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="2e2f3-126">Quando un buffer viene usato come destinazione di rendering, i test di stencil Depth e più destinazioni di rendering non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="2e2f3-127">Fino a 8 destinazioni di rendering possono essere associati simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="2e2f3-128">Tutte le destinazioni di rendering devono avere le stesse dimensioni in tutte le dimensioni (larghezza e altezza e profondità per la dimensione 3D o della matrice per i \* tipi di matrice).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="2e2f3-129">Ogni destinazione di rendering può avere un formato dati diverso.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="2e2f3-130">Write Masks consente di controllare quali dati vengono scritti in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="2e2f3-131">Il controllo Write mask di output in una destinazione per rendering, a livello di componente, i dati vengono scritti nelle destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="2e2f3-132">Tecniche avanzate degli stencil</span><span class="sxs-lookup"><span data-stu-id="2e2f3-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="2e2f3-133">La parte stencil del buffer di stencil depth può essere usata per creare effetti di rendering, ad esempio composizione, derivazione e struttura.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="2e2f3-134">Composizione</span><span class="sxs-lookup"><span data-stu-id="2e2f3-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="2e2f3-135">Decaing</span><span class="sxs-lookup"><span data-stu-id="2e2f3-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="2e2f3-136">Strutture e sagome</span><span class="sxs-lookup"><span data-stu-id="2e2f3-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="2e2f3-137">Stencil a due lati</span><span class="sxs-lookup"><span data-stu-id="2e2f3-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="2e2f3-138">Lettura del buffer Depth-Stencil come trama</span><span class="sxs-lookup"><span data-stu-id="2e2f3-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="2e2f3-139">Composizione</span><span class="sxs-lookup"><span data-stu-id="2e2f3-139">Compositing</span></span>

<span data-ttu-id="2e2f3-140">L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="2e2f3-141">Una maschera nel buffer dello stencil viene utilizzata per occludere un'area della superficie di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="2e2f3-142">Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="2e2f3-143">In alternativa, l'applicazione è in grado di eseguire il rendering di primitive 3D nell'area mascherata dallo stencil della superficie di destinazione per il rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="2e2f3-144">È anche possibile eseguire il rendering di un'intera scena.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-144">It can even render an entire scene.</span></span>

<span data-ttu-id="2e2f3-145">I giochi spesso compostano contemporaneamente più scene 3D.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="2e2f3-146">Ad esempio, per la guida dei giochi viene in genere visualizzato un mirror di visualizzazione posteriore.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="2e2f3-147">Il mirror contiene la visualizzazione della scena 3D dietro il driver.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="2e2f3-148">Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in diretta del driver.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="2e2f3-149">Decaing</span><span class="sxs-lookup"><span data-stu-id="2e2f3-149">Decaling</span></span>

<span data-ttu-id="2e2f3-150">Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="2e2f3-151">Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="2e2f3-152">Ad esempio, quando si applicano segni di pneumatico e linee gialle a una carreggiata, i contrassegni devono essere visualizzati direttamente sopra la strada.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="2e2f3-153">Tuttavia, i valori z dei contrassegni e della strada sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="2e2f3-154">Il buffer di profondità potrebbe pertanto non produrre una netta separazione tra i due.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="2e2f3-155">È possibile che venga eseguito il rendering di alcuni pixel della primitiva in primo piano sulla primitiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="2e2f3-156">L'immagine risultante sembra riflessi da frame a frame.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="2e2f3-157">Questo effetto è detto z-Fighting o flimmering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="2e2f3-158">Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva di sfondo in cui verrà visualizzata la decalcomania.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="2e2f3-159">Disattivare la memorizzazione nel buffer z ed eseguire il rendering dell'immagine della primitiva di primo piano nell'area nascosta della superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="2e2f3-160">Per risolvere questo problema, è possibile usare più miscele di trame.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="2e2f3-161">Strutture e sagome</span><span class="sxs-lookup"><span data-stu-id="2e2f3-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="2e2f3-162">È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="2e2f3-163">Se l'applicazione esegue due passaggi di rendering, uno per generare la maschera dello stencil e il secondo per applicare la maschera dello stencil all'immagine, ma con le primitive leggermente più piccole alla seconda sessione, l'immagine risultante conterrà solo il contorno della primitiva.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="2e2f3-164">L'applicazione può quindi riempire l'area con maschera di stencil dell'immagine con un colore a tinta unita, assegnando alla primitiva un aspetto in rilievo.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="2e2f3-165">Se la maschera dello stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si sta eseguendo il rendering, l'immagine risultante contiene un foro in cui la primitiva deve essere.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="2e2f3-166">L'applicazione può quindi riempire il foro con il nero per produrre una silhouette della primitiva.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="2e2f3-167">Stencil Two-Sided</span><span class="sxs-lookup"><span data-stu-id="2e2f3-167">Two-Sided Stencil</span></span>

<span data-ttu-id="2e2f3-168">I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="2e2f3-169">Tramite l'applicazione vengono calcolati i volumi shadow di cui viene eseguito il cast dalla geometria occlusione, calcolando i bordi della siluetta e estrattando i bordi dalla luce in un set di volumi 3D.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="2e2f3-170">Questi volumi vengono quindi sottoposti a rendering due volte nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="2e2f3-171">Il primo rendering disegna i poligoni rivolte verso il futuro e incrementa i valori del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="2e2f3-172">Il secondo oggetto render disegna i poligoni sul retro del volume shadow e decrementa i valori del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="2e2f3-173">In genere, tutti i valori incrementati e decrementati vengono annullati. Tuttavia, la scena è già stata sottoposta a rendering con la geometria normale causando la mancata riuscita del test del buffer z durante il rendering del volume shadow.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="2e2f3-174">I valori rimanenti nel buffer dello stencil corrispondono ai pixel presenti nell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="2e2f3-175">Questi rimanenti contenuti del buffer dello stencil vengono usati come maschera, per alfa-blend di un quadrato nero di grandi dimensioni, che include tutto il doppio nella scena.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="2e2f3-176">Con il buffer dello stencil che funge da maschera, il risultato è quello di scurire i pixel presenti nelle ombreggiature.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="2e2f3-177">Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, di conseguenza la pressione sulla velocità effettiva del vertice della GPU.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="2e2f3-178">La funzionalità stencil a due lati è stata progettata per attenuare questa situazione.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="2e2f3-179">In questo approccio sono disponibili due set di stato dello stencil, denominati di seguito, uno per i triangoli in primo piano e l'altro per i triangoli rivolti verso il retro.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="2e2f3-180">In questo modo viene disegnato un solo passaggio per ogni volume ombreggiato, per luce.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="2e2f3-181">Un esempio di implementazione di stencil a due lati è disponibile nell' [esempio ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="2e2f3-182">Lettura del buffer Depth-Stencil come trama</span><span class="sxs-lookup"><span data-stu-id="2e2f3-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="2e2f3-183">Un buffer di stencil profondità inattivo può essere letto da uno shader come trama.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="2e2f3-184">Un'applicazione che legge un buffer di stencil Depth come trama esegue il rendering in due passaggi, il primo passaggio scrive nel buffer di stencil Depth e il secondo passaggio legge dal buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="2e2f3-185">Ciò consente a uno shader di confrontare i valori di profondità o stencil scritti in precedenza nel buffer rispetto al valore per il Currrently di pixel di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="2e2f3-186">Il risultato del confronto può essere utilizzato per creare effetti quali il mapping delle ombreggiature o le particelle morbide in un sistema particellare.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="2e2f3-187">Per creare un buffer di stencil depth che può essere usato come una risorsa di stencil di profondità e una risorsa shader, è necessario apportare alcune modifiche al codice di esempio nella sezione [creare una risorsa Depth-Stencil](#create-a-depth-stencil-resource) .</span><span class="sxs-lookup"><span data-stu-id="2e2f3-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="2e2f3-188">La risorsa di stencil Depth deve avere un formato privo di tipo, ad esempio DXGI \_ Format \_ R32 \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="2e2f3-189">La risorsa di stencil Depth deve usare sia i flag di profondità di binding D3D10 \_ \_ \_ che D3D10 \_ binding \_ shader \_ .</span><span class="sxs-lookup"><span data-stu-id="2e2f3-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="2e2f3-190">Inoltre, è necessario creare una visualizzazione delle risorse dello shader per il buffer di profondità usando una struttura [**desc di d3d11 \_ shader \_ Resource \_ View \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="2e2f3-191">La visualizzazione risorse dello shader utilizzerà un formato tipizzato, ad esempio **DXGI \_ Format \_ R32 \_ float** equivalente al formato non tipizzato specificato quando è stata creata la risorsa di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="2e2f3-192">Nel primo passaggio di rendering il buffer di profondità viene associato come descritto nella sezione [associare dati Depth-Stencil alla fase om](#bind-depth-stencil-data-to-the-om-stage) .</span><span class="sxs-lookup"><span data-stu-id="2e2f3-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="2e2f3-193">Si noti che il formato passato a [**d3d11 \_ Depth \_ stencil \_ View \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Format utilizzerà un formato tipizzato, ad esempio **DXGI \_ Format \_ D32 \_ float**.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="2e2f3-194">Dopo il primo passaggio di rendering, il buffer di profondità conterrà i valori di profondità per la scena.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="2e2f3-195">Nel secondo passaggio di rendering viene usata la funzione [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) per impostare la visualizzazione depth-stencil su **null** o una risorsa di stencil Depth diversa e la visualizzazione delle risorse dello shader viene passata allo shader usando [**ID3D11EffectShaderResourceVariable:: seresource**](id3dx11effectshaderresourcevariable-setresource.md).</span><span class="sxs-lookup"><span data-stu-id="2e2f3-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="2e2f3-196">Questo consente allo shader di cercare i valori di profondità calcolati nel primo passaggio di rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="2e2f3-197">Si noti che è necessario applicare una trasformazione per recuperare i valori di profondità se il punto di visualizzazione del primo passaggio di rendering è diverso dal secondo passaggio di rendering.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="2e2f3-198">Se, ad esempio, viene usata una tecnica di mapping Shadow, il primo passaggio di rendering sarà dalla prospettiva di una sorgente di luce mentre il secondo passaggio di rendering verrà dal punto di vista del visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="2e2f3-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e2f3-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e2f3-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e2f3-200">Output-fase di Unione</span><span class="sxs-lookup"><span data-stu-id="2e2f3-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="2e2f3-201">Fasi della pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2e2f3-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 