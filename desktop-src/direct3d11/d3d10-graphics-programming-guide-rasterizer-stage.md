---
title: Fase Rasterizzazione
description: La fase di rasterizzazione converte le informazioni vettoriali (costituite da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963590"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="0a149-103">Fase Rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="0a149-103">Rasterizer Stage</span></span>

<span data-ttu-id="0a149-104">La fase di rasterizzazione converte le informazioni vettoriali (costituite da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="0a149-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="0a149-105">Durante la rasterizzazione, ogni primitiva viene convertita in pixel, durante l'interpolazione dei valori per vertice in ogni primitiva.</span><span class="sxs-lookup"><span data-stu-id="0a149-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="0a149-106">La rasterizzazione include i vertici di ritaglio nella visualizzazione tronco, eseguendo una divisione per z per fornire prospettive, mapping primitive a un viewport 2D e determinare come richiamare il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0a149-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="0a149-107">Quando si usa un pixel shader è facoltativo, la fase di rasterizzazione esegue sempre il ritaglio, una prospettiva di divisione per trasformare i punti in uno spazio omogeneo ed esegue il mapping dei vertici al viewport.</span><span class="sxs-lookup"><span data-stu-id="0a149-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="0a149-108">Si presuppone che i vertici (x, y, z, w), che entrano nella fase di rasterizzazione, siano in uno spazio di ritaglio omogeneo.</span><span class="sxs-lookup"><span data-stu-id="0a149-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="0a149-109">In questo spazio delle coordinate l'asse X punta verso destra, Y punta verso l'alto e Z fuori dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="0a149-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="0a149-110">È possibile disabilitare la rasterizzazione indicando alla pipeline che non è presente alcun pixel shader (impostare la fase pixel shader su **null** con [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) e disabilitare il test di profondità e stencil (impostare **DepthEnable** e **StencilEnable** su **false** in [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="0a149-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="0a149-111">Mentre la rasterizzazione è disabilitata, i contatori della pipeline correlati non saranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="0a149-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="0a149-112">È inoltre disponibile una descrizione completa delle [regole di rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="0a149-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="0a149-113">Nell'hardware che implementa le ottimizzazioni del buffer Z gerarchico, è possibile abilitare il precaricamento del buffer z impostando la fase di pixel shader su **null** durante l'abilitazione del test di profondità ed stencil.</span><span class="sxs-lookup"><span data-stu-id="0a149-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="0a149-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0a149-114">In this section</span></span>



| <span data-ttu-id="0a149-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="0a149-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="0a149-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a149-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a149-117">Introduzione con la fase di rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="0a149-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="0a149-118">In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="0a149-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="0a149-119">Regole di rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="0a149-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="0a149-120">Le regole di rasterizzazione definiscono la modalità di mapping dei dati vettoriali nei dati raster.</span><span class="sxs-lookup"><span data-stu-id="0a149-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="0a149-121">I dati raster vengono bloccati in posizioni intere che vengono quindi rimosse e ritagliate (per tracciare il numero minimo di pixel) e gli attributi per pixel vengono interpolati (dagli attributi per vertice) prima di essere passati a una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0a149-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0a149-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a149-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a149-123">Pipeline grafica</span><span class="sxs-lookup"><span data-stu-id="0a149-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="0a149-124">Fasi della pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0a149-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

