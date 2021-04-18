---
title: Recupero di set di risultati di grandi dimensioni
description: Quando esiste la possibilità che il set di risultati che verrà restituito conterrà più di 1000 elementi, è necessario utilizzare una ricerca di paging.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Recupero di set di risultati di grandi dimensioni ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297656"
---
# <a name="retrieving-large-results-sets"></a>Recupero di set di risultati di grandi dimensioni

Quando esiste la possibilità che il set di risultati che verrà restituito conterrà più di 1000 elementi, è necessario utilizzare una ricerca di paging. Le ricerche di Active Directory eseguite senza paging sono limitate alla restituzione di un massimo di primi 1000 record. Con una ricerca di paging, il set di risultati viene presentato come singole pagine, ognuna delle quali contiene un numero predeterminato di voci di risultato. Con questo tipo di ricerca, vengono restituite nuove pagine delle voci dei risultati fino a quando non viene raggiunta la fine del set di risultati.

Per impostazione predefinita, il server che risponde a una richiesta di query calcola completamente un set di risultati prima di restituire i dati. In un set di risultati di grandi dimensioni, questa operazione richiede memoria server mentre viene acquisito il set di risultati e la larghezza di banda di rete quando viene restituito il risultato di grandi dimensioni. L'impostazione di una dimensione di pagina consente al server di inviare i dati nelle pagine durante la compilazione delle pagine. Il client memorizza quindi i dati nella cache e fornisce un cursore al codice a livello di applicazione. Il paging viene impostato definendo il numero di righe calcolate dal server prima che i dati vengano restituiti attraverso la rete al client.

La ricerca di paging offre vantaggi sia per il client che per il server. Ad esempio, il client può essere più reattivo nella presentazione dei risultati agli utenti finali. Questo è particolarmente importante per gli strumenti dell'interfaccia utente grafica in grado di visualizzare i dati mentre un altro thread riceve contemporaneamente più dati dal server.

Quando si configura la query, se si specifica un tipo di ordinamento per il set di risultati, è necessario che il server calcoli completamente il set di risultati prima di restituire i dati al client, il che influisca sul tempo di risposta per la query.

Sul lato server, la ricerca di paging rende l'operazione scalabile. Se, ad esempio, i client 100 inviano richieste di ricerca simultaneamente e, in media, a ogni client vengono restituiti 200 oggetti, se le dimensioni della pagina non vengono specificate, il server deve disporre di memoria sufficiente per contenere il set di risultati completo di 20.000 voci. In alternativa, se ogni client specifica una dimensione di pagina di dieci oggetti, i requisiti di memoria sul server verrebbero ridotti di un fattore di 20.

> [!Note]  
> Non tutti i servizi directory supportano le ricerche di paging. Active Directory implementa l'architettura delle dimensioni di pagina.

 

Molti server di directory specificano un limite amministrativo per il numero massimo di oggetti che possono essere restituiti se un client non specifica le dimensioni della pagina. Quando viene raggiunto il limite amministrativo, viene generato il limite di errore Win32 dell'amministratore di DS per gli **errori \_ \_ \_ \_** .

Sul lato client, una ricerca di paging consente a un client di arrestare l'operazione mentre è ancora in corso. Al contrario, in una ricerca non di paging, il client viene bloccato fino a quando i dati non vengono restituiti completamente oppure si verifica un errore. Questo potrebbe influisca sulle prestazioni di rete se il set di risultati risulta più grande e impiega più tempo del previsto.

Per conto del client, ADSI gestisce in modo trasparente le dimensioni della pagina. Il client non deve contare il numero di oggetti in corso. ADSI incapsula l'interazione del server per il client. Dal punto di vista del client, la ricerca restituisce un set di risultati completo.

Per ulteriori informazioni sull'utilizzo dell'opzione timeout ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Paging con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

Una ricerca di paging è trasparente per l'applicazione perché ADSI continua a recuperare automaticamente ulteriori pagine di risultati finché non raggiunge la fine del set di risultati o la fine del limite di tempo impostato. Quando si usa una ricerca di paging, il limite di dimensioni non esegue l'override delle dimensioni della pagina. Il limite di dimensioni può essere utilizzato solo quando si recupera un set di risultati che contiene meno di 1000 voci.

 

 




