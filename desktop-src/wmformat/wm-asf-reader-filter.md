---
title: Filtro di lettura ASF WM (Windows Media Format 11 SDK)
description: Filtro di lettura ASF WM
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF Reader
- DirectShow, WM ASF Reader
- Filtri QASF, lettore ASF WM
- Lettore ASF WM
- ASF (Advanced Systems Format), lettore WM ASF
- ASF (formato avanzato dei sistemi), lettore WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739383"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtro di lettura ASF WM (Windows Media Format 11 SDK)

Quando si specifica il nome di un file ASF o un URL, il lettore WM ASF legge il contenuto compresso, analizza i flussi ed espone un pin di output per ciascuno di essi. Questo filtro si connette a valle al Windows Media Audio o Windows Media Video DMOs, che eseguono la decompressione. La ricerca è supportata se il file ASF è ricercabile. Il lettore WM ASF applica timestamp agli esempi di supporti basati sul timestamp nel file ASF, ma non modifica in alcun modo i timestamp. Internamente, il filtro usa l'oggetto lettore Windows Media Format per leggere il contenuto basato su Windows Media.

> [!Note]  
> In DirectX SDK, questo filtro non è il filtro di origine predefinito per i file ASF, quindi con tale SDK non è possibile usare questo filtro con il metodo **RenderFile** . è necessario aggiungerlo in modo esplicito al grafico di filtro utilizzando il relativo identificatore di classe (CLSID). Questo comportamento è diverso con Windows Media Format SDK. Quando si installano le librerie di runtime di Windows Media Format SDK, il lettore WM ASF viene registrato come filtro predefinito per i file ASF.

 

La tabella seguente contiene informazioni sul filtro WM ASF Reader, ad esempio le interfacce e i tipi di supporto supportati.



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementato parzialmente. Vedere la sezione Osservazioni.), **IWMReaderAdvanced2** (parzialmente implementato), **IWMDRMReader** (tramite **IServiceProvider**) |
| Tipi di supporti pin di input  | Non applicabile                                                                                                                                                                                                                                |
| Interfacce pin di input   | Non applicabile                                                                                                                                                                                                                                |
| Tipi di supporti pin di output | \_Video MEDIATYPE, \_ audio MEDIATYPE, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ filetransfer                                                                                                                                                         |
| Tipo di formato            | **VIDEOINFOHEADER2** se il contenuto è [*interlacciato*](wmformat-glossary.md), in caso contrario **VIDEOINFOHEADER**                                                                                                                    |
| Interfacce del PIN di output  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (tramite **IServiceProvider**)                                                                                                                             |
| CLSID filtro           | \_WMASFREADER CLSID                                                                                                                                                                                                                            |
| CLSID della pagina delle proprietà    | Nessuna pagina delle proprietà                                                                                                                                                                                                                              |
| File eseguibile             | Qasf.dll                                                                                                                                                                                                                                      |
| Merito                  | VALORE \_ improbabile                                                                                                                                                                                                                               |
| Categoria filtro        | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il lettore WM ASF implementa parzialmente le interfacce **IWMReaderAdvanced** e **IWMReaderAdvanced2** per consentire alle applicazioni di accedere ai metodi informativi nell'oggetto Reader. L'implementazione del filtro passa semplicemente le chiamate attraverso all'interfaccia sull'oggetto Reader. I metodi di streaming non sono implementati perché il filtro deve avere il controllo completo sul processo di streaming. Vengono implementati i seguenti metodi **IWMReaderAdvanced** e **IWMReaderAdvanced2** :

-   [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lettura di file ASF in DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




