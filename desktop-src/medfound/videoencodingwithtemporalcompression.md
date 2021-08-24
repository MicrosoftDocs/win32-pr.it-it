---
description: Codifica video con compressione temporale
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codifica video con compressione temporale (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d663b0101353d9ce72dab45f0b85e594afcacf4aa8b8a99a6d61d2db0ae07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721351"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codifica video con compressione temporale (Microsoft Media Foundation)

Per ottenere i più alti rapporti di compressione possibili, i codec video Windows media usano la *compressione temporale*. La compressione temporale è una tecnica che consente di ridurre le dimensioni del video compresso non codificando ogni fotogramma come immagine completa. I fotogrammi codificati completamente (come un'immagine statica) sono *detti fotogrammi chiave.* Tutti gli altri fotogrammi nel video sono rappresentati da dati che specificano la modifica dall'ultimo fotogramma. Questi frame sono denominati *frame differenziali.*

La quantità di compressione che può essere ottenuta usando la compressione temporale dipende dal contenuto. Se il video è statico, senza molti movimenti o altre modifiche nell'immagine, è possibile creare molti fotogrammi differenziali per ogni fotogramma chiave. Più sono i fotogrammi delta usati, più piccolo è il flusso video codificato. Tuttavia, se il video è dinamico, con molti movimenti o colori che cambiano, il vantaggio di usare la compressione temporale è minore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



