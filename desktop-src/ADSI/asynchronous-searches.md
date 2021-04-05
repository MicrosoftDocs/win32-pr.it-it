---
title: Ricerche asincrone
description: L'abilitazione dei risultati della ricerca asincrona (Async) in una chiamata a GetFirstRow o alla prima chiamata a GetNextRow blocca fino a quando non viene restituita la prima voce dal server.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI per ricerche asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955114"
---
# <a name="asynchronous-searches"></a>Ricerche asincrone

L'abilitazione dei risultati della ricerca asincrona (Async) in una chiamata a **GetFirstRow** o alla prima chiamata a **GetNextRow** blocca fino a quando non viene restituita la prima voce dal server. Ovvero, se la ricerca sul server richiede molto tempo, i primi risultati vengono restituiti rapidamente. Questo può essere utile quando si popola una casella di riepilogo con i risultati della ricerca. I risultati della ricerca vengono visualizzati quando vengono restituiti.

Se Async è disabilitato, la prima chiamata a **GetFirstRow** o **GetNextRow** si bloccherà fino a quando il server non calcola l'intero set di risultati e restituisce. Solo a questo punto viene restituita la prima riga. Questa operazione non è consigliata se si prevede che il set di risultati sia di grandi dimensioni.

Se il paging e async sono abilitati, la prima chiamata a **GetFirstRow** o **GetNextRow** si bloccherà fino a quando il server non genera e non invia la prima pagina di risultati. Se è stata impostata una dimensione di pagina ragionevole, i risultati vengono visualizzati immediatamente. Ancora più importante, se i risultati della ricerca sono molto grandi e si cerca una voce specifica, non è necessario richiedere altri risultati dal server dopo aver trovato le voci che interessano.

Una ricerca asincrona di paging fornisce un controllo accurato di una ricerca. Questa operazione è utile se i risultati della ricerca possono avere dimensioni molto elevate e richiedono tempi estesi dal server.

Per ulteriori informazioni sull'utilizzo di ricerche asincrone con un'interfaccia di ricerca specifica, vedere:

-   [Ricerche sincrone e asincrone con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




