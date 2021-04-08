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
# <a name="video-mixing-renderer-filter-9"></a>Filtro renderer di video mixing 9

In DirectX 9 il filtro video con combinazione del renderer 9 (VMR-9) offre funzionalità avanzate di rendering video su tutte le piattaforme supportate da DirectX. È completamente integrato con le funzionalità 3D di DirectX 9. Ad esempio, è possibile aggiungere facilmente video a giochi e altri ambienti 3D o trasformare immagini video usando i pixel shader Direct3D e altri effetti.

Questo filtro non supporta le porte video.

Per mantenere la compatibilità con le versioni precedenti, VMR-9 non è il renderer predefinito in alcun sistema. Per usare questo filtro, aggiungerlo al grafico filtro in modo esplicito e configurarlo prima di connettere i pin di input. VMR-9 utilizza un proprio set di interfacce, strutture ed enumerazioni, che non sono sempre identiche ai tipi di dati corrispondenti utilizzati con VMR-7.

VMR-9 supporta fino a 16 monitoraggi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td>VMR-9 supporta diverse modalità di rendering distinte. Supporta un set di interfacce diverso a seconda della modalità di rendering:<br/>
<ul>
<li>Tutte le modalità: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li>Modalità di rendering: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li>Modalità finestra: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li>Modalità senza finestra: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul>
Per impostare la modalità di rendering, chiamare <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: SetRenderingMode</strong></a>. Per ulteriori informazioni, vedere <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>I pin di input si connetteranno con qualsiasi tipo supportato dall'hardware video sottostante.</td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>iOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
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
<td>CLSID_VideoMixingRenderer9</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>N/D</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Un'applicazione può fornire un oggetto allocatore-Presenter personalizzato che espone le interfacce seguenti:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (facoltativo)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (facoltativo)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (facoltativo)

Per ulteriori informazioni sui Presenter-Presenter personalizzati, vedere la pagina relativa alla [fornitura di un Allocator-Presenter personalizzato per VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Un'applicazione può inoltre fornire un compositor plug-in personalizzato che espone l'interfaccia seguente:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Per configurare VMR con un compositor personalizzato, chiamare [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Uso del renderer video mixing](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




