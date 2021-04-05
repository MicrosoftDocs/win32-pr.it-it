---
description: Usare le funzioni PDH per raccogliere i dati sulle prestazioni.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Utilizzo delle funzioni PDH per utilizzare i dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881733"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Utilizzo delle funzioni PDH per utilizzare i dati del contatore

Usare le funzioni PDH per raccogliere i dati sulle prestazioni. Le funzioni PDH sono più facili da utilizzare rispetto alle [funzioni del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) e possono essere utilizzate per accedere ai dati dei contatori sia per i provider v1 che per quelli V2. PDH dispone di API per la raccolta dei dati sulle prestazioni correnti, il salvataggio dei dati sulle prestazioni nei file di log e la lettura dei dati dai file di log.

> [!Note]
> Non è possibile usare le funzioni del livello di astrazione dei dati sulle prestazioni se si scrivono app OneCore di Windows. Usare invece le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

PDH è un'API di alto livello che semplifica la raccolta dei dati dei contatori delle prestazioni. Consente l'analisi delle query, la memorizzazione dei metadati nella cache, la corrispondenza delle istanze tra gli esempi, l'elaborazione di valori formattati da valori non elaborati, la lettura dei dati dai file di log e il salvataggio dei dati nei file di log. PDH usa automaticamente le [funzioni del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) durante la raccolta dei dati dai **provider v1** e usa le [funzioni consumer v2](using-the-perflib-functions-to-consume-counter-data.md) durante la raccolta dei dati dai **provider v2**.

Per raccogliere dati sulle prestazioni usando le funzioni PDH, seguire questa procedura.

1. [Creare una query](creating-a-query.md)
2. [Aggiungere contatori alla query](creating-a-query.md)
3. [Raccogliere i dati sulle prestazioni](collecting-performance-data.md)
4. [Visualizzare i dati sulle prestazioni](displaying-performance-data.md)
5. [Chiudere la query](creating-a-query.md)

È possibile raccogliere dati sulle prestazioni da origini in tempo reale o da file di log. Per ulteriori informazioni su come scrivere i dati sulle prestazioni nei file di log, vedere [utilizzo dei file di log](working-with-log-files.md).

## <a name="see-also"></a>Vedi anche

- [Raccolta dei dati sulle prestazioni](collecting-performance-data.md)
- [Esplorazione dei contatori](browsing-counters.md)
- [Verifica dei valori restituiti dell'interfaccia PDH](checking-pdh-interface-return-values.md)
- [esempi](examples.md)
