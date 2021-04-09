---
description: Il gestore dell'ambito di ricerca per indicizzazione è un set di interfacce che fornisce i metodi per informare il motore di ricerca di Windows sui contenitori per eseguire la ricerca per indicizzazione e gli elementi in tali contenitori da includere o escludere nel catalogo.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Utilizzo di gestione ambito ricerca per indicizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128611"
---
# <a name="using-the-crawl-scope-manager"></a>Utilizzo di gestione ambito ricerca per indicizzazione

Il gestore dell'ambito di ricerca per indicizzazione è un set di interfacce che fornisce i metodi per informare il motore di ricerca di Windows sui contenitori per eseguire la ricerca per indicizzazione e gli elementi in tali contenitori da includere o escludere nel catalogo. Gli sviluppatori possono utilizzare CSM per definire un ambito di ricerca per indicizzazione a livello di codice per un nuovo archivio dati o gestore di protocollo. Gli amministratori possono utilizzare il CSM per visualizzare gli indici, le radici di ricerca e le regole dell'ambito di tutti gli utenti.

Questa sezione è organizzata nel modo seguente:

-   [Che cos'è gestione ambito ricerca per indicizzazione?](#what-is-the-crawl-scope-manager)
-   [Radici ricerca e regole ambito](#search-roots-and-scope-rules)
    -   [Radici di ricerca](#search-roots-and-scope-rules)
    -   [Regole ambito](#scope-rules)
-   [Criteri di gruppo supportati dal gestore dell'ambito di ricerca per indicizzazione](#group-policies-supported-by-the-crawl-scope-manager)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>Che cos'è gestione ambito ricerca per indicizzazione?

Per comprendere il gestore dell'ambito di ricerca per indicizzazione, è necessario comprendere i termini seguenti:

-   Un *ambito di ricerca per indicizzazione* è costituito da un set di URL che puntano a archivi dati o contenitori (archivi dati di posta elettronica, database, condivisioni file di rete e così via) indicizzati dall'indicizzatore per indicizzare gli elementi. Per un archivio dati gerarchico, l'ambito della ricerca per indicizzazione può includere un URL padre, ma escludere un URL figlio e viceversa. Gli elementi all'interno dell'ambito di ricerca per indicizzazione vengono indicizzati. gli elementi al di fuori dell'ambito di ricerca vengono ignorati.
-   Una *radice di ricerca* è l'URL di primo livello che identifica un contenitore o un archivio dati associato a un gestore di protocollo specifico. Le radici di ricerca possono identificare le posizioni specifiche di un utente, che si trovano in un computer remoto, o che corrispondono a un modello di carattere jolly. Quando si aggiunge un nuovo archivio dati o un gestore di protocollo, è necessario aggiungere anche una radice di ricerca all'ambito della ricerca per indicizzazione.
-   Una *regola di ambito* è una regola che include o esclude gli URL all'interno di una radice di ricerca dalla ricerca per indicizzazione e l'indicizzazione. Si supponga, ad esempio, di voler indicizzare tutti gli elementi all'interno della cartella ProjectFiles, ad eccezione dei prototipi della sottocartella. È necessaria una regola di inclusione per file:///C: \\ WorkteamA \\ ProjectFiles \\ e una regola di esclusione per file:///C: \\ WorkteamA \\ ProjectFiles \\ prototipi \\ .

Il gestore dell'ambito di ricerca per **indicizzazione** è un set di API che consente di aggiungere, rimuovere ed enumerare le radici di ricerca e le regole di ambito per l'indicizzatore di ricerca di Windows. Quando si vuole che l'indicizzatore inizi a eseguire la ricerca per indicizzazione in un nuovo contenitore, è possibile usare CSM per impostare le regole di ricerca e le radice di ricerca per i percorsi all'interno delle radice di ricerca. Ad esempio, se si installa un nuovo gestore di protocollo, è possibile creare una radice di ricerca e aggiungere una o più regole di inclusione. quindi, l'indicizzatore può avviare una ricerca per indicizzazione iniziale. Il CSM offre le interfacce seguenti che consentono di eseguire questa operazione a livello di codice.

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

Sebbene sia possibile utilizzare le API CSM per definire un ambito di ricerca per indicizzazione a livello di codice, il CSM è stato progettato per supportare anche gli utenti finali. Si supponga, ad esempio, di aver sviluppato un gestore di protocollo per un nuovo archivio dati e che si voglia consentire agli utenti o agli amministratori di gestire i percorsi da indicizzare. È possibile utilizzare il gestore dell'ambito di ricerca per indicizzazione per impostare una o più radici di ricerca (ad esempio, file:///C: \\ contenitore \\ ) e l'interfaccia utente di Windows Search per l'impostazione delle opzioni di indicizzazione visualizzerà ogni radice di ricerca con una casella di controllo. Gli utenti possono quindi includere o escludere il percorso o gli elementi figlio di tale percorso.

## <a name="search-roots-and-scope-rules"></a>Radici ricerca e regole ambito

Le radici di ricerca e le regole di ambito definiscono un working set di URL che comprendono l'ambito di ricerca per indicizzazione dell'indicizzatore.

### <a name="search-roots"></a>Radici di ricerca

L'impostazione di una radice di ricerca non specifica quali parti dell'archivio devono essere indicizzate. indica semplicemente che un archivio contenuto esiste ed è associato a un gestore di protocollo registrato. La sintassi di una radice di ricerca include un protocollo, un identificatore di sicurezza del sito o dell'utente e un percorso per la ricerca per indicizzazione.

È necessario creare nuove radici di ricerca quando:

-   Installare un gestore di protocollo o
-   Si vuole indicizzare un nuovo archivio dati

AND

-   l'archivio dati non è già presente nell'ambito di ricerca per indicizzazione dell'indicizzatore.

Per istruzioni sull'aggiunta, la rimozione e l'enumerazione delle radici di ricerca, vedere [gestione delle radici di ricerca](-search-3x-wds-extidx-csm-searchroots.md) .

### <a name="scope-rules"></a>Regole ambito

Le regole di ambito includono o escludono gli URL all'interno di una radice di ricerca da una ricerca per indicizzazione e indicizzata Le regole di ambito possono essere impostate dagli utenti finali, da criteri di gruppo o da sviluppatori di terze parti. Quando si definisce una nuova radice di ricerca, è necessario definire le regole di ambito a livello di codice. Le radici di ricerca e le regole di ambito comprendono l'ambito di ricerca per indicizzazione predefinito per l'archivio dati e il gestore del protocollo.

> [!Note]  
> Gli utenti con accesso al pannello di controllo possono modificare l'ambito di ricerca per indicizzazione predefinito. Pertanto, qualsiasi applicazione che offra la gestione degli ambiti deve sempre ottenere le regole direttamente dal CSM usando i metodi di enumerazione invece di basarsi sulla propria copia salvata delle regole dell'utente.

 

Per istruzioni sull'aggiunta, la rimozione, il ripristino e l'enumerazione delle regole dell'ambito, vedere [gestione delle regole dell'ambito](-search-3x-wds-extidx-csm-scoperules.md) .

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Criteri di gruppo supportati dal gestore dell'ambito di ricerca per indicizzazione

Gli amministratori di sistema possono definire gli ambiti di ricerca per indicizzazione nelle organizzazioni usando criteri di gruppo. Queste regole di criteri di gruppo possono fungere anche da regole predefinite, che possono essere sostituite dagli utenti. È ad esempio possibile indicizzare un set di directory per un gruppo di utenti e un set diverso per un altro gruppo di utenti, consentendo agli utenti di deselezionare queste impostazioni predefinite. Le regole di criteri di gruppo possono anche fungere da regole di esclusione forzata che non possono essere sostituite dagli utenti, ad esempio per impedire a determinati utenti di indicizzare determinate condivisioni di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle radici di ricerca](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Gestione delle regole di ambito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[Processo di indicizzazione](-search-indexing-process-overview.md)
</dt> </dl>

 

 
