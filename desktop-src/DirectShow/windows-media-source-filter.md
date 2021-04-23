---
description: Filtro origine Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtro origine Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8e2c2f2e575a70d85fdce3d9b8d643e270f721
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908999"
---
# <a name="windows-media-source-filter"></a>Filtro origine Windows Media

Questo filtro è il filtro di origine legacy per il contenuto ® Windows Media. Viene usato da Windows Media Player 6.4. In generale, il modo più semplice e affidabile per usare questo filtro è usare il controllo ActiveX Windows Media Player 6.4. Molti dei metodi esposti da questo filtro vengono esposti anche tramite il controllo ActiveX. Per altre informazioni, Windows Media Player SDK.

Quando a questo filtro viene assegnato il nome di un file ASF locale o di un URL per un file remoto, legge il file, analizza i flussi compressi e crea un pin di output per ognuno di essi. Questo filtro non usa Windows Media Format SDK. Usa le versioni di codec installabili dei decodificatori Windows Media, non le versioni DMO. Il pin di output audio si connette sempre al filtro del gestore ACM di ASF e il pin video si connette sempre al gestore ICM di ASF. In questo caso, ICM fa riferimento al nome originale di Gestione compressione video. Il filtro non supporta la ricerca.

Il diagramma seguente mostra un grafico dei filtri con questo filtro.

![Grafico del filtro dell'origine multimediale windows](images/wms-wmv-graph.png)

Per mantenere la compatibilità con le versioni precedenti Windows Media Player 6.4, questo filtro è il filtro di origine predefinito per i file con estensioni di file wma, wmv e asf. Per la riproduzione di file, le applicazioni più nuove devono usare il [filtro lettore ASF WM.](wm-asf-reader-filter.md) Tuttavia, il lettore ASF WM non supporta la riproduzione di contenuto trasmesso in streaming.

Il modo più semplice per riprodurre contenuto basato su Windows Media trasmesso da un'applicazione è usare Windows Media Player SDK. Un'altra opzione è l'uso di Windows Media Format SDK. Non è consigliabile provare a creare un lettore personalizzato basato sul filtro origine Windows Media.



| Label | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMChannelInfo,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IAMNetShowConfig,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig) [**IAMNetShowExProps,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops) [**IAMNetShowPreroll,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll) [**IAMNetworkStatus,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipi di supporti pin di output                   | Varia a seconda dei flussi all'interno del file ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtro CLSID                             | Vedere la sezione Osservazioni                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| File eseguibile                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Il CLSID del filtro non è definito in qnetwork.h. Usare questa macro nel proprio file di intestazione:


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

[Filtro lettore ASF WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



