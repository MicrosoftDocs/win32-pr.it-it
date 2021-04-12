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
# <a name="video-mixing-renderer-filter-7"></a>Filtro renderer video mixing 7

Questo argomento si applica a Windows XP o versione successiva.

In Windows XP e versioni successive, il renderer video di mixaggio 7 (VMR-7) è il renderer video predefinito. Viene chiamato VMR-7 perché internamente USA DirectDraw 7. In DirectX 9, un filtro simile ma separato, VMR-9, è disponibile per la ridistribuzione nei sistemi non XP. VMR-9 utilizza Direct3D 9.

> [!Note]  
> VMR è disponibile in Windows XP e versioni successive. Non è disponibile tramite DirectX Redistributable o nelle versioni precedenti di Windows. Per la maggior parte degli scenari, le applicazioni devono usare il [renderer 9](video-mixing-renderer-filter-9.md)per la combinazione di video.

 

Le funzionalità di VMR includono:

-   Fusione alfa reale di un massimo di 16 flussi di input
-   Accesso all'immagine composita prima del rendering
-   Modello di plug-in che consente a terze parti di implementare effetti video personalizzati.
-   Supporto per un massimo di 15 monitoraggi.

Durante la creazione di Graph in Windows XP e versioni successive, il gestore del grafico del filtro non utilizzerà i filtri per il renderer video o il mixer sovrapposti precedenti, a meno che l'applicazione non li crei in modo esplicito e aggiunga al grafo.

Per ulteriori informazioni, vedere [using the video Mixing Renderer](using-the-video-mixing-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td>Tutte le modalità:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
</ul>
Modalità finestra:<br/>
<ul>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modalità senza finestra:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modalità di rendering:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
</ul>
Modalità Mixer:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
</ul>
Per informazioni sulle diverse modalità VMR-7, vedere <a href="vmr-modes-of-operation.md">modalità di funzionamento di VMR</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_VideoSubtype: dipende dall'hardware grafico. Deve essere un video non compresso.<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (vedere la sezione Osservazioni)</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>Al filtro sono associati due CLSID:
<ul>
<li>CLSID_VideoMixingRenderer: crea VMR-7. Se non sono disponibili risorse di sistema sufficienti per creare VMR-7, la chiamata a <strong>CoCreateInstance</strong> ha esito negativo.</li>
<li>CLSID_VideoRendererDefault: crea VMR-7 se sono disponibili risorse di sistema, altrimenti crea il vecchio filtro <a href="video-renderer-filter.md">renderer video</a> .</li>
</ul>
Usare CLSID_VideoMixingRenderer se sono necessarie le funzionalità specifiche di VMR-7. In caso contrario, utilizzare CLSID_VideoRendererDefault, che è quasi certo che non abbia esito negativo, in quanto viene eseguito il fallback al vecchio filtro renderer video.<br/></td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Non applicabile.</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Il pin di input espone l'interfaccia **iOverlay** solo quando il filtro VMR-7 è in modalità finestra. L'unico metodo **iOverlay** implementato dal pin è **GetWindowHandle**, che consente a un'applicazione di ottenere un handle per la finestra video del filtro. Tutti gli altri metodi **iOverlay** restituiscono E \_ NOTIMPL. In modalità senza finestra, il filtro non crea una finestra video, quindi il PIN non espone l'interfaccia.

Un'applicazione può fornire un oggetto allocatore-Presenter personalizzato che espone le interfacce seguenti:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (facoltativo)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (facoltativo)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (facoltativo)

Per ulteriori informazioni su Custom Allocator-Presenter, vedere la pagina relativa alla [fornitura di un Allocator-Presenter personalizzato per VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Un'applicazione può inoltre fornire un compositor plug-in personalizzato che espone l'interfaccia seguente:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Per configurare VMR con un compositor personalizzato, chiamare [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




