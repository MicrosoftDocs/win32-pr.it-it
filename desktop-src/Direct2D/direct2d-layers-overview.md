---
title: Panoramica sui livelli
description: Descrive le nozioni di base dei livelli Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, livelli
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0e86b32296718a975ebabccd5fc4ef0ee30cf289
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963287"
---
# <a name="layers-overview"></a><span data-ttu-id="37171-104">Panoramica sui livelli</span><span class="sxs-lookup"><span data-stu-id="37171-104">Layers Overview</span></span>

<span data-ttu-id="37171-105">Questa panoramica descrive le nozioni di base sull'uso dei livelli Direct2D.</span><span class="sxs-lookup"><span data-stu-id="37171-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="37171-106">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="37171-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="37171-107">Che cosa sono i livelli?</span><span class="sxs-lookup"><span data-stu-id="37171-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="37171-108">Livelli in Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="37171-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="37171-109">ID2D1DeviceContext e PushLayer</span><span class="sxs-lookup"><span data-stu-id="37171-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="37171-110">D2D1 \_ Layer \_ PARAMETERS1 e d2d1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="37171-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="37171-111">Modalità di fusione</span><span class="sxs-lookup"><span data-stu-id="37171-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="37171-112">Interazione</span><span class="sxs-lookup"><span data-stu-id="37171-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="37171-113">Creazione di livelli</span><span class="sxs-lookup"><span data-stu-id="37171-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="37171-114">Limiti del contenuto</span><span class="sxs-lookup"><span data-stu-id="37171-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="37171-115">Maschere geometriche</span><span class="sxs-lookup"><span data-stu-id="37171-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="37171-116">Maschere di opacità</span><span class="sxs-lookup"><span data-stu-id="37171-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="37171-117">Alternative ai livelli</span><span class="sxs-lookup"><span data-stu-id="37171-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="37171-118">Ritaglio di una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="37171-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="37171-119">Clip allineate asse</span><span class="sxs-lookup"><span data-stu-id="37171-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="37171-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37171-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="37171-121">Che cosa sono i livelli?</span><span class="sxs-lookup"><span data-stu-id="37171-121">What Are Layers?</span></span>

<span data-ttu-id="37171-122">I livelli, rappresentati da oggetti [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , consentono a un'applicazione di modificare un gruppo di operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="37171-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="37171-123">Si usa un livello eseguendone il push in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="37171-124">Le successive operazioni di disegno da parte della destinazione di rendering vengono indirizzate al livello.</span><span class="sxs-lookup"><span data-stu-id="37171-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="37171-125">Una volta terminato il livello, si "estrae" il livello dalla destinazione di rendering, che compone nuovamente il contenuto del livello nella destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="37171-126">Analogamente ai pennelli, i livelli sono risorse dipendenti dal dispositivo create dalle destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="37171-127">I livelli possono essere usati in qualsiasi destinazione di rendering nello stesso dominio delle risorse che contiene la destinazione di rendering che l'ha creata.</span><span class="sxs-lookup"><span data-stu-id="37171-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="37171-128">Tuttavia, una risorsa livello può essere usata solo da una destinazione di rendering alla volta.</span><span class="sxs-lookup"><span data-stu-id="37171-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="37171-129">Per ulteriori informazioni sulle risorse, vedere [Panoramica delle risorse](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="37171-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="37171-130">Sebbene i livelli offrano una tecnica di rendering potente per produrre effetti interessanti, un numero eccessivo di livelli in un'applicazione può influire negativamente sulle prestazioni, a causa dei diversi costi associati alla gestione di livelli e risorse del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="37171-131">Ad esempio, il costo del riempimento o della cancellazione del livello e la successiva fusione, soprattutto sull'hardware di fascia superiore.</span><span class="sxs-lookup"><span data-stu-id="37171-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="37171-132">Quindi, esiste il costo della gestione delle risorse del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="37171-133">Se questi vengono riallocati di frequente, i blocchi risultanti rispetto alla GPU saranno il problema più significativo.</span><span class="sxs-lookup"><span data-stu-id="37171-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="37171-134">Quando si progetta un'applicazione, provare a massimizzare il riutilizzo delle risorse di livello.</span><span class="sxs-lookup"><span data-stu-id="37171-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="37171-135">Livelli in Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="37171-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="37171-136">In Windows 8 sono state introdotte nuove API correlate ai livelli che semplificano, migliorano le prestazioni di e aggiungono funzionalità a livelli.</span><span class="sxs-lookup"><span data-stu-id="37171-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="37171-137">ID2D1DeviceContext e PushLayer</span><span class="sxs-lookup"><span data-stu-id="37171-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="37171-138">L'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) è derivata dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ed è fondamentale per visualizzare il contenuto Direct2D in Windows 8. per ulteriori informazioni su questa interfaccia, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="37171-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="37171-139">Con l'interfaccia del contesto di dispositivo, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare null al metodo [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="37171-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="37171-140">Direct2D gestisce automaticamente la risorsa livello e può condividere le risorse tra i livelli e i grafici degli effetti.</span><span class="sxs-lookup"><span data-stu-id="37171-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="37171-141">D2D1 \_ Layer \_ PARAMETERS1 e d2d1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="37171-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="37171-142">La [**struttura \_ \_ PARAMETERS1 di livello d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) è uguale a quella dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), ad eccezione del fatto che il membro finale della struttura è ora un'enumerazione [**d2d1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .</span><span class="sxs-lookup"><span data-stu-id="37171-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="37171-143">[**D2d1 \_ Il livello \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) non dispone di un'opzione ClearType e prevede due opzioni diverse che è possibile utilizzare per migliorare le prestazioni:</span><span class="sxs-lookup"><span data-stu-id="37171-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="37171-144">[**D2d1 \_ LIVELLO \_ OPTIONS1 \_ Inizializza \_ da \_ background**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D esegue il rendering delle primitive nel livello senza cancellarlo con un nero trasparente.</span><span class="sxs-lookup"><span data-stu-id="37171-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="37171-145">Questo non è il valore predefinito, ma nella maggior parte dei casi produce prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="37171-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="37171-146">[**D2d1 \_ LAYER \_ OPTIONS1 \_ Ignore \_ Alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): se la superficie sottostante è impostata su [**d2d1 \_ Alpha \_ mode \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), questa opzione consente a Direct2D di evitare di modificare il canale alfa del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="37171-147">Non utilizzarlo in altri casi.</span><span class="sxs-lookup"><span data-stu-id="37171-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="37171-148">Modalità di fusione</span><span class="sxs-lookup"><span data-stu-id="37171-148">Blend Modes</span></span>

<span data-ttu-id="37171-149">A partire da Windows 8, il contesto di dispositivo ha una [**modalità di Blend primitiva**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) che determina il modo in cui ogni primitiva viene fusa con la superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="37171-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="37171-150">Questa modalità si applica anche ai livelli quando si chiama il metodo [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="37171-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="37171-151">Se, ad esempio, si usa un livello per ritagliare le primitive con trasparenza, impostare la modalità di [**\_ \_ \_ copia primitiva di d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) nel contesto di dispositivo per ottenere risultati appropriati.</span><span class="sxs-lookup"><span data-stu-id="37171-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="37171-152">La modalità di copia rende il contesto di dispositivo lineare interpolare tutti i 4 canali dei colori, incluso il canale alfa, di ogni pixel con il contenuto della superficie di destinazione in base alla maschera geometrica del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="37171-153">Interazione</span><span class="sxs-lookup"><span data-stu-id="37171-153">Interoperation</span></span>

<span data-ttu-id="37171-154">A partire da Windows 8, Direct2D supporta l'interoperabilità con Direct3D e GDI mentre viene eseguito il push di un livello o di una clip.</span><span class="sxs-lookup"><span data-stu-id="37171-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="37171-155">È possibile chiamare [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) mentre viene eseguito il push di un livello per interagire con GDI.</span><span class="sxs-lookup"><span data-stu-id="37171-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="37171-156">È possibile chiamare [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) e quindi eseguire il rendering sulla superficie sottostante per interagire con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="37171-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="37171-157">È responsabilità dell'utente eseguire il rendering all'interno del livello o della clip con Direct3D o GDI.</span><span class="sxs-lookup"><span data-stu-id="37171-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="37171-158">Se si tenta di eseguire il rendering al di fuori del livello o di ritagliare i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="37171-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="37171-159">Creazione di livelli</span><span class="sxs-lookup"><span data-stu-id="37171-159">Creating Layers</span></span>

<span data-ttu-id="37171-160">Per lavorare con i livelli è necessaria una certa familiarità con i metodi [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) e con la struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , che contiene un set di dati parametrici che definiscono il modo in cui è possibile utilizzare il livello.</span><span class="sxs-lookup"><span data-stu-id="37171-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="37171-161">Nell'elenco seguente vengono descritti i metodi e la struttura.</span><span class="sxs-lookup"><span data-stu-id="37171-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="37171-162">Chiamare il metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare una risorsa livello.</span><span class="sxs-lookup"><span data-stu-id="37171-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="37171-163">A partire da Windows 8, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare null al metodo [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) sull'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="37171-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="37171-164">Si tratta di una soluzione più semplice che consente a Direct2D di gestire automaticamente la risorsa di livello e di condividere le risorse tra i livelli e i grafici di effetto.</span><span class="sxs-lookup"><span data-stu-id="37171-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="37171-165">Dopo che la destinazione di rendering ha iniziato a disegnare (dopo che è stato chiamato il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ), è possibile usare il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="37171-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="37171-166">Il metodo **PushLayer** aggiunge il livello specificato alla destinazione di rendering, in modo che la destinazione riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="37171-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="37171-167">Questo metodo accetta un oggetto [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) restituito chiamando [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e un *layerParameters* nella struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="37171-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="37171-168">Nella tabella seguente vengono descritti i campi della struttura.</span><span class="sxs-lookup"><span data-stu-id="37171-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="37171-169">Campo</span><span class="sxs-lookup"><span data-stu-id="37171-169">Field</span></span>                 | <span data-ttu-id="37171-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37171-170">Description</span></span>                                                                                                                                                                                                                                                                 |     |
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
    | <span data-ttu-id="37171-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="37171-171">**contentBounds**</span></span>     | <span data-ttu-id="37171-172">Limiti del contenuto del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-172">The content bounds of the layer.</span></span> <span data-ttu-id="37171-173">Non è garantito il rendering del contenuto al di fuori di questi limiti.</span><span class="sxs-lookup"><span data-stu-id="37171-173">Content outside these bounds is guaranteed not to render.</span></span> <span data-ttu-id="37171-174">Il valore predefinito di questo parametro è [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="37171-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="37171-175">Quando viene utilizzato il valore predefinito, i limiti del contenuto vengono effettivamente considerati i limiti della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |     |
    | <span data-ttu-id="37171-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="37171-176">**geometricMask**</span></span>     | <span data-ttu-id="37171-177">Opzionale Area, definita da un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), a cui deve essere ritagliato il livello.</span><span class="sxs-lookup"><span data-stu-id="37171-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="37171-178">Impostare su **null** se il livello non deve essere ritagliato in una geometria.</span><span class="sxs-lookup"><span data-stu-id="37171-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span>                                                                                           |     |
    | <span data-ttu-id="37171-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="37171-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="37171-180">Valore che specifica la modalità di anti-aliasing per la maschera geometrica specificata dal campo **geometricMask** .</span><span class="sxs-lookup"><span data-stu-id="37171-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span>                                                                                                                                                               |     |
    | <span data-ttu-id="37171-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="37171-181">**maskTransform**</span></span>     | <span data-ttu-id="37171-182">Valore che specifica la trasformazione applicata alla maschera geometrica quando si compone il livello.</span><span class="sxs-lookup"><span data-stu-id="37171-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="37171-183">Questa operazione è relativa alla trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="37171-183">This is relative to the world transform.</span></span>                                                                                                                               |     |
    | <span data-ttu-id="37171-184">**opacità**</span><span class="sxs-lookup"><span data-stu-id="37171-184">**opacity**</span></span>           | <span data-ttu-id="37171-185">Valore di opacità del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-185">The opacity value of the layer.</span></span> <span data-ttu-id="37171-186">L'opacità di ogni risorsa nel livello viene moltiplicata con questo valore durante la composizione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="37171-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>                                                                                                                                     |     |
    | <span data-ttu-id="37171-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="37171-187">**opacityBrush**</span></span>      | <span data-ttu-id="37171-188">Opzionale Pennello usato per modificare l'opacità del livello.</span><span class="sxs-lookup"><span data-stu-id="37171-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="37171-189">Il pennello viene mappato al livello e il canale alfa di ogni pixel del pennello mappato viene moltiplicato per il pixel del livello corrispondente.</span><span class="sxs-lookup"><span data-stu-id="37171-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="37171-190">Impostare su **null** se il livello non deve avere una maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="37171-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>    |     |
    | <span data-ttu-id="37171-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="37171-191">**layerOptions**</span></span>      | <span data-ttu-id="37171-192">Valore che specifica se il livello intende eseguire il rendering del testo con anti-aliasing ClearType.</span><span class="sxs-lookup"><span data-stu-id="37171-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="37171-193">Per impostazione predefinita, questo parametro è disattivato.</span><span class="sxs-lookup"><span data-stu-id="37171-193">This parameter defaults to off.</span></span> <span data-ttu-id="37171-194">La sua attivazione consente il corretto funzionamento di ClearType, ma comporta una velocità di rendering leggermente più lenta.</span><span class="sxs-lookup"><span data-stu-id="37171-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>                                          |     |

    

     

    > [!Note]  
    > <span data-ttu-id="37171-195">A partire da Windows 8, non è possibile eseguire il rendering con ClearType in un livello, quindi il parametro **layerOptions** deve essere sempre impostato su [**d2d1 \_ Layer \_ Options \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="37171-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="37171-196">Per praticità, Direct2D fornisce il metodo [**D2D1:: LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) per semplificare la creazione di strutture di [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="37171-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="37171-197">Per comporre il contenuto del livello nella destinazione di rendering, chiamare il metodo [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="37171-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="37171-198">Prima di chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , è necessario chiamare il metodo **PopLayer** .</span><span class="sxs-lookup"><span data-stu-id="37171-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="37171-199">Nell'esempio seguente viene illustrato come utilizzare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span><span class="sxs-lookup"><span data-stu-id="37171-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="37171-200">Tutti i campi nella struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sulle impostazioni predefinite, ad eccezione di **opacityBrush**, che è impostato su un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="37171-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="37171-201">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="37171-202">Si noti che quando si chiamano [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), assicurarsi che ogni **PushLayer** disponga di una chiamata **PopLayer** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="37171-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="37171-203">Se sono presenti più chiamate **PopLayer** rispetto alle chiamate di **PushLayer** , la destinazione di rendering viene inserita in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="37171-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="37171-204">Se [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato prima che vengano estratti tutti i livelli in attesa, la destinazione di rendering viene inserita in uno stato di errore e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="37171-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="37171-205">Per cancellare lo stato di errore, usare [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="37171-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="37171-206">Limiti del contenuto</span><span class="sxs-lookup"><span data-stu-id="37171-206">Content Bounds</span></span>

<span data-ttu-id="37171-207">**ContentBounds** imposta il limite di elementi da disegnare sul livello.</span><span class="sxs-lookup"><span data-stu-id="37171-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="37171-208">Solo gli elementi all'interno dei limiti del contenuto vengono ricomposti alla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="37171-209">Nell'esempio seguente viene illustrato come specificare **ContentBounds** in modo che l'immagine originale venga ritagliata nei limiti del contenuto con l'angolo superiore sinistro in corrispondenza di (10, 108) e l'angolo inferiore destro in (121, 177).</span><span class="sxs-lookup"><span data-stu-id="37171-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="37171-210">Nella figura seguente viene illustrata l'immagine originale e il risultato del ritaglio dell'immagine ai limiti del contenuto.</span><span class="sxs-lookup"><span data-stu-id="37171-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![illustrazione dei limiti del contenuto in un'immagine originale e nell'immagine ritagliata risultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="37171-212">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="37171-213">L'immagine ritagliata risultante viene interessata ulteriormente se si specifica un **geometricMask**.</span><span class="sxs-lookup"><span data-stu-id="37171-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="37171-214">Per ulteriori informazioni, vedere la sezione [maschere geometriche](#geometric-masks) .</span><span class="sxs-lookup"><span data-stu-id="37171-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="37171-215">Maschere geometriche</span><span class="sxs-lookup"><span data-stu-id="37171-215">Geometric Masks</span></span>

<span data-ttu-id="37171-216">Una maschera geometrica è una clip o un ritaglio, definito da un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , che maschera un livello quando viene disegnato da una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="37171-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="37171-217">È possibile usare il campo **geometricMask** della struttura [**\_ \_ parametri livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per mascherare i risultati in una geometria.</span><span class="sxs-lookup"><span data-stu-id="37171-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="37171-218">Se, ad esempio, si desidera visualizzare un'immagine mascherata da una lettera di blocco "A", è possibile creare innanzitutto una geometria che rappresenta la lettera di blocco "A" e utilizzare tale geometria come maschera geometrica per un livello.</span><span class="sxs-lookup"><span data-stu-id="37171-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="37171-219">Quindi, dopo aver eseguito il push del livello, è possibile creare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="37171-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="37171-220">Se si schiocca il livello, l'immagine viene ritagliata nella forma della lettera di blocco "A".</span><span class="sxs-lookup"><span data-stu-id="37171-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="37171-221">Nell'esempio seguente viene illustrato come creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contenente una forma di una montagna, quindi passare la geometria del percorso al [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="37171-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="37171-222">Quindi disegna una bitmap e i quadrati.</span><span class="sxs-lookup"><span data-stu-id="37171-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="37171-223">Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap bloccato per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="37171-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="37171-224">L'immagine seguente illustra l'output dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-224">The following illustration shows the output from the example.</span></span>

![illustrazione di un'immagine di una foglia e dell'immagine risultante dopo che è stata applicata una maschera geometrica di una montagna](images/layers-bitmapmask.png)

<span data-ttu-id="37171-226">Nel primo esempio viene definita la geometria da utilizzare come maschera.</span><span class="sxs-lookup"><span data-stu-id="37171-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="37171-227">Nell'esempio seguente viene usata la geometria come maschera per il livello.</span><span class="sxs-lookup"><span data-stu-id="37171-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="37171-228">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="37171-229">In generale, se si specifica un **geometricMask**, è possibile usare il valore predefinito [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)per **ContentBounds**.</span><span class="sxs-lookup"><span data-stu-id="37171-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="37171-230">Se **ContentBounds** è null e **geometricMask** è diverso da null, i limiti del contenuto sono in effetti i limiti della maschera geometrica dopo l'applicazione della trasformazione della maschera.</span><span class="sxs-lookup"><span data-stu-id="37171-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="37171-231">Se **ContentBounds** è diverso da null e **geometricMask** è diverso da null, la maschera geometrica trasformata viene effettivamente ritagliata rispetto ai limiti del contenuto e si presuppone che i limiti del contenuto siano infiniti.</span><span class="sxs-lookup"><span data-stu-id="37171-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="37171-232">Maschere di opacità</span><span class="sxs-lookup"><span data-stu-id="37171-232">Opacity Masks</span></span>

<span data-ttu-id="37171-233">Una maschera di opacità è una maschera, descritta da un pennello o una bitmap, applicata a un altro oggetto per rendere tale oggetto parzialmente o completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="37171-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="37171-234">Consente di utilizzare il canale alfa di un pennello da utilizzare come maschera di contenuto.</span><span class="sxs-lookup"><span data-stu-id="37171-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="37171-235">Ad esempio, è possibile definire un pennello a sfumatura radiale che varia da opaco a trasparente per creare un effetto vignette.</span><span class="sxs-lookup"><span data-stu-id="37171-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="37171-236">Nell'esempio seguente viene usato un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="37171-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="37171-237">Quindi disegna una bitmap e i quadrati.</span><span class="sxs-lookup"><span data-stu-id="37171-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="37171-238">Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap bloccato per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="37171-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="37171-239">La figura seguente mostra l'output di questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-239">The following illustration shows the output from this example.</span></span>

![illustrazione di un'immagine di alberi e dell'immagine risultante dopo l'applicazione di una maschera di opacità](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="37171-241">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37171-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="37171-242">Questo esempio usa un livello per applicare una maschera di opacità a un singolo oggetto per rendere l'esempio il più semplice possibile.</span><span class="sxs-lookup"><span data-stu-id="37171-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="37171-243">Quando si applica una maschera di opacità a un singolo oggetto, è più efficiente usare i metodi [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) o [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) anziché un livello.</span><span class="sxs-lookup"><span data-stu-id="37171-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="37171-244">Per istruzioni su come applicare una maschera di opacità senza usare un livello, vedere [Cenni preliminari sulle maschere di opacità](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37171-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="37171-245">Alternative ai livelli</span><span class="sxs-lookup"><span data-stu-id="37171-245">Alternatives to Layers</span></span>

<span data-ttu-id="37171-246">Come indicato in precedenza, un numero eccessivo di livelli può influire negativamente sulle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37171-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="37171-247">Per migliorare le prestazioni, evitare di usare i livelli laddove possibile; usare invece le alternative.</span><span class="sxs-lookup"><span data-stu-id="37171-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="37171-248">Nell'esempio di codice seguente viene illustrato come utilizzare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per ritagliare un'area, in alternativa all'utilizzo di un livello con limiti di contenuto.</span><span class="sxs-lookup"><span data-stu-id="37171-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="37171-249">Analogamente, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap clampato come alternativa all'uso di un livello con una maschera di opacità quando è presente un solo contenuto del livello di cui eseguire il rendering, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="37171-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="37171-250">In alternativa all'uso di un livello con una maschera geometrica, provare a usare una maschera di bitmap per ritagliare un'area, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="37171-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="37171-251">Infine, se si desidera applicare l'opacità a una singola primitiva, è necessario moltiplicare l'opacità nell'oggetto nel colore del pennello e quindi eseguire il rendering della primitiva.</span><span class="sxs-lookup"><span data-stu-id="37171-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="37171-252">Non è necessario un livello o una bitmap maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="37171-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="37171-253">Ritaglio di una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="37171-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="37171-254">La figura seguente mostra il risultato dell'applicazione di una clip a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="37171-254">The figure here shows the result of applying a clip to an image.</span></span>

![immagine che mostra un esempio di immagine prima e dopo un clip.](images/clip.png)

<span data-ttu-id="37171-256">È possibile ottenere questo risultato usando i livelli con una maschera di geometria o il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello di opacità.</span><span class="sxs-lookup"><span data-stu-id="37171-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="37171-257">Di seguito è riportato un esempio che usa un livello:</span><span class="sxs-lookup"><span data-stu-id="37171-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="37171-258">Di seguito è riportato un esempio che usa il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :</span><span class="sxs-lookup"><span data-stu-id="37171-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="37171-259">In questo esempio di codice, quando si chiama il metodo PushLayer, non si passa un livello creato dall'app.</span><span class="sxs-lookup"><span data-stu-id="37171-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="37171-260">Direct2D crea automaticamente un livello.</span><span class="sxs-lookup"><span data-stu-id="37171-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="37171-261">Direct2D è in grado di gestire l'allocazione e l'eliminazione di questa risorsa senza alcun intervento da parte dell'app.</span><span class="sxs-lookup"><span data-stu-id="37171-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="37171-262">Questo consente a Direct2D di riutilizzare i livelli internamente e di applicare le ottimizzazioni di gestione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="37171-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="37171-263">In Windows 8 sono state apportate numerose ottimizzazioni all'utilizzo dei livelli ed è consigliabile provare a usare le API di livello anziché [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) quando possibile.</span><span class="sxs-lookup"><span data-stu-id="37171-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="37171-264">Clip allineate asse</span><span class="sxs-lookup"><span data-stu-id="37171-264">Axis aligned clips</span></span>

<span data-ttu-id="37171-265">Se l'area da ritagliare è allineata all'asse della superficie di disegno, anziché arbitraria.</span><span class="sxs-lookup"><span data-stu-id="37171-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="37171-266">Questo caso è adatto per l'utilizzo di un rettangolo di ritaglio anziché di un livello.</span><span class="sxs-lookup"><span data-stu-id="37171-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="37171-267">Il miglioramento delle prestazioni è maggiore per la geometria con alias rispetto alla geometria con alias.</span><span class="sxs-lookup"><span data-stu-id="37171-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="37171-268">Per altre informazioni sulle clip allineate asse, vedere l'argomento [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="37171-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37171-269">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37171-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37171-270">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="37171-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 