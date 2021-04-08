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
# <a name="interfaces-for-video-rendering-and-overlay"></a>Interfacce per il rendering e la sovrapposizione di video

Queste interfacce supportano il controllo delle applicazioni sul rendering dei video. Si noti che alcune di queste interfacce sono ora deprecate, perché il filtro renderer di mixaggio video fornisce un controllo di rendering e sovrapposizione superiore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Interfaccia</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Consente di accedere alle informazioni e alle impostazioni con didascalia chiusa.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></td>
<td>Applicare effetti sovrapposti alla superficie del video. (Deprecata)</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></td>
<td>Controllare il modo in cui DirectShow ridimensiona un'immagine video se la finestra del video è inferiore alla dimensione nativa del video. (Deprecata)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Impostare le proprietà del video.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></td>
<td>Esegue il rendering del video nella modalità a schermo intero esclusivo di Microsoft DirectDraw. (Deprecata)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></td>
<td>Interfaccia di callback per ricevere notifiche sulle modifiche alla posizione, alle dimensioni e alla visibilità della sovrimpressione. (Deprecata)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></td>
<td>Disabilitare le funzionalità DirectDraw specificate. (Deprecata)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></td>
<td>Accedere a una superficie DirectDraw allocata dal filtro della <a href="overlay-mixer-filter.md">sovrimpressione</a> . (Deprecato).</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></td>
<td>Implementato nel mixer overlay. Consente ai client privi di finestra, ad esempio i controlli ActiveX® di ottenere e impostare le proprietà del rettangolo video e di consigliare il filtro degli eventi.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></td>
<td>Implementato da client senza finestra e chiamato dal mixer overlay per inviare notifiche di eventi che interessano il rettangolo di visualizzazione video.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Impostare i controlli colore video sul filtro della sovrimpressione quando si combinano più flussi video. (Deprecata)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></td>
<td>Eseguire una query su un renderer video per ottenere informazioni sulle prestazioni.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></td>
<td>Imposta le proprietà della finestra video.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul></td>
<td>Interfacce video di combinazione di renderer 9.</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
</ul></td>
<td>Interfacce video di combinazione di renderer 7.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del renderer video mixing](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



