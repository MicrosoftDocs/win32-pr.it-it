---
description: Filtro renderer di combinazione video 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro renderer di combinazione video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2077679599db45ab80e7be931a83f500c156405c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466588"
---
# <a name="video-mixing-renderer-filter-9"></a>Filtro renderer di combinazione video 9

In DirectX 9 il filtro Video Mixing Renderer 9 (VMR-9) offre funzionalità avanzate di rendering video in tutte le piattaforme supportate da DirectX. È completamente integrato con le funzionalità directx 9 3D. Ad esempio, è possibile aggiungere facilmente video a giochi e altri ambienti 3D o trasformare immagini video usando i pixel shader Direct3D e altri effetti.

Questo filtro non supporta le porte video.

Per mantenere la compatibilità con le versioni precedenti, VMR-9 non è il renderer predefinito in alcun sistema. Per usare questo filtro, aggiungerlo al grafico dei filtri in modo esplicito e configurarlo prima di connettere uno dei relativi pin di input. VmR-9 usa un proprio set di interfacce, strutture ed enumerazioni, che non sono sempre identiche ai tipi di dati corrispondenti usati con VMR-7.

VmR-9 supporta fino a 16 monitor.




| | | Filtrare le interfacce | VMR-9 supporta diverse modalità di rendering distinte. Supporta un set diverso di interfacce a seconda della modalità di rendering:<br /><ul><li>Tutte le modalità: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Modalità senza rendering: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Modalità finestra: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Modalità senza finestra: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Per impostare la modalità di rendering, chiamare <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>. Per altre informazioni, vedere <a href="vmr-modes-of-operation.md">Modalità operative vmr.</a><br /> | | Tipi di supporti pin di input | I pin di input si connetteranno a qualsiasi tipo supportato dall'hardware video sottostante. | | Interfacce pin di input | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | | Tipi di supporti pin di output | Non applicabile. | | Interfacce pin di output | Non applicabile. | | Filtrare i | CLSID CLSID_VideoMixingRenderer9 | | ClSID della pagina delle proprietà | N/D | | File eseguibile | Quartz.dll | | <a href="merit.md">Merito</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Un'applicazione può fornire un oggetto allocatore-presenter personalizzato che espone le interfacce seguenti:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (facoltativo)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (facoltativo)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (facoltativo)

Per altre informazioni sugli allocator-presenter personalizzati, vedere [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Un'applicazione può anche fornire un compositore plug-in personalizzato che espone l'interfaccia seguente:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Per configurare la macchina virtuale con un compositore personalizzato, chiamare [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Uso del renderer di combinazione video](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




