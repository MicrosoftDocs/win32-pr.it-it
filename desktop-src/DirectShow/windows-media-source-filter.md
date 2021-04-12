---
description: Filtro origine Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtro origine Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234479"
---
# <a name="windows-media-source-filter"></a>Filtro origine Windows Media

Questo filtro è il filtro di origine legacy per Windows Media® contenuto. Viene usato da Windows Media Player 6,4. In generale, il modo più semplice e affidabile per utilizzare questo filtro consiste nell'utilizzare il controllo ActiveX Windows Media Player 6,4. Molti dei metodi esposti da questo filtro vengono esposti anche tramite il controllo ActiveX. Per ulteriori informazioni, vedere Windows Media Player SDK.

Quando a questo filtro viene assegnato il nome di un file ASF locale o un URL per un file remoto, il file viene letto, analizzato i flussi compressi e viene creato un pin di output per ciascuno di essi. Questo filtro non usa Windows Media Format SDK. Usa le versioni dei codec installabili di Windows Media decodificatori e non le versioni DMO. Il pin di output audio si connette sempre al filtro del gestore ACM ASF e il pin del video si connette sempre al gestore ICM ASF. (ICM in questo caso si riferisce al nome originale di Gestione compressione video). Il filtro non supporta la ricerca.

Il diagramma seguente mostra un grafico di filtro con questo filtro.

![grafico filtro origine Windows Media](images/wms-wmv-graph.png)

Per mantenere la compatibilità con le versioni precedenti di Windows Media Player 6,4, questo filtro è il filtro di origine predefinito per i file con estensione WMA, WMV e ASF. Per la riproduzione di file, le applicazioni più recenti devono usare il filtro [WM ASF Reader](wm-asf-reader-filter.md) . Tuttavia, il lettore WM ASF non supporta la riproduzione di contenuto trasmesso.

Il modo più semplice per un'applicazione di riprodurre contenuti basati su Windows Media con flusso consiste nell'usare Windows Media Player SDK. Un'altra opzione consiste nell'utilizzare Windows Media Format SDK. Il tentativo di creare un lettore personalizzato basato sul filtro origine Windows Media non è consigliato.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipi di supporti pin di output                   | Varia a seconda dei flussi all'interno del file ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfacce del PIN di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| CLSID filtro                             | Vedere la sezione Osservazioni                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| File eseguibile                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | VALORE \_ normale                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Il CLSID del filtro non è definito in qnetwork. h. Usare questa macro nel proprio file di intestazione:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro di lettura ASF WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



