---
title: Ottimizzazione file composto
description: L'archiviazione asincrona consente alle applicazioni di eseguire il layout preciso dei file composti, in modo che i dati siano disponibili nell'ordine in cui le applicazioni lo richiedono.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Ottimizzazione file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708200"
---
# <a name="compound-file-optimization"></a>Ottimizzazione file composto

L'archiviazione asincrona consente alle applicazioni di eseguire il layout preciso dei file composti, in modo che i dati siano disponibili nell'ordine in cui le applicazioni lo richiedono. Se un'applicazione richiede solo una parte dei dati per visualizzare una prima pagina di informazioni, questi dati possono essere posizionati all'inizio del file, anche se si trova logicamente alla fine di un flusso. I dati provenienti da flussi diversi possono essere interfogliati. I dati audio e video, ad esempio, possono essere interfogliati in modo che le operazioni di lettura successive recuperino contemporaneamente un requisito per le applicazioni multimediali.

[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) può essere utilizzato per il layout di un DocFile, migliorando così le prestazioni nella maggior parte degli scenari.

 

 




