---
title: Ricerche asincrone
description: L'abilitazione della ricerca asincrona (asincrona) comporta una chiamata a GetFirstRow o la prima chiamata a GetNextRow si blocca fino a quando non viene restituita la prima voce dal server.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Ricerche asincrone ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082785"
---
# <a name="asynchronous-searches"></a>Ricerche asincrone

L'abilitazione della ricerca asincrona (asincrona) comporta una chiamata a **GetFirstRow** o la prima chiamata a **GetNextRow** si blocca fino a quando non viene restituita la prima voce dal server. In altre parole, se la ricerca nel server richiede molto tempo, i primi risultati vengono restituiti rapidamente. Ciò può essere utile quando si popola una casella di riepilogo con i risultati della ricerca. I risultati della ricerca vengono visualizzati non appena vengono restituiti.

Se la funzionalità asincrona è disabilitata, la prima chiamata a **GetFirstRow** o **GetNextRow** si blocchi fino a quando il server non calcola l'intero set di risultati e restituisce un risultato. Solo in questo caso viene restituita la prima riga. Questa operazione non è consigliata se si prevede che il set di risultati sia di grandi dimensioni.

Se sono abilitati sia il paging che async, la prima chiamata a **GetFirstRow** o **GetNextRow** si blocchi fino a quando il server non genera e invia la prima pagina di risultati. Se è stata impostata una dimensione di pagina ragionevole, i risultati verranno visualizzati immediatamente. Ancora più importante, se si prevede che i risultati della ricerca siano molto grandi e si cerca una voce specifica, non è necessario richiedere altri risultati al server dopo aver trovato le voci di interesse.

Una ricerca asincrona di pagine fornisce un controllo completo di una ricerca. Ciò è utile se i risultati della ricerca possono essere molto grandi e richiedono molto tempo dal server.

Per altre informazioni sull'uso delle ricerche asincrone con un'interfaccia di ricerca specifica, vedere:

-   [Ricerche sincrone e asincrone con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




