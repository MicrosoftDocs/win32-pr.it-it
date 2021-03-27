---
title: Uso del livello di debug per eseguire il debug di app
description: In questo articolo viene illustrato come abilitare il livello di debug e alcuni dei problemi che è possibile prevenire utilizzando il livello di debug.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708176"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="526e2-103">Uso del livello di debug per eseguire il debug di app</span><span class="sxs-lookup"><span data-stu-id="526e2-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="526e2-104">Si consiglia di usare il [livello di debug](overviews-direct3d-11-devices-layers.md) per eseguire il debug delle app per assicurarsi che siano puliti da errori e avvisi.</span><span class="sxs-lookup"><span data-stu-id="526e2-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="526e2-105">Il livello di debug consente di scrivere codice Direct3D.</span><span class="sxs-lookup"><span data-stu-id="526e2-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="526e2-106">Inoltre, la produttività può aumentare quando si usa il livello di debug, in quanto è possibile visualizzare immediatamente le cause degli errori di rendering oscuri o persino le schermate nere nell'origine.</span><span class="sxs-lookup"><span data-stu-id="526e2-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="526e2-107">Il livello di debug fornisce avvisi per molti problemi.</span><span class="sxs-lookup"><span data-stu-id="526e2-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="526e2-108">Ad esempio, il livello di debug fornisce avvisi per i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="526e2-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="526e2-109">Non è stato possibile impostare una trama ma è possibile leggerla nel pixel shader</span><span class="sxs-lookup"><span data-stu-id="526e2-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="526e2-110">Profondità di output senza associazione di stato depth-stencil</span><span class="sxs-lookup"><span data-stu-id="526e2-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="526e2-111">Creazione trama non riuscita con INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="526e2-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="526e2-112">In questo articolo viene illustrato come abilitare il [livello di debug](overviews-direct3d-11-devices-layers.md) e alcuni dei problemi che è possibile prevenire utilizzando il livello di debug.</span><span class="sxs-lookup"><span data-stu-id="526e2-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="526e2-113">Abilitazione del livello di debug</span><span class="sxs-lookup"><span data-stu-id="526e2-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="526e2-114">Prevenzione degli errori nell'app con il livello di debug</span><span class="sxs-lookup"><span data-stu-id="526e2-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="526e2-115">Non passare puntatori NULL a map</span><span class="sxs-lookup"><span data-stu-id="526e2-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="526e2-116">Casella origine limite all'interno delle risorse di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="526e2-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="526e2-117">Non eliminare DiscardResource o DiscardView</span><span class="sxs-lookup"><span data-stu-id="526e2-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="526e2-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="526e2-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="526e2-119">Abilitazione del livello di debug</span><span class="sxs-lookup"><span data-stu-id="526e2-119">Enabling the debug layer</span></span>

<span data-ttu-id="526e2-120">Per abilitare il [livello di debug](overviews-direct3d-11-devices-layers.md), specificare il flag [**d3d11 \_ Create \_ Device \_ debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) nel parametro *Flags* quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare il dispositivo di rendering.</span><span class="sxs-lookup"><span data-stu-id="526e2-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="526e2-121">Questo esempio di codice illustra come abilitare il livello di debug quando il progetto Microsoft Visual Studio si trova in una build di debug:</span><span class="sxs-lookup"><span data-stu-id="526e2-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="526e2-122">Prevenzione degli errori nell'app con il livello di debug</span><span class="sxs-lookup"><span data-stu-id="526e2-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="526e2-123">Se si utilizza l'API Direct3D 11 o si passano parametri non validi, l'output di debug del [livello di debug](overviews-direct3d-11-devices-layers.md) segnala un errore o un avviso.</span><span class="sxs-lookup"><span data-stu-id="526e2-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="526e2-124">È quindi possibile correggere l'errore.</span><span class="sxs-lookup"><span data-stu-id="526e2-124">You can then correct your mistake.</span></span> <span data-ttu-id="526e2-125">Verranno ora esaminati alcuni problemi di codifica che possono causare un comportamento indefinito o anche il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="526e2-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="526e2-126">È possibile intercettare e impedire tali problemi utilizzando il livello debug.</span><span class="sxs-lookup"><span data-stu-id="526e2-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="526e2-127">Non passare puntatori NULL a map</span><span class="sxs-lookup"><span data-stu-id="526e2-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="526e2-128">Se si passa **null** al parametro *PreSource* o *pMappedResource* del metodo [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , il comportamento di **Map** non è definito.</span><span class="sxs-lookup"><span data-stu-id="526e2-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="526e2-129">Se è stato creato un dispositivo che supporta solo il [livello di base](overviews-direct3d-11-devices-layers.md), i parametri non validi per la **mappa** possono causare l'arresto anomalo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="526e2-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="526e2-130">Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore in questa chiamata della **mappa** non valida.</span><span class="sxs-lookup"><span data-stu-id="526e2-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="526e2-131">Casella origine limite all'interno delle risorse di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="526e2-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="526e2-132">In una chiamata al metodo [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) la casella di origine deve trovarsi all'interno della risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="526e2-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="526e2-133">Gli offset di destinazione, (x, y e z) consentono l'offset della casella di origine durante la scrittura nella risorsa di destinazione, ma le dimensioni della casella di origine e degli offset devono essere comprese tra le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="526e2-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="526e2-134">Se si tenta di copiare al di fuori della risorsa di destinazione o di specificare una casella di origine maggiore della risorsa di origine, il comportamento di **CopySubresourceRegion** non è definito.</span><span class="sxs-lookup"><span data-stu-id="526e2-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="526e2-135">Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore in questa chiamata **CopySubresourceRegion** non valida.</span><span class="sxs-lookup"><span data-stu-id="526e2-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="526e2-136">I parametri non validi per **CopySubresourceRegion** causano un comportamento non definito e potrebbero comportare il rendering errato, il ritaglio, nessuna copia o persino la rimozione del dispositivo di rendering.</span><span class="sxs-lookup"><span data-stu-id="526e2-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="526e2-137">Non eliminare DiscardResource o DiscardView</span><span class="sxs-lookup"><span data-stu-id="526e2-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="526e2-138">Il runtime rilascia una chiamata a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a meno che non si crei correttamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="526e2-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="526e2-139">La risorsa passata a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve essere stata creata usando il [**\_ \_ valore predefinito di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o la [**\_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). in caso contrario, il runtime elimina la chiamata a **DiscardResource**.</span><span class="sxs-lookup"><span data-stu-id="526e2-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="526e2-140">La risorsa sottostante la visualizzazione passata a [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve essere stata creata usando il [**\_ \_ valore predefinito di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o la [**\_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). in caso contrario, il runtime elimina la chiamata a **DiscardView**.</span><span class="sxs-lookup"><span data-stu-id="526e2-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="526e2-141">Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore relativo alla chiamata eliminata.</span><span class="sxs-lookup"><span data-stu-id="526e2-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="526e2-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="526e2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="526e2-143">Livelli software</span><span class="sxs-lookup"><span data-stu-id="526e2-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




