---
description: Filtro codec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro codec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083451"
---
# <a name="wst-codec-filter"></a>Filtro codec WST

> [!IMPORTANT]
> Questo componente è stato rimosso da Windows Vista e sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

A partire Windows Vista, questo filtro viene sostituito dal filtro VBICodec, documentato nella documentazione di Microsoft TV Technologies.

WST (World Standard Teletext) è lo standard europao per la trasmissione dei dati tramite VBI su segnali tv analogici PAL. Questo standard viene fornito sia per la didascalia che per i servizi dati. Il codec WST è un filtro in modalità kernel che riceve campioni VBI non elaborati e, facoltativamente, campioni teletesto decodificati dal filtro di acquisizione tramite il filtro [Tee/Sink-to-Sink Converter.](tee-sink-to-sink-converter.md) Questo codec decodifica e/o duplica i dati Teletext decodificati e con correzione dell'errore in avanti per il filtro [WST Decoder.](wst-decoder-filter.md) Il codec WST corrisponde al filtro cc decoder per le trasmissioni NTSC. Il decodificatore WST corrisponde al decodificatore [di riga 21](line-21-decoder-filter.md) per NTSC; Questi filtri creano le bitmap che vengono inviate al Mixer o al renderer di combinazione video.

Questo filtro ha due pin di input, VBI e HWCC. Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione. Quando i dati vengono ricevuti sul pin HWCC, il codec WST opera in modalità "pass-through" e invia i dati direttamente al decodificatore WST senza elaborarlo in alcun modo. Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente nel codec WST.

Il filtro codec WST viene visualizzato nella categoria di filtro "Codec VBI di streaming WDM" (**AM \_ KSCATEGORY \_ VBICODEC).**

Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente usando **CoCreateInstance.** Usare invece [Enumeratore dispositivo di sistema](system-device-enumerator.md). Per altre informazioni, vedere [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Visualizzazione del teletesto standard mondiale](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



