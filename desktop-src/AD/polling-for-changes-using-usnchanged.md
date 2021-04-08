---
title: Polling delle modifiche tramite USNChanged
description: Le modifiche da Active Directory possono essere ottenute anche eseguendo una query sull'attributo uSNChanged, che evita le limitazioni del controllo DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Polling delle modifiche tramite USNChanged AD
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e062c84fae575f837f45d78be7c92e5e284c1e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872277"
---
# <a name="polling-for-changes-using-usnchanged"></a>Polling delle modifiche tramite USNChanged

Il controllo DirSync è potente ed efficiente, ma presenta due limitazioni significative:

-   Solo per le applicazioni con privilegi elevati: per usare il controllo DirSync, un'applicazione deve essere eseguita con un account che disponga del privilegio **\_ \_ \_ nome agente di sincronizzazione se** nel controller di dominio. Pochi account hanno privilegi elevati, pertanto un'applicazione che utilizza il controllo DirSync non può essere eseguita da utenti normali.
-   Nessun ambito del sottoalbero: il controllo DirSync restituisce tutte le modifiche che si verificano all'interno di un contesto dei nomi. Un'applicazione interessata solo alle modifiche che si verificano in un piccolo sottoalbero di un contesto dei nomi deve guadare molte modifiche irrilevanti, il che risulta inefficiente sia per l'applicazione sia per il controller di dominio.

Le modifiche da Active Directory possono essere ottenute anche eseguendo una query sull'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) , che evita le limitazioni del controllo DirSync. Questa alternativa non è preferibile rispetto al controllo DirSync, perché comporta la trasmissione di tutti gli attributi quando viene modificato un attributo e richiede più lavoro da parte dello sviluppatore di applicazioni per gestire correttamente determinati scenari di errore. Attualmente, il modo migliore per scrivere alcune applicazioni di rilevamento delle modifiche.

Quando un controller di dominio modifica un oggetto, imposta l'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) dell'oggetto su un valore maggiore del valore precedente dell'attributo **uSNChanged** per quell'oggetto e maggiore del valore corrente dell'attributo **uSNChanged** per tutti gli altri oggetti contenuti in tale controller di dominio. Di conseguenza, un'applicazione può trovare l'oggetto modificato più di recente in un controller di dominio individuando l'oggetto con il valore **uSNChanged** più grande. Il secondo oggetto modificato più di recente in un controller di dominio avrà il secondo valore **uSNChanged** più grande e così via.

L'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) non viene replicato, pertanto la lettura dell'attributo **uSNChanged** di un oggetto in due controller di dominio diversi fornirà in genere valori diversi.

Ad esempio, l'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) può essere usato per tenere traccia delle modifiche in un sottoalbero. Eseguire prima di tutto una "sincronizzazione completa" del sottoalbero. si supponga che il valore **uSNChanged** più grande per qualsiasi oggetto in S sia U. periodicamente eseguire una query per tutti gli oggetti nel sottoalbero s il cui valore **uSNChanged** è maggiore di U. La query restituirà tutti gli oggetti che sono stati modificati dopo la sincronizzazione completa. Impostare la **uSNChanged** più grande tra questi oggetti modificati e si è pronti per eseguire nuovamente il polling.

Le sottigliezze dell'implementazione di un'applicazione di sincronizzazione [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) includono:

-   Usare l'attributo **highestCommittedUSN** di RootDSE per associare i filtri [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) . Ovvero, prima di avviare una sincronizzazione completa, leggere il **highestCommittedUSN** del controller di dominio affiliato. Eseguire quindi una query di sincronizzazione completa (usando i risultati di paging) per inizializzare il database. Al termine dell'operazione, archiviare il valore **highestCommittedUSN** letto prima della query di sincronizzazione completa; da utilizzare come limiti inferiori dell'attributo **uSNChanged** per la sincronizzazione successiva. Successivamente, per eseguire una sincronizzazione incrementale, rileggere l'attributo RootDSE di **highestCommittedUSN** . Quindi eseguire una query per gli oggetti rilevanti, usando i risultati di paging, il cui **uSNChanged** è maggiore dei limiti inferiori del valore dell'attributo **uSNChanged** salvato dalla sincronizzazione precedente. Aggiornare il database usando queste informazioni. Al termine, aggiornare i limiti inferiori dell'attributo **uSNChanged** dal valore **highestCommittedUSN** letto prima della query di sincronizzazione incrementale. Archiviare sempre i limiti inferiori del valore dell'attributo **uSNChanged** nella stessa archiviazione che l'applicazione sta sincronizzando con il contenuto del controller di dominio.

    Attenendosi a questa procedura, anziché a quella basata sui valori [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) sugli oggetti recuperati, evita di riesaminare gli oggetti aggiornati che non rientrano nel set applicabile all'applicazione.

-   Poiché [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) è un attributo non replicato, l'applicazione deve essere associata allo stesso controller di dominio ogni volta che viene eseguita. Se non è possibile eseguire l'associazione a tale controller di dominio, è necessario attendere fino a quando non è possibile eseguire questa operazione oppure affiliare un nuovo controller di dominio ed eseguire una sincronizzazione completa con tale controller di dominio. Quando l'applicazione è affiliata a un controller di dominio, registra il nome DNS del controller di dominio in una risorsa di archiviazione stabile, ovvero lo stesso spazio di archiviazione mantenuto coerente con il contenuto del controller di dominio. USA quindi il nome DNS archiviato per eseguire il binding allo stesso controller di dominio per le sincronizzazioni successive.
-   L'applicazione deve rilevare quando il controller di dominio a cui è attualmente affiliata è stato ripristinato dal backup, perché ciò può causare incoerenze. Quando l'applicazione è affiliata a un controller di dominio, memorizza nella cache il "ID chiamata" del controller di dominio in una risorsa di archiviazione stabile, ovvero lo stesso spazio di archiviazione mantenuto coerente con il contenuto del controller di dominio. Il "ID chiamata" di un controller di dominio è un GUID archiviato nell'attributo **invocationID** dell'oggetto servizio del controller di dominio. Per ottenere il nome distinto di un oggetto servizio del controller di dominio, leggere l'attributo **dsServiceName** di RootDSE.

    Tenere presente che quando l'archiviazione stabile dell'applicazione viene ripristinata dal backup, non sono presenti problemi di coerenza perché il nome del controller di dominio, l'ID di chiamata e i limiti inferiori del valore dell'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) vengono archiviati con i dati sincronizzati con il contenuto del controller di dominio.

-   Utilizzare il paging quando si eseguono query sul server, sia le sincronizzazioni complete che quelle incrementali, per evitare la possibilità di recuperare contemporaneamente set di risultati di grandi dimensioni. Per ulteriori informazioni, vedere [specifica di altre opzioni di ricerca](specifying-other-search-options.md).
-   Eseguire query basate sugli indici per evitare di forzare il server a archiviare risultati intermedi di grandi dimensioni quando si utilizzano risultati di paging. Per ulteriori informazioni, vedere [attributi indicizzati](indexed-attributes.md).
-   In generale, non usare l'ordinamento lato server dei risultati della ricerca, che può forzare il server a archiviare e ordinare i risultati intermedi di grandi dimensioni. Si applica alle sincronizzazioni complete e incrementali. Per ulteriori informazioni, vedere [specifica di altre opzioni di ricerca](specifying-other-search-options.md).
-   Non gestire correttamente le condizioni padre. È possibile che l'applicazione riconosca un oggetto prima di aver riconosciuto il relativo padre. A seconda dell'applicazione, questo potrebbe non essere un problema. L'applicazione può sempre leggere lo stato corrente dell'elemento padre dalla directory.
-   Per gestire gli oggetti spostati o eliminati, archiviare l'attributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) di ogni oggetto rilevato. L'attributo **objectGUID** di un oggetto rimane invariato indipendentemente dalla posizione in cui viene spostato nell'insieme di strutture.
-   Per gestire gli oggetti spostati, eseguire sincronizzazioni complete periodiche o aumentare l'ambito di ricerca e filtrare le modifiche non interessanti al termine del client.
-   Per gestire gli oggetti eliminati, eseguire sincronizzazioni complete periodiche oppure eseguire una ricerca separata degli oggetti eliminati quando si esegue una sincronizzazione incrementale. Quando si eseguono query sugli oggetti eliminati, recuperare il [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) degli oggetti eliminati per determinare gli oggetti da eliminare dal database. Per ulteriori informazioni, vedere [recupero di oggetti eliminati](retrieving-deleted-objects.md).
-   Tenere presente che i risultati della ricerca includono solo gli oggetti e gli attributi che il chiamante è autorizzato a leggere (in base ai descrittori di sicurezza e agli elenchi DACL sui vari oggetti). Per ulteriori informazioni, vedere [effetti della protezione sulle query](effects-of-security-on-queries.md).

Per ulteriori informazioni e un esempio di codice in cui vengono illustrate le nozioni di base di un'applicazione di sincronizzazione USNChanged, vedere il [codice di esempio per recuperare le modifiche utilizzando uSNChanged](example-code-to-retrieve-changes-using-usnchanged.md).

 

 