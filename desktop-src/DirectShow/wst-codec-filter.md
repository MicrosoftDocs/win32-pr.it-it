---
description: Filtro codec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro codec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349796"
---
# <a name="wst-codec-filter"></a>Filtro codec WST

> [!IMPORTANT]
> Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

A partire da Windows Vista, questo filtro viene sostituito dal filtro VBICodec, documentato nella documentazione relativa alle tecnologie Microsoft TV.

Il televideo (WST) è lo standard europeo per la trasmissione dei dati tramite VBI nei segnali TV analoghi di PAL. La didascalia e i servizi dati vengono forniti utilizzando questo standard. Il codec WST è un filtro in modalità kernel che riceve esempi di VBI non elaborati e, facoltativamente, gli esempi di televideo decodificati dal filtro di acquisizione tramite il filtro del [convertitore Tee/Sink-to-sink](tee-sink-to-sink-converter.md) . Questo codec decodifica e/o duplica i dati di televideo decodificati e con errori in diretta per il filtro del [decodificatore WST](wst-decoder-filter.md) . Il codec WST corrisponde al filtro del decodificatore CC per le trasmissioni NTSC. Il decodificatore WST corrisponde al [decodificatore della riga 21](line-21-decoder-filter.md) per NTSC; Questi filtri creano le bitmap inviate al mixer overlay o al renderer di mixaggio video.

Questo filtro ha due pin di input, VBI e HWCC. Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione. Quando i dati vengono ricevuti sul pin HWCC, il codec WST funziona in modalità "pass-through" e invia i dati direttamente al decodificatore WST senza elaborarli in alcun modo. Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente nel codec WST.

Il filtro codec WST viene visualizzato nella categoria di filtro "WDM Streaming VBI codecs" (**am \_ KSCATEGORY \_ VBICODEC**).

Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite **CoCreateInstance**. Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md). Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Visualizzazione del televideo standard internazionale](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



