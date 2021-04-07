---
description: Il filtro EVR (Enhanced video renderer) è un mixer video a 16 canali e un renderer. Ha la stessa funzionalità di base e il modello di plug-in come Media Foundation sink di supporto EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro renderer video migliorato
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048970"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="03230-104">Filtro renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="03230-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="03230-105">Questo argomento si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="03230-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="03230-106">Il filtro EVR (Enhanced video renderer) è un mixer video a 16 canali e un renderer.</span><span class="sxs-lookup"><span data-stu-id="03230-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="03230-107">Ha la stessa funzionalità di base e il modello di plug-in come Media Foundation sink di supporto EVR.</span><span class="sxs-lookup"><span data-stu-id="03230-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="03230-108">Il filtro DirectShow EVR è documentato nella documentazione di Media Foundation SDK; per altre informazioni, vedere [renderer video migliorato](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="03230-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03230-109">Interfacce di filtro (tramite <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="03230-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="03230-110">Interfacce DirectShow:</span><span class="sxs-lookup"><span data-stu-id="03230-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="03230-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="03230-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="03230-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="03230-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="03230-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="03230-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="03230-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="03230-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="03230-119">Interfacce di Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="03230-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="03230-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="03230-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="03230-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="03230-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03230-124">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="03230-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="03230-125">Variabile, a seconda del driver della grafica.</span><span class="sxs-lookup"><span data-stu-id="03230-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03230-126">Interfacce pin di input (tramite <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="03230-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="03230-127">Interfacce DirectShow:</span><span class="sxs-lookup"><span data-stu-id="03230-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="03230-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="03230-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="03230-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="03230-131">Interfacce di Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="03230-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="03230-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="03230-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="03230-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="03230-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03230-135">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="03230-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="03230-136">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="03230-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03230-137">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="03230-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="03230-138">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="03230-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03230-139">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="03230-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="03230-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="03230-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03230-141">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="03230-141">Executable</span></span></td>
<td><span data-ttu-id="03230-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="03230-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03230-143"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="03230-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="03230-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="03230-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03230-145"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="03230-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="03230-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="03230-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="03230-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="03230-147">Remarks</span></span>

<span data-ttu-id="03230-148">Oltre alle interfacce esposte tramite **QueryInterface**, EVR espone altre interfacce tramite il metodo [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="03230-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="03230-149">Alcune di queste interfacce sono implementate dal relatore EVR o dal mixer EVR, anziché da EVR.</span><span class="sxs-lookup"><span data-stu-id="03230-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="03230-150">Se l'applicazione imposta un Presenter o un mixer personalizzato in EVR, le versioni personalizzate possono esporre un set di interfacce diverso.</span><span class="sxs-lookup"><span data-stu-id="03230-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="03230-151">Oggetto</span><span class="sxs-lookup"><span data-stu-id="03230-151">Object</span></span>     | <span data-ttu-id="03230-152">Identificatore servizio</span><span class="sxs-lookup"><span data-stu-id="03230-152">Service Identifier</span></span>                                              | <span data-ttu-id="03230-153">Interfacce</span><span class="sxs-lookup"><span data-stu-id="03230-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03230-154">Filtro EVR</span><span class="sxs-lookup"><span data-stu-id="03230-154">EVR filter</span></span> | <span data-ttu-id="03230-155">\_Servizio di rendering video di Mr \_ \_ (query EVR o Presenter)</span><span class="sxs-lookup"><span data-stu-id="03230-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="03230-156">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="03230-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="03230-157">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="03230-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="03230-158">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="03230-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="03230-159">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="03230-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="03230-160">Filtro EVR</span><span class="sxs-lookup"><span data-stu-id="03230-160">EVR filter</span></span> | <span data-ttu-id="03230-161">\_Servizio di accelerazione video di Mr \_ \_ (Presenter query)</span><span class="sxs-lookup"><span data-stu-id="03230-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="03230-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="03230-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="03230-163">Filtro EVR</span><span class="sxs-lookup"><span data-stu-id="03230-163">EVR filter</span></span> | <span data-ttu-id="03230-164">\_Servizio mixer video di Mr \_ \_ (mixer query)</span><span class="sxs-lookup"><span data-stu-id="03230-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="03230-165">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="03230-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="03230-166">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="03230-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="03230-167">**IMFVideoMixerControl**</span><span class="sxs-lookup"><span data-stu-id="03230-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="03230-168">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="03230-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="03230-169">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="03230-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="03230-170">Pin di input</span><span class="sxs-lookup"><span data-stu-id="03230-170">Input pins</span></span> | <span data-ttu-id="03230-171">\_ \_ servizio accelerazione video di Mr \_</span><span class="sxs-lookup"><span data-stu-id="03230-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="03230-172">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03230-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="03230-173">EVR può combinare fino a 16 flussi video.</span><span class="sxs-lookup"><span data-stu-id="03230-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="03230-174">Il primo flusso di input (pin 0) viene chiamato *flusso di riferimento*.</span><span class="sxs-lookup"><span data-stu-id="03230-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="03230-175">Il flusso di riferimento viene sempre visualizzato per primo nell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="03230-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="03230-176">Tutti i flussi aggiuntivi sono denominati sottoflussi e sono combinati sopra il flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="03230-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="03230-177">L'applicazione può modificare l'ordine z dei sottoflussi, ma nessun sottoflusso può essere prima nell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="03230-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="03230-178">Il driver di grafica determina quali formati video sono supportati, ma in genere sono limitati agli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="03230-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="03230-179">Flusso di riferimento: YUV progressivo o interlacciato senza alfa per pixel, ad esempio NV12 o YUY2. o RGB progressivo.</span><span class="sxs-lookup"><span data-stu-id="03230-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="03230-180">Sottoflussi: YUV progressivo con l'alfa per pixel, ad esempio AYUV o AI44.</span><span class="sxs-lookup"><span data-stu-id="03230-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="03230-181">I formati dei sottoflussi disponibili possono dipendere dal formato del flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="03230-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="03230-182">EVR trasmette i comandi Seek upstream tramite il pin 0.</span><span class="sxs-lookup"><span data-stu-id="03230-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="03230-183">I pin dei sottoflussi non eseguono i comandi Seek.</span><span class="sxs-lookup"><span data-stu-id="03230-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="03230-184">È responsabilità del filtro di origine o di barra di divisione mantenerli sincronizzati con il flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="03230-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="03230-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03230-185">Requirements</span></span>



| <span data-ttu-id="03230-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="03230-186">Requirement</span></span> | <span data-ttu-id="03230-187">Valore</span><span class="sxs-lookup"><span data-stu-id="03230-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03230-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03230-188">Minimum supported client</span></span><br/> | <span data-ttu-id="03230-189">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03230-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03230-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03230-190">Minimum supported server</span></span><br/> | <span data-ttu-id="03230-191">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03230-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03230-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03230-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03230-193">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="03230-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

