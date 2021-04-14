---
title: Ricerca di Active Directory
description: Una funzione importante di Active Directory consiste nel risolvere le query sui dati degli utenti, nonché i dati di configurazione per i computer e i servizi.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Ricerca di Active Directory ADSI
- ADSI ADSI, ricerca in Active Directory
- query ADSI, ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328356"
---
# <a name="searching-active-directory"></a>Ricerca di Active Directory

Una funzione importante di Active Directory consiste nel risolvere le query sui dati degli utenti, nonché i dati di configurazione per i computer e i servizi. Per scrivere query efficienti per Active Directory, è utile acquisire familiarità con quanto segue:

-   Determinazione dell'ambito della query: è necessario che il client trovi proprietà per oggetti che potrebbero trovarsi in qualsiasi punto all'interno di una foresta o solo all'interno di un dominio o in una determinata unità organizzativa (OU)?
-   Determinazione della profondità della query: è necessario che la query cerchi un solo livello o possa incrociare altre directory LDAP?
-   Prestazioni e gestione di set di risultati di grandi dimensioni: in che modo il client può gestire efficacemente il potenziale di un set di risultati di grandi dimensioni?
-   Determinazione delle query migliori: quale tipo di query fornisce i risultati più efficienti? Quale tipo di query lo sviluppatore deve evitare?
-   Informazioni sulla sintassi della query: ADSI supporta sia la sintassi LDAP come documentata in RFC 2254, sia un subset di SQL.
-   Scelta delle interfacce: ADSI offre supporto OLE DB e un'interfaccia C/C++ denominata [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Poiché ADSI funziona per più spazi dei nomi, è possibile utilizzare queste interfacce per eseguire query in altri spazi dei nomi, ad esempio Exchange, nonché Active Directory. Poiché ADO (ActiveX Data Object) è un semplice modello a oggetti di accesso ai dati con script in OLE DB, le interfacce OLE DB sono ideali per Visual Basic programmatori e writer di script di pagine Web. Le nuove funzionalità di accesso ai dati in Visual Studio e nelle applicazioni di Office che sfruttano i vantaggi di ADO e OLE DB possono ora accedere ai dati di Active Directory in modo analogo all'accesso ai dati da altri provider OLE DB, ad esempio SQL Server. Tuttavia, se uno sviluppatore C/C++ deve eseguire una semplice ricerca di directory, l'interfaccia **IDirectorySearch** potrebbe essere più appropriata delle interfacce OLE DB.

Negli argomenti seguenti viene descritto come eseguire la ricerca Active Directory per assicurarsi che l'applicazione rilascia la query più efficiente, in base ai requisiti del client:

-   [Ambito della query](scope-of-query.md)
-   [Prestazioni e gestione di set di risultati di grandi dimensioni](performance-and-handling-large-result-sets.md)
-   [Sintassi del filtro di ricerca](search-filter-syntax.md)
-   [Interfacce di query](query-interfaces.md)
-   [Ricerca di dati binari](searching-binary-data.md)
-   [Query distribuite](distributed-query.md)

 

 




