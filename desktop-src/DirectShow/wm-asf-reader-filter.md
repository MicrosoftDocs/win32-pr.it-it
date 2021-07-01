---
description: Informazioni sul filtro lettore ASF WM per DirectShow. Si tratta di un filtro wrapper per l'oggetto lettore fornito con Windows Media Format SDK.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro lettore ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330ab870b97fc3e84ccb5b0f726d4f35ef1af147
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118666"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro lettore ASF WM (DirectShow)

Wm ASF Reader è un filtro wrapper per l'oggetto lettore fornito con Windows Media Format SDK ed è il filtro di origine consigliato per la riproduzione di file del contenuto basato su Windows Media e del contenuto creato con uno dei DMO del codificatore MPEG-4 Microsoft.



| Etichetta | Valore |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) **IServiceProvider** Inoltre, il filtro espone le interfacce di Windows Media Format SDK seguenti: [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) [**IWMReaderAdvanced,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) [**IWMReaderAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (tramite **IServiceProvider)**<br/> |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfacce pin di output                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IAMWMBufferPass,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) **IServiceProvider** Inoltre, i pin espongono le interfacce di Windows Media Format SDK seguenti: **IWMStreamConfig2** (tramite **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| Filtro CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Merito](merit.md)                       | MERITO \_ IMPROBABILE                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Quando viene assegnato il nome di un file ASF o di un URL, il lettore ASF WM legge il contenuto compresso, analizza i flussi compressi ed espone un pin di output per ognuno di essi. Questo filtro connette downstream ai filtri codec audio e/o video, che esecutori della decompressione. La ricerca è supportata se il file ASF è ricercabile. Il lettore ASF contrassegna gli esempi prima di inviarli a valle, ma non modifica i timestamp in alcun modo.

La riproduzione a velocità diverse da 1.0 (come specificato in [**IMediaSeeking::SetRate)**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)non è supportata.

Quando il runtime di Windows Media Format SDK invia messaggi [**WMT \_ STATUS**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) al filtro WM ASF Writer, il filtro inoltra tutti i messaggi correlati all'acquisizione della licenza DRM come eventi [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md) Per altre informazioni, vedere [Reading DRM-Protected ASF Files in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Wm ASF Reader implementa parzialmente le [**interfacce IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) e [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) per concedere alle applicazioni l'accesso ai metodi in formato informativo sull'oggetto reader. L'implementazione del filtro passa semplicemente le chiamate all'interfaccia sull'oggetto lettore. I metodi di streaming non vengono implementati perché il filtro deve avere il controllo completo sul processo di streaming. Vengono implementati i metodi seguenti:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
