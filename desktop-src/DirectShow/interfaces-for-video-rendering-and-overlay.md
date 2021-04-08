---
description: Interfacce per il rendering e la sovrapposizione di video
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Interfacce per il rendering e la sovrapposizione di video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747103"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="5ddf9-103">Interfacce per il rendering e la sovrapposizione di video</span><span class="sxs-lookup"><span data-stu-id="5ddf9-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="5ddf9-104">Queste interfacce supportano il controllo delle applicazioni sul rendering dei video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="5ddf9-105">Si noti che alcune di queste interfacce sono ora deprecate, perché il filtro renderer di mixaggio video fornisce un controllo di rendering e sovrapposizione superiore.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ddf9-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="5ddf9-106">Interface</span></span></th>
<th><span data-ttu-id="5ddf9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ddf9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ddf9-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-109">Consente di accedere alle informazioni e alle impostazioni con didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-111">Applicare effetti sovrapposti alla superficie del video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="5ddf9-112">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-114">Controllare il modo in cui DirectShow ridimensiona un'immagine video se la finestra del video è inferiore alla dimensione nativa del video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="5ddf9-115">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-117">Impostare le proprietà del video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-119">Esegue il rendering del video nella modalità a schermo intero esclusivo di Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="5ddf9-120">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-122">Interfaccia di callback per ricevere notifiche sulle modifiche alla posizione, alle dimensioni e alla visibilità della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="5ddf9-123">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-125">Disabilitare le funzionalità DirectDraw specificate.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="5ddf9-126">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-128">Accedere a una superficie DirectDraw allocata dal filtro della <a href="overlay-mixer-filter.md">sovrimpressione</a> . (Deprecato).</span><span class="sxs-lookup"><span data-stu-id="5ddf9-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-130">Implementato nel mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="5ddf9-131">Consente ai client privi di finestra, ad esempio i controlli ActiveX® di ottenere e impostare le proprietà del rettangolo video e di consigliare il filtro degli eventi.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-133">Implementato da client senza finestra e chiamato dal mixer overlay per inviare notifiche di eventi che interessano il rettangolo di visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-135">Impostare i controlli colore video sul filtro della sovrimpressione quando si combinano più flussi video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="5ddf9-136">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="5ddf9-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ddf9-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-138">Eseguire una query su un renderer video per ottenere informazioni sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ddf9-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="5ddf9-140">Imposta le proprietà della finestra video.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="5ddf9-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5ddf9-155">Interfacce video di combinazione di renderer 9.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5ddf9-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="5ddf9-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ddf9-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5ddf9-167">Interfacce video di combinazione di renderer 7.</span><span class="sxs-lookup"><span data-stu-id="5ddf9-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5ddf9-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ddf9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ddf9-169">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="5ddf9-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



