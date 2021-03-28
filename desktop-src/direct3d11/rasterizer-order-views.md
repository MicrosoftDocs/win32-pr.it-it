---
title: Visualizzazioni degli ordini di rasterizzatore
description: Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118191"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="e73d0-103">Visualizzazioni degli ordini di rasterizzatore</span><span class="sxs-lookup"><span data-stu-id="e73d0-103">Rasterizer Order Views</span></span>

<span data-ttu-id="e73d0-104">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.</span><span class="sxs-lookup"><span data-stu-id="e73d0-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="e73d0-105">In questo modo è possibile utilizzare gli algoritmi OIT (Order Independent Transparency), che forniscono risultati di rendering migliori quando più oggetti trasparenti sono in linea tra loro in una vista.</span><span class="sxs-lookup"><span data-stu-id="e73d0-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="e73d0-106">Overview</span><span class="sxs-lookup"><span data-stu-id="e73d0-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="e73d0-107">Dettagli di implementazione</span><span class="sxs-lookup"><span data-stu-id="e73d0-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="e73d0-108">Riepilogo API</span><span class="sxs-lookup"><span data-stu-id="e73d0-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="e73d0-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73d0-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e73d0-110">Panoramica</span><span class="sxs-lookup"><span data-stu-id="e73d0-110">Overview</span></span>

<span data-ttu-id="e73d0-111">Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame che contengono la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="e73d0-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="e73d0-112">Oggetti quali recinzioni di trasmissione, fumo, incendi, vegetazione e vetro colorato usano la trasparenza per ottenere l'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="e73d0-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="e73d0-113">Si verificano problemi quando più trame che contengono la trasparenza sono allineate l'una all'altra (fumo davanti a una recinzione davanti a una costruzione di vetro che contiene la vegetazione, come esempio).</span><span class="sxs-lookup"><span data-stu-id="e73d0-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="e73d0-114">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono agli algoritmi OIT sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="e73d0-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="e73d0-115">La trasparenza viene gestita dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e73d0-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="e73d0-116">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.</span><span class="sxs-lookup"><span data-stu-id="e73d0-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="e73d0-117">Rov garantiscono l'ordine degli accessi UAV per qualsiasi coppia di chiamate pixel shader sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="e73d0-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="e73d0-118">In questo caso "sovrapposta" significa che le chiamate vengono generate dalle stesse chiamate di disegni e condividono la stessa coordinata pixel in modalità di esecuzione con frequenza in pixel e lo stesso pixel e la stessa coordinata di esempio in modalità frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="e73d0-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="e73d0-119">L'ordine in cui vengono eseguiti gli accessi ROV sovrapposti delle chiamate pixel shader è identico all'ordine in cui viene inviata la geometria.</span><span class="sxs-lookup"><span data-stu-id="e73d0-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="e73d0-120">Ciò significa che, per le chiamate di pixel shader sovrapposte, le Scritture ROV eseguite da una chiamata di pixel shader devono essere disponibili per essere lette da una chiamata successiva e non devono influire sulle letture da una chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="e73d0-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="e73d0-121">Le letture ROV eseguite da una chiamata di pixel shader devono riflettere le Scritture da una chiamata precedente e non devono riflettere le Scritture da una chiamata successiva.</span><span class="sxs-lookup"><span data-stu-id="e73d0-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="e73d0-122">Questa operazione è importante per UAV perché vengono omesse in modo esplicito dalle garanzie di invarianza dell'output normalmente impostate dall'ordine fisso dei risultati della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="e73d0-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="e73d0-123">Dettagli dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="e73d0-123">Implementation details</span></span>

<span data-ttu-id="e73d0-124">Le visualizzazioni ordinate del rasterizzatore (ROV) sono dichiarate con i nuovi oggetti HLSL (High Level Shader Language) seguenti e sono disponibili solo per l'pixel shader:</span><span class="sxs-lookup"><span data-stu-id="e73d0-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="e73d0-125">Usare questi oggetti allo stesso modo degli altri oggetti UAV, ad esempio e così `RWBuffer` via.</span><span class="sxs-lookup"><span data-stu-id="e73d0-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="e73d0-126">Riepilogo dell'API</span><span class="sxs-lookup"><span data-stu-id="e73d0-126">API summary</span></span>

<span data-ttu-id="e73d0-127">Rov sono un costrutto solo HLSL che applica una semantica di comportamento diversa a UAV.</span><span class="sxs-lookup"><span data-stu-id="e73d0-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="e73d0-128">Tutte le API rilevanti per UAV sono rilevanti anche per rov.</span><span class="sxs-lookup"><span data-stu-id="e73d0-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="e73d0-129">Si noti che il metodo, le strutture e la classe helper seguenti fanno riferimento al rasterizzatore:</span><span class="sxs-lookup"><span data-stu-id="e73d0-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="e73d0-130">[**D3d11 \_ RASTERIZZAtore \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : struttura che contiene la descrizione del rasterizzatore, notando la \_ \_ classe helper DESC2 CD3D12 rasterizzator per la creazione di descrizioni del rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="e73d0-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="e73d0-131">[**D3d11 \_ FEATURE \_ data \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : struttura che contiene il valore booleano `ROVsSupported` che indica il supporto.</span><span class="sxs-lookup"><span data-stu-id="e73d0-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="e73d0-132">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : metodo per accedere alle funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="e73d0-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e73d0-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73d0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e73d0-134">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="e73d0-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="e73d0-135">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="e73d0-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 