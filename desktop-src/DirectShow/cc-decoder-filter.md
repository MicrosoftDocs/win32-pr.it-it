---
description: Filtro decodificatore CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro decodificatore CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965540"
---
# <a name="cc-decoder-filter"></a>Filtro decodificatore CC

> [!IMPORTANT]
> Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

Il decodificatore CC VBI è un filtro della classe del flusso in modalità kernel. Viene visualizzato in GraphEdit sotto la categoria "WDM Streaming VBI codecs". Accetta le forme d'onda di esempio fornite da un filtro di acquisizione e recapita i dati decodificati per la didascalia al [decodificatore della riga 21](line-21-decoder-filter.md) e/o alle applicazioni interessate.

Questo filtro ha due pin di input, VBI e HWCC. Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione. Quando i dati vengono ricevuti sul pin HWCC, il decodificatore CC funziona in modalità "pass-through" e invia i dati direttamente al decodificatore della riga 21 senza elaborarli in alcun modo. Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente sul decoder CC. La categoria pin è **PINNAME \_ video \_ CC \_ Capture**.

Il decodificatore CC dispone di un massimo di otto pin di output, ognuno dei quali può selezionare le proprie righe e sottoflussi. Il primo pin di output è connesso al decodificatore line-21.

Il filtro del decodificatore CC viene visualizzato nella categoria di filtro "WDM Streaming VBI codecs" (**am \_ KSCATEGORY \_ VBICODEC**).

Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite **CoCreateInstance**. Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md). Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Visualizzazione di didascalie chiuse](viewing-closed-captions.md)
</dt> </dl>

 

 



