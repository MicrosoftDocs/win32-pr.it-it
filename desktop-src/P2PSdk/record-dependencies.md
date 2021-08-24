---
description: L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Registrare le dipendenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8121c22525a3a2d8065014eaf27143a324b2f6410f194d3257ec3b840958d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675021"
---
# <a name="record-dependencies"></a>Registrare le dipendenze

L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record. Se l'applicazione ha dipendenze tra record, ovvero l'elaborazione o la convalida di un record si basa su un altro record, l'applicazione deve essere in grado di gestire situazioni in cui i record potrebbero essere ricevuti in un ordine arbitrario e imprevedibile. Ad esempio, un'applicazione di chat può avere due tipi di record: un record che contiene informazioni su un utente specifico e un record che contiene un messaggio di chat che fa riferimento al record utente.

Un'applicazione deve essere in grado di gestire la situazione quando viene ricevuto un record del messaggio di chat prima del record utente per il messaggio di chat. Un modo per gestire la situazione è attendere il record utente usando un elenco autonomo **o** una cache e un timer. L'applicazione può esaminare periodicamente ogni record nell'elenco o nella cache e quindi gestire la situazione quando viene ricevuto il record utente richiesto.

Per gestire le dipendenze dei record, un'applicazione ben progettata è costituita dai seguenti elementi:

-   Verifica sempre le dipendenze dei record prima di eseguire un'azione.
-   Prevede le condizioni che potrebbero verificarsi quando i record vengono ricevuti in un ordine imprevisto e quindi gestisce la situazione.

 

 



