---
description: Codifica video con compressione temporale
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codifica video con compressione temporale (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310162"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codifica video con compressione temporale (Microsoft Media Foundation)

Per ottenere i rapporti di compressione più elevati possibili, i codec Windows Media Video usano la *compressione temporale*. La compressione temporale è una tecnica che consente di ridurre le dimensioni dei video compressi senza codificare ogni fotogramma come immagine completa. I frame codificati completamente (come un'immagine statica) sono denominati *fotogrammi chiave*. Tutti gli altri frame del video sono rappresentati da dati che specificano la modifica dall'ultimo frame. Questi frame sono detti *frame Delta*.

La quantità di compressione che è possibile ottenere tramite la compressione temporale dipende dal contenuto. Se il video è statico, senza molto movimento o altre modifiche nell'immagine, è possibile creare molti frame Delta per ogni fotogramma chiave. Maggiore è il numero di frame Delta utilizzati, minore è il flusso video codificato. Tuttavia, se il video è dinamico, con una grande quantità di movimento o colori mutevoli, il vantaggio di usare la compressione temporale è inferiore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



