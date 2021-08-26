---
description: Filtro del renderer di combinazione video 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro del renderer di combinazione video 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac39dfeab90fe97085c97b3a767f06d348a0f02
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466038"
---
# <a name="video-mixing-renderer-filter-7"></a>Filtro del renderer di combinazione video 7

Questo argomento si applica Windows XP o versioni successive.

In Windows XP e versioni successive, il renderer video predefinito è Video Mixing Renderer 7 (VMR-7). Viene chiamato VMR-7 perché usa internamente DirectDraw 7. In DirectX 9, un filtro simile ma separato, VMR-9, è disponibile per la ridistribuzione nei sistemi non XP. VMR-9 usa Direct3D 9.

> [!Note]  
> VmR è disponibile in Windows XP e versioni successive. Non è disponibile tramite DirectX Redistributable o nelle versioni precedenti di Windows. Per la maggior parte degli scenari, le applicazioni devono usare [il renderer di combinazione video 9.](video-mixing-renderer-filter-9.md)

 

Le funzionalità della macchina virtuale includono:

-   Vera fusione alfa di un massimo di 16 flussi di input
-   Accesso all'immagine composita prima del rendering
-   Modello plug-in che consente a terze parti di implementare effetti video personalizzati.
-   Supporto per un massimo di 15 monitor.

Durante la compilazione di grafi in Windows XP e versioni successive, Filter Graph Manager non userà i filtri meno recenti di Rendering video o Overlay Mixer, a meno che non vengano creati e aggiunti esplicitamente dall'applicazione al grafo.

Per altre informazioni, vedere [Uso del renderer di combinazione video.](using-the-video-mixing-renderer.md)




| | | Interfacce di filtro | Tutte le modalità:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Filtro IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>Modalità finestra:<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modalità senza finestra:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modalità senza rendering:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>Mixer predefinita:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>Per informazioni sulle varie modalità VMR-7, vedere <a href="vmr-modes-of-operation.md">Modalità operative di VMR.</a><br /> | | Tipi di supporti pin di input | Tipo principale: MEDIATYPE_VideoSubtype: dipende dall'hardware grafico. Deve essere un video non compresso.<br /> | | Interfacce pin di input | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (vedere la sezione Osservazioni)</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | | Tipi di supporti pin di output | Non applicabile. | | Interfacce pin di output | Non applicabile. | | Filtrare l'| CLSID A questo filtro sono associati due CLSID:<ul><li>CLSID_VideoMixingRenderer: crea VMR-7. Se le risorse di sistema non sono sufficienti per creare VMR-7, la chiamata a <strong>CoCreateInstance</strong> ha esito negativo.</li><li>CLSID_VideoRendererDefault: crea VMR-7 se sono disponibili risorse di sistema oppure crea il filtro <a href="video-renderer-filter.md">del renderer video</a> precedente.</li></ul>Usare CLSID_VideoMixingRenderer se sono necessarie le funzionalità specifiche di VMR-7. In caso contrario, CLSID_VideoRendererDefault, che è quasi certo di non avere esito negativo, perché viene eseguito il fall back al filtro del renderer video precedente.<br /> | | Proprietà pagina CLSID | Non applicabile. | | File eseguibili | Quartz.dll | | <a href="merit.md">|</a> MERIT_PREFERRED + 1 | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Il pin di input espone **l'interfaccia IOverlay** solo quando il filtro VMR-7 è in modalità finestra. **L'unico metodo IOverlay** implementato dal pin è **GetWindowHandle,** che consente a un'applicazione di ottenere un handle per la finestra video del filtro. Tutti gli **altri metodi IOverlay** restituiscono E \_ NOTIMPL. In modalità senza finestra, il filtro non crea una finestra video, quindi il segnaposto non espone l'interfaccia.

Un'applicazione può fornire un oggetto allocatore-presentatore personalizzato che espone le interfacce seguenti:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (facoltativo)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (facoltativo)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (facoltativo)

Per altre informazioni sugli allocator-presenter personalizzati, vedere [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)(Specifica di un Allocator-Presenter personalizzato per VMR-7).

Un'applicazione può anche fornire un provider di plug-in personalizzato che espone l'interfaccia seguente:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Per configurare vmr con un compositor personalizzato, chiamare [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




