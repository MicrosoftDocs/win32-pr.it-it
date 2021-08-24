---
description: Filtro decodificatore CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro decodificatore CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5feab764883754407030f2b4f72f794d049f5a394efb107ac149b10125da8d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757401"
---
# <a name="cc-decoder-filter"></a>Filtro decodificatore CC

> [!IMPORTANT]
> Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

Cc VBI Decoder è un filtro di classe di flusso in modalità kernel. Viene visualizzato in GraphEdit nella categoria "Codec VBI di streaming WDM". Accetta forme d'onda di esempio recapitate da un filtro di acquisizione e recapita i dati codificati codificati al decodificatore [Line 21](line-21-decoder-filter.md) e/o alle applicazioni interessate.

Questo filtro ha due pin di input, VBI e HWCC. Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione. Quando i dati vengono ricevuti sul pin HWCC, il decodificatore CC opera in modalità "pass-through" e invia i dati direttamente al decodificatore Line 21 senza elaborarlo in alcun modo. Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente sul decodificatore CC. La categoria pin è **PINNAME \_ VIDEO CC \_ \_ CAPTURE.**

Il decodificatore CC dispone di un massimo di otto pin di output, ognuno dei quali può selezionare le proprie linee e sottostream. Il primo pin di output è connesso al decodificatore Line-21.

Il filtro CC Decoder viene visualizzato nella categoria di filtro "Codec VBI di streaming WDM" (**AM \_ KSCATEGORY \_ VBICODEC**).

Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente usando **CoCreateInstance**. Usare invece [l'enumeratore del dispositivo di sistema](system-device-enumerator.md). Per altre informazioni, vedere [Creazione di Kernel-Mode filtri](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Visualizzazione di sottotitoli codificati](viewing-closed-captions.md)
</dt> </dl>

 

 



