---
description: L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Registrare le dipendenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312225"
---
# <a name="record-dependencies"></a>Registrare le dipendenze

L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record. Se l'applicazione ha dipendenze dei record, il che significa che l'elaborazione o la convalida di un record si basa su un altro record, l'applicazione deve essere in grado di gestire le situazioni in cui è possibile che i record vengano ricevuti in ordine arbitrario e imprevedibile. Ad esempio, un'applicazione di chat può avere due tipi di record: un record che contiene informazioni su un utente specifico e un record contenente un messaggio di chat che fa riferimento al record utente.

Un'applicazione deve essere in grado di gestire la situazione di ricezione di un record di messaggio di chat prima del record utente per il messaggio di chat. Un modo per gestire la situazione consiste nell'attendere il record utente usando un **elenco autonomo** o una cache e un timer. L'applicazione può esaminare periodicamente ogni record nell'elenco o nella cache e quindi gestire la situazione quando viene ricevuto il record utente richiesto.

Per gestire le dipendenze dei record, un'applicazione ben progettata è costituita dagli elementi seguenti:

-   Verifica sempre le dipendenze dei record prima di eseguire un'azione.
-   Anticipa le condizioni che possono verificarsi quando i record vengono ricevuti in un ordine imprevisto e quindi gestisce la situazione.

 

 



