---
description: Convertitore da tee a sink a sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertitore da tee a sink a sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316295"
---
# <a name="teesink-to-sink-converter"></a>Convertitore da tee a sink a sink

Il convertitore Tee/Sink-to-sink è un filtro basato su KsProxy in modalità kernel. Viene usato nei grafici di filtri per la televisione video analogici in cui viene eseguito il rendering o l'acquisizione di dati VBI. Il filtro è connesso upstream al filtro di [acquisizione video WDM](wdm-video-capture-filter.md) e fornisce un modo efficiente per duplicare i flussi di dati in modalità kernel senza le transizioni dispendiose tra il kernel e la modalità utente. Recapita ogni blocco di dati ricevuti a tutti i pin di output e il codec downstream è responsabile dell'individuazione dei dati VBI specifici da decodificare.

Il convertitore Tee/Sink-to-sink viene visualizzato nella categoria del filtro "dispositivi con splitter o di streaming WDM" (AM \_ KSCATEGORY \_ splitter).

Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md). Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 
