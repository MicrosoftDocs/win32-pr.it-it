---
description: Filtro renderer video mixing 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro renderer video mixing 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527811"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="6391e-103">Filtro renderer video mixing 7</span><span class="sxs-lookup"><span data-stu-id="6391e-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="6391e-104">Questo argomento si applica a Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6391e-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="6391e-105">In Windows XP e versioni successive, il renderer video di mixaggio 7 (VMR-7) è il renderer video predefinito.</span><span class="sxs-lookup"><span data-stu-id="6391e-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="6391e-106">Viene chiamato VMR-7 perché internamente USA DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="6391e-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="6391e-107">In DirectX 9, un filtro simile ma separato, VMR-9, è disponibile per la ridistribuzione nei sistemi non XP.</span><span class="sxs-lookup"><span data-stu-id="6391e-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="6391e-108">VMR-9 utilizza Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6391e-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="6391e-109">VMR è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6391e-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="6391e-110">Non è disponibile tramite DirectX Redistributable o nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="6391e-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="6391e-111">Per la maggior parte degli scenari, le applicazioni devono usare il [renderer 9](video-mixing-renderer-filter-9.md)per la combinazione di video.</span><span class="sxs-lookup"><span data-stu-id="6391e-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="6391e-112">Le funzionalità di VMR includono:</span><span class="sxs-lookup"><span data-stu-id="6391e-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="6391e-113">Fusione alfa reale di un massimo di 16 flussi di input</span><span class="sxs-lookup"><span data-stu-id="6391e-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="6391e-114">Accesso all'immagine composita prima del rendering</span><span class="sxs-lookup"><span data-stu-id="6391e-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="6391e-115">Modello di plug-in che consente a terze parti di implementare effetti video personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6391e-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="6391e-116">Supporto per un massimo di 15 monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="6391e-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="6391e-117">Durante la creazione di Graph in Windows XP e versioni successive, il gestore del grafico del filtro non utilizzerà i filtri per il renderer video o il mixer sovrapposti precedenti, a meno che l'applicazione non li crei in modo esplicito e aggiunga al grafo.</span><span class="sxs-lookup"><span data-stu-id="6391e-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="6391e-118">Per ulteriori informazioni, vedere [using the video Mixing Renderer](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6391e-119">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="6391e-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="6391e-120">Tutte le modalità:</span><span class="sxs-lookup"><span data-stu-id="6391e-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="6391e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="6391e-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="6391e-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="6391e-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="6391e-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="6391e-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="6391e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="6391e-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="6391e-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="6391e-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="6391e-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="6391e-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="6391e-133">Modalità finestra:</span><span class="sxs-lookup"><span data-stu-id="6391e-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="6391e-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="6391e-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="6391e-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="6391e-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="6391e-138">Modalità senza finestra:</span><span class="sxs-lookup"><span data-stu-id="6391e-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="6391e-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="6391e-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="6391e-141">Modalità di rendering:</span><span class="sxs-lookup"><span data-stu-id="6391e-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="6391e-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="6391e-143">Modalità Mixer:</span><span class="sxs-lookup"><span data-stu-id="6391e-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="6391e-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="6391e-145">Per informazioni sulle diverse modalità VMR-7, vedere <a href="vmr-modes-of-operation.md">modalità di funzionamento di VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="6391e-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6391e-146">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="6391e-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="6391e-147">Tipo principale: MEDIATYPE_VideoSubtype: dipende dall'hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="6391e-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="6391e-148">Deve essere un video non compresso.</span><span class="sxs-lookup"><span data-stu-id="6391e-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6391e-149">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="6391e-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="6391e-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="6391e-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="6391e-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (vedere la sezione Osservazioni)</span><span class="sxs-lookup"><span data-stu-id="6391e-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="6391e-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="6391e-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="6391e-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="6391e-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6391e-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6391e-157">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="6391e-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="6391e-158">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="6391e-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6391e-159">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="6391e-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="6391e-160">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="6391e-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6391e-161">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="6391e-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="6391e-162">Al filtro sono associati due CLSID:</span><span class="sxs-lookup"><span data-stu-id="6391e-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="6391e-163">CLSID_VideoMixingRenderer: crea VMR-7.</span><span class="sxs-lookup"><span data-stu-id="6391e-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="6391e-164">Se non sono disponibili risorse di sistema sufficienti per creare VMR-7, la chiamata a <strong>CoCreateInstance</strong> ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6391e-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="6391e-165">CLSID_VideoRendererDefault: crea VMR-7 se sono disponibili risorse di sistema, altrimenti crea il vecchio filtro <a href="video-renderer-filter.md">renderer video</a> .</span><span class="sxs-lookup"><span data-stu-id="6391e-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="6391e-166">Usare CLSID_VideoMixingRenderer se sono necessarie le funzionalità specifiche di VMR-7.</span><span class="sxs-lookup"><span data-stu-id="6391e-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="6391e-167">In caso contrario, utilizzare CLSID_VideoRendererDefault, che è quasi certo che non abbia esito negativo, in quanto viene eseguito il fallback al vecchio filtro renderer video.</span><span class="sxs-lookup"><span data-stu-id="6391e-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6391e-168">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="6391e-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="6391e-169">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="6391e-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6391e-170">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="6391e-170">Executable</span></span></td>
<td><span data-ttu-id="6391e-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6391e-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6391e-172"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="6391e-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="6391e-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="6391e-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6391e-174"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="6391e-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="6391e-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6391e-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6391e-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="6391e-176">Remarks</span></span>

<span data-ttu-id="6391e-177">Il pin di input espone l'interfaccia **iOverlay** solo quando il filtro VMR-7 è in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="6391e-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="6391e-178">L'unico metodo **iOverlay** implementato dal pin è **GetWindowHandle**, che consente a un'applicazione di ottenere un handle per la finestra video del filtro.</span><span class="sxs-lookup"><span data-stu-id="6391e-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="6391e-179">Tutti gli altri metodi **iOverlay** restituiscono E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6391e-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="6391e-180">In modalità senza finestra, il filtro non crea una finestra video, quindi il PIN non espone l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6391e-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="6391e-181">Un'applicazione può fornire un oggetto allocatore-Presenter personalizzato che espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="6391e-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="6391e-182">**IVMRImagePresenter**</span><span class="sxs-lookup"><span data-stu-id="6391e-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="6391e-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6391e-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="6391e-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6391e-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="6391e-185">**IVMRSurfaceAllocator**</span><span class="sxs-lookup"><span data-stu-id="6391e-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="6391e-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6391e-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="6391e-187">Per ulteriori informazioni su Custom Allocator-Presenter, vedere la pagina relativa alla [fornitura di un Allocator-Presenter personalizzato per VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="6391e-188">Un'applicazione può inoltre fornire un compositor plug-in personalizzato che espone l'interfaccia seguente:</span><span class="sxs-lookup"><span data-stu-id="6391e-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="6391e-189">**IVMRImageCompositor**</span><span class="sxs-lookup"><span data-stu-id="6391e-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="6391e-190">Per configurare VMR con un compositor personalizzato, chiamare [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="6391e-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6391e-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6391e-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6391e-192">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="6391e-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




