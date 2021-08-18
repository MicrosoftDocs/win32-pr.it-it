---
title: Polling delle modifiche tramite USNChanged
description: È anche possibile ottenere modifiche da Active Directory tramite query sull'attributo uSNChanged, evitando così le limitazioni del controllo DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Polling delle modifiche tramite USNChanged AD
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c665d536eb3dcb0e3265a2e3abb87808ddf630510e5d0600f6185007c72bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025529"
---
# <a name="polling-for-changes-using-usnchanged"></a>Polling delle modifiche tramite USNChanged

Il controllo DirSync è potente ed efficiente, ma presenta due limitazioni significative:

-   Solo per le applicazioni con privilegi elevati: per usare il controllo DirSync, un'applicazione deve essere eseguita con un account con il privilegio **\_ edizione Standard SYNC AGENT \_ \_ NAME** nel controller di dominio. Pochi account hanno così privilegi elevati, quindi un'applicazione che usa il controllo DirSync non può essere eseguita da utenti normali.
-   Nessun ambito del sottoalbero: il controllo DirSync restituisce tutte le modifiche che si verificano all'interno di un contesto dei nomi. Un'applicazione interessata solo alle modifiche che si verificano in un piccolo sottoalbero di un contesto di denominazione deve essere interessata da molte modifiche irrilevanti, che non sono efficienti sia per l'applicazione che per il controller di dominio.

È anche possibile ottenere modifiche da Active Directory tramite query [**sull'attributo uSNChanged,**](/windows/desktop/ADSchema/a-usnchanged) evitando così le limitazioni del controllo DirSync. Questa alternativa non è migliore del controllo DirSync sotto tutti gli aspetti perché comporta la trasmissione di tutti gli attributi quando viene modificato un attributo e richiede più lavoro da parte dello sviluppatore dell'applicazione per gestire correttamente determinati scenari di errore. Attualmente è il modo migliore per scrivere determinate applicazioni di rilevamento delle modifiche.

Quando un controller di dominio modifica un oggetto, imposta l'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) dell'oggetto su un valore maggiore del valore precedente **dell'attributo uSNChanged** per tale oggetto e maggiore del valore corrente dell'attributo **uSNChanged** per tutti gli altri oggetti contenuti in tale controller di dominio. Di conseguenza, un'applicazione può trovare l'oggetto modificato più di recente in un controller di dominio trovando l'oggetto con il valore **uSNChanged più** grande. Il secondo oggetto modificato più di recente in un controller di dominio avrà il secondo valore **uSNChanged** più grande e così via.

[**L'attributo uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) non viene replicato, pertanto la lettura dell'attributo **uSNChanged** di un oggetto in due controller di dominio diversi genererà valori diversi.

Ad esempio, [**l'attributo uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) può essere usato per tenere traccia delle modifiche in un sottoalbero S. Per prima cosa, eseguire una "sincronizzazione completa" del sottoalbero S. Si supponga che il valore **uSNChanged** più grande per qualsiasi oggetto in S sia U. Eseguire periodicamente una query per tutti gli oggetti nel sottoalbero S il cui **valore uSNChanged** è maggiore di U. La query restituirà tutti gli oggetti modificati dopo la sincronizzazione completa. Impostare il valore **uSNChanged più** grande tra questi oggetti modificati e si è pronti per eseguire nuovamente il polling.

Le sottigliezze dell'implementazione di un'applicazione di sincronizzazione [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) includono:

-   Usare **l'attributo highestCommittedUSN** di rootDSE per delimitare i [**filtri uSNChanged.**](/windows/desktop/ADSchema/a-usnchanged) In altre informazioni, prima di avviare una sincronizzazione completa, leggere **il valore highestCommittedUSN** del controller di dominio affiliato. Eseguire quindi una query di sincronizzazione completa (usando i risultati di cui è stato eseguito il paged) per inizializzare il database. Al termine, archiviare il **valore highestCommittedUSN** letto prima della query di sincronizzazione completa. da utilizzare come limiti inferiori **dell'attributo uSNChanged** per la sincronizzazione successiva. Successivamente, per eseguire una sincronizzazione incrementale, leggere nuovamente **l'attributo rootDSE highestCommittedUSN.** Eseguire quindi una query per gli oggetti pertinenti, usando i risultati di pagina, il cui **uSNChanged** è maggiore dei limiti inferiori del **valore dell'attributo uSNChanged** salvato dalla sincronizzazione precedente. Aggiornare il database usando queste informazioni. Al termine, aggiornare i limiti inferiori **dell'attributo uSNChanged** dal **valore highestCommittedUSN** letto prima della query di sincronizzazione incrementale. Archiviare sempre i limiti inferiori del **valore dell'attributo uSNChanged** nella stessa archiviazione che l'applicazione sta sincronizzando con il contenuto del controller di dominio.

    Seguendo questa procedura, anziché in base ai valori [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) sugli oggetti recuperati, si evita di fare in modo che il server eseezioni gli oggetti aggiornati che non rientrano nel set applicabile all'applicazione.

-   Poiché [**uSNChanged è**](/windows/desktop/ADSchema/a-usnchanged) un attributo non replicato, l'applicazione deve essere associata allo stesso controller di dominio ogni volta che viene eseguita. Se non è in grado di eseguire l'associazione a tale controller di dominio, deve attendere fino a quando non è in grado di eseguire questa operazione oppure eseguire una sincronizzazione completa con tale controller di dominio. Quando l'applicazione è affiliata a un controller di dominio, registra il nome DNS di tale controller di dominio nell'archiviazione stabile, ovvero la stessa archiviazione che mantiene coerente con il contenuto del controller di dominio. Usa quindi il nome DNS archiviato per eseguire il binding allo stesso controller di dominio per le sincronizzazioni successive.
-   L'applicazione deve rilevare quando il controller di dominio a cui è attualmente affiliato è stato ripristinato dal backup, perché ciò può causare incoerenza. Quando l'applicazione è affiliata a un controller di dominio, memorizza nella cache l'"ID chiamata" di tale controller di dominio nell'archiviazione stabile, vale a volta la stessa risorsa di archiviazione che mantiene coerente con il contenuto del controller di dominio. L'"ID chiamata" di un controller di dominio è un GUID archiviato **nell'attributo invocationID** dell'oggetto servizio del controller di dominio. Per ottenere il nome distinto dell'oggetto servizio di un controller di dominio, leggere l'attributo **dsServiceName** di rootDSE.

    Tenere presente che quando l'archiviazione stabile dell'applicazione viene ripristinata dal backup non si verificano problemi di coerenza perché il nome del controller di dominio, l'ID chiamata e i limiti inferiori del valore dell'attributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) vengono archiviati con i dati sincronizzati con il contenuto del controller di dominio.

-   Usare il paging durante l'esecuzione di query sul server, sia sincronizzazioni complete che incrementali, per evitare la possibilità di recuperare contemporaneamente set di risultati di grandi dimensioni. Per altre informazioni, vedere [Specifica di altre opzioni di ricerca.](specifying-other-search-options.md)
-   Eseguire query basate su indice per evitare di forzare il server a archiviare risultati intermedi di grandi dimensioni quando si usano risultati di pagina. Per altre informazioni, vedere [Attributi indicizzati](indexed-attributes.md).
-   In generale, non usare l'ordinamento lato server dei risultati della ricerca, che può forzare il server a archiviare e ordinare risultati intermedi di grandi dimensioni. Questo vale sia per le sincronizzazioni complete che per le sincronizzazioni incrementali. Per altre informazioni, vedere [Specifica di altre opzioni di ricerca.](specifying-other-search-options.md)
-   Non gestire correttamente alcuna condizione padre. L'applicazione può riconoscere un oggetto prima che ne riconosca l'elemento padre. A seconda dell'applicazione, potrebbe trattarsi di un problema. L'applicazione può sempre leggere lo stato corrente dell'elemento padre dalla directory.
-   Per gestire gli oggetti spostati o eliminati, archiviare [**l'attributo objectGUID**](/windows/desktop/ADSchema/a-objectguid) di ogni oggetto tracciato. L'attributo **objectGUID di** un oggetto rimane invariato indipendentemente dalla posizione in cui viene spostato nell'intera foresta.
-   Per gestire gli oggetti spostati, eseguire sincronizzazioni complete periodiche o aumentare l'ambito di ricerca e filtrare le modifiche non interessante alla fine del client.
-   Per gestire gli oggetti eliminati, eseguire sincronizzazioni complete periodiche o eseguire una ricerca separata degli oggetti eliminati quando si esegue una sincronizzazione incrementale. Quando si esegue una query per gli oggetti eliminati, recuperare [**l'objectGUID**](/windows/desktop/ADSchema/a-objectguid) degli oggetti eliminati per determinare gli oggetti da eliminare dal database. Per altre informazioni, vedere [Recupero di oggetti eliminati.](retrieving-deleted-objects.md)
-   Tenere presente che i risultati della ricerca includono solo gli oggetti e gli attributi che il chiamante ha l'autorizzazione per leggere (in base ai descrittori di sicurezza e ai DACL nei vari oggetti). Per altre informazioni, vedere [Effetti della sicurezza sulle query](effects-of-security-on-queries.md).

Per altre informazioni e un esempio di codice che illustra le nozioni di base di un'applicazione di sincronizzazione USNChanged, vedere Codice di esempio per recuperare le modifiche [usando USNChanged](example-code-to-retrieve-changes-using-usnchanged.md).

 

 