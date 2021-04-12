---
description: Filtro di lettura ASF WM
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro di lettura ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df563667ed614a238e8fb31e08a2d71c721c2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231894"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro di lettura ASF WM (DirectShow)

Il lettore ASF WM è un filtro wrapper per l'oggetto Reader fornito con Windows Media Format SDK ed è il filtro di origine consigliato per la riproduzione di contenuto basato su Windows Media e il contenuto creato con uno dei DMOs di Microsoft MPEG-4 Encoder.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider**, inoltre, il filtro espone le seguenti interfacce SDK del formato Windows Media: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (tramite **IServiceProvider**)<br/> |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipi di supporti pin di output                   | \_Video MEDIATYPE, \_ audio MEDIATYPE, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ filetransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfacce del PIN di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** inoltre, i pin espongono le seguenti interfacce SDK del formato Windows Media: **IWMStreamConfig2** (tramite **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| CLSID filtro                             | \_WMASFREADER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Quando si specifica il nome di un file ASF o un URL, il lettore WM ASF legge il contenuto compresso, analizza i flussi compressi ed espone un pin di output per ognuno di essi. Questo filtro si connette a valle ai filtri audio e/o video codecs, che eseguono la decompressione. La ricerca è supportata se il file ASF è ricercabile. Il tempo di lettura ASF timbra gli esempi prima di inviarli a valle, ma non modifica in alcun modo gli indicatori temporali.

La riproduzione a velocità diverse da 1,0 (come specificato in [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) non è supportata.

Quando il runtime di Windows Media Format SDK invia messaggi di [**\_ stato WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) al filtro del writer ASF WM, il filtro inoltra tutti i messaggi correlati all'acquisizione della licenza DRM come eventi di [**\_ \_ evento WMT EC**](ec-wmt-event.md) . Per ulteriori informazioni, vedere la pagina relativa alla [lettura dei file ASF DRM-Protected in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Il lettore WM ASF implementa parzialmente le interfacce [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) e [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) per consentire alle applicazioni di accedere ai metodi informativi nell'oggetto Reader. L'implementazione del filtro passa semplicemente le chiamate attraverso all'interfaccia sull'oggetto Reader. I metodi di streaming non sono implementati perché il filtro deve avere il controllo completo sul processo di streaming. Vengono implementati i metodi seguenti:

-   [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
