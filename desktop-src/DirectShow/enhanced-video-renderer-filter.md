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
# <a name="enhanced-video-renderer-filter"></a>Filtro renderer video migliorato

> [!Note]  
> Questo argomento si applica a Windows Vista e versioni successive.

 

Il filtro EVR (Enhanced video renderer) è un mixer video a 16 canali e un renderer. Ha la stessa funzionalità di base e il modello di plug-in come Media Foundation sink di supporto EVR.

Il filtro DirectShow EVR è documentato nella documentazione di Media Foundation SDK; per altre informazioni, vedere [renderer video migliorato](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro (tramite <strong>QueryInterface</strong>)</td>
<td>Interfacce DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
</ul>
Interfacce di Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Variabile, a seconda del driver della grafica.</td>
</tr>
<tr class="odd">
<td>Interfacce pin di input (tramite <strong>QueryInterface</strong>)</td>
<td>Interfacce DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul>
Interfacce di Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
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
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>File eseguibile</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Oltre alle interfacce esposte tramite **QueryInterface**, EVR espone altre interfacce tramite il metodo [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Alcune di queste interfacce sono implementate dal relatore EVR o dal mixer EVR, anziché da EVR. Se l'applicazione imposta un Presenter o un mixer personalizzato in EVR, le versioni personalizzate possono esporre un set di interfacce diverso.



| Oggetto     | Identificatore servizio                                              | Interfacce                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro EVR | \_Servizio di rendering video di Mr \_ \_ (query EVR o Presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro EVR | \_Servizio di accelerazione video di Mr \_ \_ (Presenter query)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro EVR | \_Servizio mixer video di Mr \_ \_ (mixer query)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Pin di input | \_ \_ servizio accelerazione video di Mr \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

EVR può combinare fino a 16 flussi video. Il primo flusso di input (pin 0) viene chiamato *flusso di riferimento*. Il flusso di riferimento viene sempre visualizzato per primo nell'ordine z. Tutti i flussi aggiuntivi sono denominati sottoflussi e sono combinati sopra il flusso di riferimento. L'applicazione può modificare l'ordine z dei sottoflussi, ma nessun sottoflusso può essere prima nell'ordine z.

Il driver di grafica determina quali formati video sono supportati, ma in genere sono limitati agli elementi seguenti:

-   Flusso di riferimento: YUV progressivo o interlacciato senza alfa per pixel, ad esempio NV12 o YUY2. o RGB progressivo.
-   Sottoflussi: YUV progressivo con l'alfa per pixel, ad esempio AYUV o AI44.

I formati dei sottoflussi disponibili possono dipendere dal formato del flusso di riferimento.

EVR trasmette i comandi Seek upstream tramite il pin 0. I pin dei sottoflussi non eseguono i comandi Seek. È responsabilità del filtro di origine o di barra di divisione mantenerli sincronizzati con il flusso di riferimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

