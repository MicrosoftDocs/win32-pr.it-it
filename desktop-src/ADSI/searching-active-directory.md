---
title: Ricerca in Active Directory
description: Una funzione importante di Active Directory è risolvere le query sui dati per gli utenti, nonché i dati di configurazione per computer e servizi.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Ricerca di ACTIVE Directory ADSI
- ADSI ADSI , ricerca in Active Directory
- query ADSI, ricerca in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d3ec83268556ebcacd89efeca425db87e2c0cc06e69a1e6eea810bcd6a21de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005471"
---
# <a name="searching-active-directory"></a>Ricerca in Active Directory

Una funzione importante di Active Directory è risolvere le query sui dati per gli utenti, nonché i dati di configurazione per computer e servizi. Per scrivere query efficienti per Active Directory, è utile avere familiarità con quanto segue:

-   Determinazione dell'ambito della query: il client deve trovare le proprietà per gli oggetti che possono trovarsi in qualsiasi posizione all'interno di una foresta o solo all'interno di un dominio o all'interno di una determinata unità organizzativa?
-   Determinazione della profondità della query: la query deve cercare solo un livello o potrebbe attraversare altre directory LDAP?
-   Prestazioni e gestione di set di risultati di grandi dimensioni: in che modo il client deve gestire in modo efficace le potenzialità di un set di risultati di grandi dimensioni?
-   Determinazione delle query migliori: quale tipo di query offre i risultati più efficienti? Quale tipo di query deve evitare lo sviluppatore?
-   Informazioni sulla sintassi della query: ADSI supporta sia la sintassi LDAP, come documentato in RFC 2254, sia un subset di SQL.
-   Scelta delle interfacce: ADSI fornisce sia OLE DB supporto sia un'interfaccia C/C++ denominata [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Poiché ADSI funziona per più spazi dei nomi, è possibile usare queste interfacce per eseguire query su altri spazi dei nomi, ad esempio Exchange, oltre ad Active Directory. Poiché ActiveX Data Object (ADO) è un semplice modello a oggetti di accesso ai dati con script su OLE DB, le interfacce OLE DB funzionano bene per i programmatori di Visual Basic e gli script writer di pagine Web. Le nuove funzionalità di accesso ai dati nelle applicazioni Visual Studio e Office che sfruttano ADO e OLE DB possono ora accedere ai dati di Active Directory nello stesso modo in cui accedono ai dati da altri provider OLE DB, ad esempio SQL Server. Tuttavia, se uno sviluppatore C/C++ deve eseguire una semplice ricerca di directory, **l'interfaccia IDirectorySearch** potrebbe essere più appropriata rispetto alle OLE DB seguenti.

Negli argomenti seguenti viene descritto come eseguire ricerche in Active Directory per assicurarsi che l'applicazione eserciti la query più efficiente, in base ai requisiti del client:

-   [Ambito della query](scope-of-query.md)
-   [Prestazioni e gestione di set di risultati di grandi dimensioni](performance-and-handling-large-result-sets.md)
-   [Sintassi del filtro di ricerca](search-filter-syntax.md)
-   [Interfacce di query](query-interfaces.md)
-   [Ricerca di dati binari](searching-binary-data.md)
-   [Query distribuite](distributed-query.md)

 

 




