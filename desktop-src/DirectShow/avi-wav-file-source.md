---
description: Origine file AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origine file AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689361"
---
# <a name="aviwav-file-source"></a>Origine file AVI/WAV

Operazione deprecata: Per i file AVI e WAV, usare [l'origine file (Async)](file-source--async--filter.md) e il parser [AVI Splitter](avi-splitter-filter.md) [o WAVE.](wave-parser-filter.md)

Il filtro origine file AVI/WAV legge i file di origine AVI e WAV e genera i pin di output appropriati per il tipo di file.

Per i file WAV, il filtro crea un pin di output audio, che produce un flusso audio che può essere connesso a un filtro di rendering audio o a un filtro di trasformazione audio.

Per i file AVI, il filtro crea un pin di output video, che produce un flusso AVI compresso adatto per il filtro codec AVI, e un pin di output audio, che produce un flusso audio adatto per un filtro di rendering audio o un filtro di trasformazione audio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



