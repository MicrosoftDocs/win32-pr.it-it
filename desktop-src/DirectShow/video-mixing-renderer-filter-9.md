---
description: Filtro renderer di video mixing 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro renderer di video mixing 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757673"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="e67ea-103">Filtro renderer di video mixing 9</span><span class="sxs-lookup"><span data-stu-id="e67ea-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="e67ea-104">In DirectX 9 il filtro video con combinazione del renderer 9 (VMR-9) offre funzionalità avanzate di rendering video su tutte le piattaforme supportate da DirectX.</span><span class="sxs-lookup"><span data-stu-id="e67ea-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="e67ea-105">È completamente integrato con le funzionalità 3D di DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="e67ea-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="e67ea-106">Ad esempio, è possibile aggiungere facilmente video a giochi e altri ambienti 3D o trasformare immagini video usando i pixel shader Direct3D e altri effetti.</span><span class="sxs-lookup"><span data-stu-id="e67ea-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="e67ea-107">Questo filtro non supporta le porte video.</span><span class="sxs-lookup"><span data-stu-id="e67ea-107">This filter does not support video ports.</span></span>

<span data-ttu-id="e67ea-108">Per mantenere la compatibilità con le versioni precedenti, VMR-9 non è il renderer predefinito in alcun sistema.</span><span class="sxs-lookup"><span data-stu-id="e67ea-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="e67ea-109">Per usare questo filtro, aggiungerlo al grafico filtro in modo esplicito e configurarlo prima di connettere i pin di input.</span><span class="sxs-lookup"><span data-stu-id="e67ea-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="e67ea-110">VMR-9 utilizza un proprio set di interfacce, strutture ed enumerazioni, che non sono sempre identiche ai tipi di dati corrispondenti utilizzati con VMR-7.</span><span class="sxs-lookup"><span data-stu-id="e67ea-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="e67ea-111">VMR-9 supporta fino a 16 monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="e67ea-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e67ea-112">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="e67ea-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="e67ea-113">VMR-9 supporta diverse modalità di rendering distinte.</span><span class="sxs-lookup"><span data-stu-id="e67ea-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="e67ea-114">Supporta un set di interfacce diverso a seconda della modalità di rendering:</span><span class="sxs-lookup"><span data-stu-id="e67ea-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="e67ea-115">Tutte le modalità: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="e67ea-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="e67ea-116">Modalità di rendering: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="e67ea-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="e67ea-117">Modalità finestra: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="e67ea-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="e67ea-118">Modalità senza finestra: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="e67ea-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="e67ea-119">Per impostare la modalità di rendering, chiamare <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: SetRenderingMode</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e67ea-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="e67ea-120">Per ulteriori informazioni, vedere <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span><span class="sxs-lookup"><span data-stu-id="e67ea-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e67ea-121">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="e67ea-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="e67ea-122">I pin di input si connetteranno con qualsiasi tipo supportato dall'hardware video sottostante.</span><span class="sxs-lookup"><span data-stu-id="e67ea-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e67ea-123">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="e67ea-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="e67ea-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>iOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="e67ea-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e67ea-125">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="e67ea-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="e67ea-126">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="e67ea-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e67ea-127">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="e67ea-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="e67ea-128">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="e67ea-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e67ea-129">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="e67ea-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="e67ea-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="e67ea-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e67ea-131">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e67ea-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="e67ea-132">N/D</span><span class="sxs-lookup"><span data-stu-id="e67ea-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e67ea-133">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="e67ea-133">Executable</span></span></td>
<td><span data-ttu-id="e67ea-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e67ea-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e67ea-135"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="e67ea-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="e67ea-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="e67ea-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e67ea-137"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="e67ea-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="e67ea-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e67ea-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e67ea-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="e67ea-139">Remarks</span></span>

<span data-ttu-id="e67ea-140">Un'applicazione può fornire un oggetto allocatore-Presenter personalizzato che espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="e67ea-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="e67ea-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="e67ea-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="e67ea-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e67ea-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="e67ea-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="e67ea-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="e67ea-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e67ea-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="e67ea-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e67ea-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="e67ea-146">Per ulteriori informazioni sui Presenter-Presenter personalizzati, vedere la pagina relativa alla [fornitura di un Allocator-Presenter personalizzato per VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="e67ea-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="e67ea-147">Un'applicazione può inoltre fornire un compositor plug-in personalizzato che espone l'interfaccia seguente:</span><span class="sxs-lookup"><span data-stu-id="e67ea-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="e67ea-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="e67ea-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="e67ea-149">Per configurare VMR con un compositor personalizzato, chiamare [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="e67ea-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e67ea-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e67ea-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e67ea-151">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="e67ea-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e67ea-152">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="e67ea-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




