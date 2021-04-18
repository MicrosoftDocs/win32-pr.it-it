---
description: Origine file AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origine file AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304264"
---
# <a name="aviwav-file-source"></a>Origine file AVI/WAV

Operazione deprecata: Per i file AVI e WAV, usare il [file di origine (Async)](file-source--async--filter.md) e la [barra di divisione AVI](avi-splitter-filter.md) o il [parser Wave](wave-parser-filter.md).

Il filtro di origine file AVI/WAV legge i file di origine AVI e WAV e genera i pin di output appropriati per il tipo di file.

Per i file WAV, il filtro crea un pin di output audio che produce un flusso audio che può essere connesso a un filtro di rendering audio o a un filtro di trasformazione audio corrispondente.

Per i file AVI, il filtro crea un pin di output video, che produce un flusso AVI compresso adatto per il filtro codec AVI e un pin di output audio, che produce un flusso audio adatto per un filtro per il rendering audio o un filtro di trasformazione audio corrispondente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



