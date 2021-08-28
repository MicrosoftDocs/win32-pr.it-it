---
description: Il filtro Enhanced Video Renderer (EVR) è un mixer video a 16 canali e un renderer. Ha la stessa funzionalità di base e lo stesso modello di plug-in del sink Media Foundation multimediale EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro renderer video avanzato
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed63ba80864f98012a178ed775e5812ee5abe88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475527"
---
# <a name="enhanced-video-renderer-filter"></a>Filtro renderer video avanzato

> [!Note]  
> Questo argomento si applica a Windows Vista e versioni successive.

 

Il filtro Enhanced Video Renderer (EVR) è un mixer video a 16 canali e un renderer. Ha la stessa funzionalità di base e lo stesso modello di plug-in del sink Media Foundation multimediale EVR.

Il DirectShow EVR è documentato nella documentazione di Media Foundation SDK. Per altre informazioni, vedere [Renderer video avanzato](../medfound/enhanced-video-renderer.md).




| | | Filtrare le interfacce (tramite <strong>QueryInterface)</strong>| DirectShow interfacce:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li></ul>Media Foundation interfacce:<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li></ul> | | Tipi di supporti pin di input | Variabile, a seconda del driver di grafica. | | Interfacce pin di input (tramite <strong>QueryInterface)</strong>| DirectShow interfacce:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul>Media Foundation interfacce:<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li></ul> | | Tipi di supporti pin di output | Non applicabile. | | Interfacce pin di output | Non applicabile. | | Filtrare i | CLSID CLSID_EnhancedVideoRenderer | | File eseguibile | evr.dll | | <a href="merit.md">Merito</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Oltre alle interfacce esposte tramite **QueryInterface,** l'EVR espone altre interfacce tramite il [**metodo IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Alcune di queste interfacce vengono implementate dal presentatore EVR o dal mixer EVR, anziché dall'EVR stesso. Se l'applicazione imposta un presenter o un mixer personalizzato nel EVR, le versioni personalizzate potrebbero esporre un set diverso di interfacce.



| Oggetto     | Identificatore del servizio                                              | Interfacce                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro EVR | MR \_ VIDEO RENDER SERVICE \_ \_ (esegue query su EVR o presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro EVR | SERVIZIO DI \_ \_ ACCELERAZIONE VIDEO MR \_ (presentatore di query)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro EVR | MR \_ VIDEO \_ MIXER SERVICE \_ (mixer di query)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Pin di input | SERVIZIO DI \_ \_ ACCELERAZIONE VIDEO \_ MR                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

L'EVR può combinare fino a 16 flussi video. Il primo flusso di input (pin 0) è denominato *flusso di riferimento*. Il flusso di riferimento viene sempre visualizzato per primo nell'ordine z. Tutti i flussi aggiuntivi sono denominati flussi secondari e vengono misti all'inizio del flusso di riferimento. L'applicazione può modificare l'ordine z dei sottostream, ma nessun flusso secondario può essere prima nell'ordine z.

Il driver di grafica determina quali formati video sono supportati, ma in genere sono limitati ai seguenti:

-   Flusso di riferimento: YUV progressivo o interlacciato senza alfa per pixel (ad esempio NV12 o YUY2); o RGB progressivo.
-   Sottostream: YUV progressivo con alfa per pixel, ad esempio AYUV o AI44.

I formati di flusso secondari disponibili possono dipendere dal formato del flusso di riferimento.

L'EVR inoltra i comandi di ricerca a monte fino al pin 0. I pin del flusso secondario non inoltrano i comandi di ricerca. È responsabilità del filtro di origine o della barra di divisione mantenere sincronizzati i flussi secondari con il flusso di riferimento.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

