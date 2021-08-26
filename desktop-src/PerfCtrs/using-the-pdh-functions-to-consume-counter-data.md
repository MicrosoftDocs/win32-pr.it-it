---
description: Usare le funzioni PDH per raccogliere dati sulle prestazioni.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Uso delle funzioni PDH per l'utilizzo dei dati dei contatori
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 6c506e3c7a73a94a6bc3c282920e17504e28dedb42e0e3bee8a6f05a1e77ebbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033191"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Uso delle funzioni PDH per l'utilizzo dei dati dei contatori

Usare le funzioni PDH per raccogliere dati sulle prestazioni. Le funzioni PDH sono più [](using-the-registry-functions-to-consume-counter-data.md) facili da usare rispetto alle funzioni del Registro di sistema e possono essere usate per accedere ai dati dei contatori sia nei provider V1 che V2. PDH include API per la raccolta dei dati sulle prestazioni correnti, il salvataggio dei dati sulle prestazioni nei file di log e la lettura dei dati dai file di log.

> [!Note]
> Non è possibile usare le funzioni del livello di astrazione dell'helper dati delle prestazioni se si scrivono Windows OneCore app. Usare invece le [funzioni consumer PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

PDH è un'API di alto livello che semplifica la raccolta dei dati dei contatori delle prestazioni. Semplifica l'analisi delle query, la memorizzazione nella cache dei metadati, la corrispondenza delle istanze tra gli esempi, il calcolo di valori formattati da valori non elaborati, la lettura dei dati dai file di log e il salvataggio dei dati nei file di log. PDH usa automaticamente [le](using-the-registry-functions-to-consume-counter-data.md) funzioni del Registro di sistema durante la raccolta di dati dai provider **V1** e usa le funzioni [consumer V2](using-the-perflib-functions-to-consume-counter-data.md) durante la raccolta di dati dai **provider V2.**

Per raccogliere dati sulle prestazioni usando le funzioni PDH, seguire questa procedura.

1. [Creare una query](creating-a-query.md)
2. [Aggiungere contatori alla query](creating-a-query.md)
3. [Raccogliere i dati sulle prestazioni](collecting-performance-data.md)
4. [Visualizzare i dati sulle prestazioni](displaying-performance-data.md)
5. [Chiudere la query](creating-a-query.md)

È possibile raccogliere dati sulle prestazioni da origini in tempo reale o file di log. Per altre informazioni su come scrivere dati sulle prestazioni nei file di log, vedere [Utilizzo dei file di log](working-with-log-files.md).

## <a name="see-also"></a>Vedi anche

- [Raccolta dei dati sulle prestazioni](collecting-performance-data.md)
- [Esplorazione dei contatori](browsing-counters.md)
- [Controllo dei valori restituiti dell'interfaccia PDH](checking-pdh-interface-return-values.md)
- [esempi](examples.md)
