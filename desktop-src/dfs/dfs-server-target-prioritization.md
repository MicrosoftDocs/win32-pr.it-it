---
title: Assegnazione di priorità di destinazione server DFS
description: La definizione delle priorità di destinazione server DFS è una funzionalità disponibile in Microsoft Windows Server 2003 con Service Pack 1 (SP1) e sistemi operativi successivi.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225772"
---
# <a name="dfs-server-target-prioritization"></a>Assegnazione di priorità di destinazione server DFS

La definizione delle priorità di destinazione server DFS è una funzionalità disponibile in Microsoft Windows Server 2003 con Service Pack 1 (SP1) e sistemi operativi successivi. Questa funzionalità consente ai server DFS di sfruttare i vantaggi offerti da Active Directory informazioni sui costi del sito per assegnare la priorità alle destinazioni nei riferimenti client.

Prima di Windows Server 2003 con SP1, le destinazioni venivano raggruppate in due set: un gruppo per contenere tutte le destinazioni nello stesso sito del client. e un altro gruppo per tutte le altre destinazioni. Le destinazioni che condividono lo stesso sito del client sono denominate "in-site" e se il costo del sito è abilitato, viene assegnato un valore di costo specifico rispetto al sito globale, con costi di sito inferiori preferiti rispetto a quelli più alti.

Con la disponibilità di questi dati di costo del sito, le destinazioni server possono essere classificate in ordine di priorità per strategie di failover del server DFS più efficaci. In passato, questo livello di dettaglio granulare non era disponibile e gli amministratori dovevano ricorrere a mezzi artificiali (come i siti fittizi in AD) per supportare requisiti ancora semplici, come la designazione di server specifici come server "backup" o "secondario" nel caso in cui un server DFS "primario" abbia esito negativo. Ora, con i dettagli aggiuntivi forniti dal costo del sito, sono possibili strategie di failover a più livelli.

Nella discussione seguente si presuppone che i costi del sito siano abilitati.

## <a name="target-prioritization"></a>Priorità di destinazione

La priorità di destinazione è un ordinamento specifico da una prospettiva amministrativa, classificazione e classificazione dei server nel sito in termini di preferenza esplicita in base al costo del sito da parte di un client DFS. La priorità globale è indipendente dal costo del sito. Si noti che le classi di priorità globali non indicano necessariamente gli obiettivi più ottimali dal punto di vista di un client DFS, ma riflettono invece l'importanza o la mancanza di importanza di destinazioni specifiche dal punto di vista dell'amministratore del sito.

La priorità di destinazione server è divisa in due categorie di valori: classe di priorità e rango di priorità. Le classi di priorità sono divise in due livelli: locale e globale. All'interno di queste classi si verifica un ordinamento approssimativo delle destinazioni in base ai costi del sito, raggruppati come alta, normale e bassa priorità. Il risultato è cinque classi di priorità, in ordine dalla priorità più alta a quella più bassa, come indicato di seguito:

- Priorità alta globale
- Priorità elevata ai costi del sito
- Priorità normale dei costi del sito
- Costo-priorità bassa del sito
- Priorità bassa globale

Le classi costo sito possono essere considerate come suddivisioni di "priorità normale globale". Priority Rank è una semplice classificazione di interi basata sui valori ordinali: 0, 1, 2 e successive, con 0 come valore più alto e tutti i valori successivi che indicano un rango decrescente.

Le priorità globali alta e bassa non considerano i valori di costo del sito. Le destinazioni con una preferenza di ricezione a priorità alta globale su tutte le altre destinazioni e le destinazioni con priorità bassa globale ricevono la preferenza minima.

Per ordinare un riferimento, il processo completo prevede i passaggi seguenti:

1. Vengono identificati i set di destinazioni globali alta e bassa, insieme alle altre destinazioni "globali normali".
2. Se l'opzione "insite" è impostata, tutte le destinazioni esterne al sito del client vengono rimosse. L'opzione "insite" non viene applicata ai set globali massimi e con priorità bassa.
3. All'interno di ognuno di questi tre set, le destinazioni vengono ordinate usando il meccanismo di costo del sito Active Directory, usando il costo locale o completo del sito. Il risultato è costituito da set di destinazioni di uguale costo del sito.
4. All'interno dei set di destinazioni "normali globali" di uguale costo del sito, alle destinazioni viene assegnata una classe di priorità dalle classificazioni con priorità alta, normale e a basso costo del sito.
5. All'interno dei set di destinazioni di EQUAL site cost e Priority Class, le destinazioni sono ora ordinate in base alla priorità, con 0 come rango più alto.
6. All'interno dei set di destinazioni di EQUAL site cost, Priority Class e Priority Rank, le destinazioni vengono mescolate in modo casuale per il bilanciamento del carico.

Graficamente, un set di destinazioni viene ordinato come illustrato di seguito:

- destinazioni della classe con priorità alta globale 
- destinazioni della classe con priorità alta dei costi del sito con costo del sito = 0
- normale con costo del sito = 0
- basso con costo del sito = 0
- destinazioni della classe con priorità alta dei costi del sito con costo del sito = 1
- normale con costo del sito = 1
- basso con costo del sito = 1
- E così via
- destinazioni di classi con priorità bassa globali

All'interno di ognuno di questi set, le destinazioni vengono ordinate in base alla priorità. Il rango più alto è zero, con ogni valore integer successivo (1, 2 e così via) che indica un rango sempre più basso.

La priorità di destinazione è impostata su una destinazione specifica di un collegamento (o radice) in uno spazio dei nomi DFS. La priorità di una destinazione per un collegamento non influisce sull'ordinamento di altri collegamenti se lo stesso percorso di destinazione viene usato più volte. Se, ad esempio, due collegamenti hanno \\ \\ \\ Share1 server come destinazione, la priorità del \\ \\ server \\ Share1 viene impostata separatamente per entrambi i collegamenti.

La priorità predefinita per tutti i collegamenti è la priorità normale del costo del sito con un rango pari a 0. La priorità di destinazione non influisce sull'ordinamento dei riferimenti, a meno che non venga utilizzato e tutti i collegamenti esistenti vengano ordinati al momento della ricezione.

La risposta di riferimento da un server DFS è costituita da set di destinazione ordinati come indicato in precedenza, con ogni set di destinazioni non globali contenente le destinazioni dello stesso costo del sito, classe di priorità e rango di priorità. Le destinazioni all'interno di ogni set vengono ordinate in modo casuale. I client DFS che ricevono il riferimento iniziano con la prima destinazione del primo set e continuano l'elenco fino a quando non viene trovata una destinazione disponibile per un determinato collegamento o radice DFS.

Per l'implementazione dell'API specifica di questa funzionalità, vedere gli argomenti di riferimento seguenti:

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)
