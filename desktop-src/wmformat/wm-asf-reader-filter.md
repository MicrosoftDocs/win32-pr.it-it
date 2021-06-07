---
title: Filtro lettore ASF WM (Windows Media Format 11 SDK)
description: Informazioni sul filtro lettore ASF WM.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,Lettore ASF WM
- DirectShow, Lettore ASF WM
- Filtri QASF, Lettore ASF WM
- Lettore ASF WM
- Advanced Systems Format (ASF),Lettore ASF WM
- ASF (Advanced Systems Format),Lettore ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444282"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtro lettore ASF WM (Windows Media Format 11 SDK)

Quando viene specificato il nome di un file ASF o di un URL, il lettore ASF WM legge il contenuto compresso, analizza i flussi ed espone un pin di output per ognuno di essi. Questo filtro connette downstream al Windows Media Audio o Windows Media Video dmo, che esecuno la decompressione. La ricerca è supportata se il file ASF è ricercabile. Il lettore ASF WM applica timestamp agli esempi multimediali in base al timestamp nel file ASF, ma non modifica in alcun modo i timestamp. Internamente, il filtro usa l'oggetto lettore di Windows Media Format per leggere il contenuto basato su Windows Media.

> [!Note]  
> In DirectX SDK questo filtro non è il filtro di origine predefinito per i file ASF, quindi con tale SDK non è possibile usare questo filtro con il **metodo RenderFile.** È necessario aggiungerlo in modo esplicito al grafico dei filtri usando il relativo identificatore di classe (CLSID). Questo comportamento è diverso con Windows Media Format SDK. Quando si installano le librerie di runtime di Windows Media Format SDK, WM ASF Reader viene registrato come filtro predefinito per i file ASF.

 

La tabella seguente contiene informazioni sul filtro Lettore ASF WM, ad esempio le interfacce e i tipi di supporti supportati.



|  Filtrare le informazioni                      |  Tipi                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro      | **IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (implementato parzialmente. Vedere Osservazioni, **IWMReaderAdvanced2** (implementato parzialmente), **IWMDRMReader** (tramite **IServiceProvider)** |
| Tipi di supporti pin di input  | Non applicabile                                                                                                                                                                                                                                |
| Interfacce pin di input   | Non applicabile                                                                                                                                                                                                                                |
| Tipi di supporti pin di output | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                         |
| Tipo di formato            | **VIDEOINFOHEADER2 se** il contenuto è [*interlacciato;*](wmformat-glossary.md)in caso **contrario, VIDEOINFOHEADER**                                                                                                                    |
| Interfacce pin di output  | **IMediaSeeking,** **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (tramite **IServiceProvider**)                                                                                                                             |
| CLSID del filtro           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID pagina delle proprietà    | Nessuna pagina delle proprietà                                                                                                                                                                                                                              |
| File eseguibile             | Qasf.dll                                                                                                                                                                                                                                      |
| Merito                  | PROBABILITÀ \_ IMPROBABILE                                                                                                                                                                                                                               |
| Categoria filtro        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il lettore ASF WM implementa parzialmente le interfacce **IWMReaderAdvanced** e **IWMReaderAdvanced2** per consentire alle applicazioni di accedere ai metodi in formato informativo sull'oggetto lettore. L'implementazione del filtro passa semplicemente le chiamate all'interfaccia sull'oggetto reader. I metodi di streaming non vengono implementati perché il filtro deve avere il controllo completo sul processo di streaming. Vengono **implementati i metodi IWMReaderAdvanced** e **IWMReaderAdvanced2** seguenti:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lettura di file ASF in DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




