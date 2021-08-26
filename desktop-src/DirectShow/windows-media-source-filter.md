---
description: Windows Filtro origine supporti
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Filtro origine supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1e617a51095aec7cb409e46ba8f19f14f76fcd6f8d8a9bffeaa13843b1728b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982207"
---
# <a name="windows-media-source-filter"></a>Windows Filtro origine supporti

Questo filtro è il filtro di origine legacy per Windows contenuti ® multimediali. Viene usato da Windows Media Player 6.4. In generale, il modo più semplice e affidabile per usare questo filtro è usare il Windows Media Player 6.4 ActiveX controllo. Molti dei metodi esposti da questo filtro vengono esposti anche tramite il ActiveX controllo . Per altre informazioni, Windows Media Player SDK.

Quando a questo filtro viene assegnato il nome di un file ASF locale o di un URL per un file remoto, legge il file, analizza i flussi compressi e crea un pin di output per ognuno di essi. Questo filtro non usa l'SDK Windows Media Format. Usa le versioni di codec installabili dei Windows media, non le versioni DMO. Il pin di output audio si connette sempre al filtro del gestore ACM di ASF e il pin video si connette sempre al gestore di ICM ASF. (ICM in questo caso si riferisce al nome originale di Gestione compressione video. Il filtro non supporta la ricerca.

Il diagramma seguente mostra un grafico dei filtri con questo filtro.

![Grafico del filtro dell'origine multimediale windows](images/wms-wmv-graph.png)

Per mantenere la compatibilità con le versioni precedenti Windows Media Player 6.4, questo filtro è il filtro di origine predefinito per i file con estensioni di file wma, wmv e asf. Per la riproduzione di file, le applicazioni più nuove devono usare il [filtro lettore ASF WM.](wm-asf-reader-filter.md) Tuttavia, il lettore ASF WM non supporta la riproduzione di contenuto trasmesso in streaming.

Il modo più semplice per riprodurre contenuti basati su Windows streaming in un'applicazione è usare Windows Media Player SDK. Un'altra opzione è usare Windows Media Format SDK. Non è consigliabile provare a creare un lettore personalizzato basato Windows filtro origine multimediale.



| Etichetta | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMChannelInfo,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IAMNetShowConfig,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig) [**IAMNetShowExProps,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops) [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipi di supporti pin di output                   | Varia a seconda dei flussi all'interno del file ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| CLSID del filtro                             | Vedere la sezione Osservazioni                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| File eseguibile                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | MERIT \_ NORMAL                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Il CLSID del filtro non è definito in qnetwork.h. Usare questa macro nel file di intestazione:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro lettore ASF WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



