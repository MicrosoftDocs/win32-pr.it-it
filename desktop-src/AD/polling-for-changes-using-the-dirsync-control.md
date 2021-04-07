---
title: Polling delle modifiche tramite il controllo DirSync
description: Il controllo Active Directory Directory Synchronization (DirSync) è un'estensione del server LDAP che consente a un'applicazione di eseguire la ricerca in una partizione di directory per gli oggetti che sono stati modificati dopo uno stato precedente.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Polling delle modifiche tramite il controllo DirSync AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d105757d39bc25bd10df21ab68c4d1d1202be
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724471"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Polling delle modifiche tramite il controllo DirSync

Il controllo Active Directory Directory Synchronization (DirSync) è un'estensione del server LDAP che consente a un'applicazione di eseguire la ricerca in una partizione di directory per gli oggetti che sono stati modificati dopo uno stato precedente.

Usare il controllo DirSync tramite ADSI specificando la preferenza di ricerca **Ads \_ SEARCHPREF \_ dirsync** quando si usa [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Per altre informazioni e un esempio di codice, vedere [codice di esempio con ADS \_ SEARCHPREF \_ dirsync](example-code-using-ads-searchpref-dirsync.md). È anche possibile eseguire una ricerca DirSync usando l'API LDAP. Di seguito viene descritta l'implementazione di ADSI, la maggior parte delle quali si applica anche all'uso diretto di LDAP, fatta eccezione per quanto illustrato alla fine di questo argomento.

Quando si esegue una ricerca DirSync, si passa un elemento dati specifico del provider (cookie) che identifica lo stato della directory al momento della ricerca DirSync precedente. Per la prima ricerca, viene passato un cookie null e la ricerca restituisce tutti gli oggetti che corrispondono al filtro. La ricerca restituisce anche un cookie valido. Archiviare il cookie nella stessa risorsa di archiviazione che si sta sincronizzando con il server Active Directory. Nelle ricerche successive recuperare il cookie dalla risorsa di archiviazione e passarlo alla richiesta di ricerca. I risultati della ricerca ora includono solo gli oggetti e gli attributi che sono stati modificati dopo lo stato precedente identificato dal cookie. La ricerca restituisce anche un nuovo cookie da archiviare per la ricerca successiva.

La tabella seguente elenca i parametri di ricerca che la richiesta di ricerca del client può specificare.



| Parametro          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base della ricerca | La base di una ricerca DirSync deve essere la radice di una partizione di directory, che può essere una partizione di dominio, la partizione di configurazione o la partizione dello schema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Ambito              | L'ambito di una ricerca DirSync deve essere un sottoalbero dell' **\_ ambito \_ ADS**, ovvero l'intero sottoalbero della partizione. Tenere presente che per la ricerca di una partizione di dominio, il sottoalbero include le intestazioni, ma non il contenuto, delle partizioni di configurazione e dello schema. Per eseguire il polling delle modifiche in un ambito più piccolo, utilizzare la tecnica **uSNChanged** anziché dirsync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtra             | È possibile specificare qualsiasi filtro di ricerca valido. Per una ricerca iniziale con un cookie null, i risultati includono tutti gli oggetti che corrispondono al filtro. Per le ricerche successive con un cookie valido, i risultati della ricerca includono i dati solo per gli oggetti che corrispondono al filtro e sono stati modificati dopo lo stato indicato dal cookie. Per ulteriori informazioni sui filtri di ricerca, vedere [creazione di un filtro query](creating-a-query-filter.md).                                                                                                                                                                                                                                                                                                                |
| Attributi         | È possibile specificare un elenco di attributi da restituire quando si verifica una modifica. Per ogni oggetto, i risultati iniziali includono tutti gli attributi richiesti impostati per l'oggetto. I risultati della ricerca successivi includono solo gli attributi specificati che sono stati modificati. Gli attributi non modificati non vengono inclusi nei risultati della ricerca. Nell'implementazione di ADSI i risultati della ricerca includono sempre **objectGUID** e **instanceType** di ogni oggetto. Inoltre, l'elenco di attributi specificato funge da filtro aggiuntivo. i risultati della ricerca iniziale includono solo gli oggetti per i quali è stato impostato almeno uno degli attributi specificati. nelle ricerche successive sono inclusi solo gli oggetti in cui uno o più attributi sono stati modificati (valori aggiunti o eliminati). |



 

Tenere inoltre presente quanto segue:

-   Per le ricerche incrementali, la procedura consigliata consiste nell'associare lo stesso controller di dominio usato nella ricerca precedente, ovvero il controller di dominio che ha generato il cookie. Se lo stesso controller di dominio non è disponibile, attendere che sia o eseguire un'associazione a un nuovo controller di dominio ed eseguire una sincronizzazione completa. Archiviare il nome DNS del controller di dominio nell'archivio secondario con il cookie.

    È possibile passare un cookie generato da un controller di dominio a un controller di dominio diverso che ospita una replica della stessa partizione di directory. Non è possibile che un client perda le modifiche utilizzando un cookie da un controller di dominio in un altro controller di dominio. Tuttavia, è possibile che i risultati della ricerca del nuovo controller di dominio includano le modifiche segnalate dal DC precedente; in alcuni casi, il nuovo controller di dominio può restituire tutti gli oggetti e gli attributi, come con una sincronizzazione completa. Il client deve semplicemente rendere il proprio database coerente con i risultati della ricerca segnalati per una determinata chiamata a DirSync, ovvero gestire tutti i risultati incrementali come se fossero lo stato più recente. Non è importante sapere se la modifica è stata apportata prima o addirittura a uno stato precedente perché le sincronizzazioni incrementali ripetute convergeranno sulla coerenza.

-   Quando un oggetto viene rinominato o spostato, i relativi oggetti figlio, se presenti, non vengono inclusi nei risultati della ricerca, anche se i nomi distinti degli oggetti figlio sono stati modificati. Analogamente, quando una voce ACE ereditabile viene modificata in un descrittore di sicurezza dell'oggetto, gli oggetti figlio dell'oggetto non vengono inclusi nei risultati della ricerca, anche se i descrittori di sicurezza degli oggetti figlio sono stati modificati.
-   Usare l'attributo **objectGUID** per identificare gli oggetti rilevati. Il **objectGUID** di ogni oggetto rimane invariato indipendentemente dalla posizione in cui l'oggetto viene spostato all'interno dell'insieme di strutture.
-   Tenere presente che i risultati della ricerca di una ricerca DirSync indicano lo stato degli oggetti in una replica della partizione di directory al momento della ricerca. Ciò significa che le modifiche apportate agli altri controller di dominio non verranno incluse se non sono state replicate nel controller di dominio di destinazione. Significa anche che gli attributi di un oggetto possono essere stati modificati più volte dalla ricerca DirSync precedente, ma la ricerca visualizzerà solo lo stato finale, non la sequenza di modifiche.
-   Nell'implementazione di ADSI, l'applicazione deve gestire il cookie come opaco e non creare presupposti sul valore o sull'organizzazione interna.
-   Tenere presente che il client archivia il cookie, la lunghezza dei cookie e il nome DNS del controller di dominio nella stessa risorsa di archiviazione che contiene i dati dell'oggetto sincronizzato. In questo modo si garantisce che il cookie e gli altri parametri rimangano sincronizzati con i dati dell'oggetto se l'archiviazione viene ripristinata da un backup.
-   Per recuperare l'attributo [**parentGUID**](/windows/desktop/ADSchema/a-parentguid) , costruito per il controllo DirSync, è anche necessario richiedere l'attributo [**Name**](/windows/desktop/ADSchema/a-name) .

Per usare il controllo DirSync, il chiamante deve avere il diritto "directory Get Changes" assegnato alla radice della partizione monitorata. Per impostazione predefinita, questo diritto viene assegnato agli account Administrator e LocalSystem nei controller di dominio. Il chiamante deve avere anche il diritto di accesso per il controllo esteso [**DS-Replication-Get-Changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) . Per ulteriori informazioni sull'implementazione di un meccanismo di rilevamento delle modifiche per le applicazioni che devono essere eseguite con un account che non dispone di questo diritto, vedere [polling delle modifiche con uSNChanged](polling-for-changes-using-usnchanged.md). Per ulteriori informazioni sui privilegi, vedere [privilegi](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Recupero di oggetti eliminati con una ricerca DirSync

I risultati della ricerca di **Ads \_ SEARCHPREF \_ dirsync** includono automaticamente oggetti eliminati (Tombstone) che corrispondono al filtro di ricerca specificato. Tuttavia, un filtro di ricerca che corrisponderà a un oggetto quando è attivo potrebbe non corrispondere all'oggetto dopo l'eliminazione. Questo perché la rimozione definitiva mantiene solo un subset degli attributi presenti nell'oggetto originale. Ad esempio, si usa in genere il filtro seguente per gli oggetti utente.


```C++
(&(objectClass=user)(objectCategory=person))
```



L'attributo **objectCategory** viene rimosso quando viene eliminato un oggetto, quindi il filtro precedente non corrisponde ad alcun oggetto contrassegnato per la rimozione definitiva. Viceversa, l'attributo **objectClass** viene mantenuto sugli oggetti contrassegnati per la rimozione definitiva, quindi un filtro di "(objectClass = user)" corrisponderà a oggetti utente eliminati.

L'elenco di attributi specificato con una ricerca DirSync funge anche da filtro; i risultati della ricerca includono solo oggetti in cui uno o più attributi specificati sono stati modificati dopo la ricerca DirSync precedente. Se nell'elenco di attributi non sono inclusi attributi conservati per la rimozione definitiva, i risultati della ricerca non includeranno oggetti contrassegnati per la rimozione definitiva. Per gestire questo problema, richiedere tutti gli attributi specificando un elenco di attributi null; in alternativa, è possibile richiedere l'attributo **eliminato** , impostare su **true** per tutte le lapidi. Per gli attributi Tombstone il bit 0x8 è impostato nell'attributo **searchFlags** della definizione **attributeSchema** .

Per ulteriori informazioni, vedere [recupero di oggetti eliminati](retrieving-deleted-objects.md).

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implementazione LDAP del controllo DirSync

È anche possibile eseguire una ricerca DirSync usando l'API LDAP con il controllo [ \_ \_ \_ OID del server LDAP](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) . Se si usa l'API LDAP, specificare anche l' [ \_ \_ \_ \_ OID del server LDAP esteso](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) e il [server LDAP Visualizza i controlli \_ \_ \_ \_ OID eliminati](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . Il \_ \_ controllo OID di DN esteso del server LDAP causa la restituzione di una \_ \_ forma estesa del nome distinto che include **objectGUID** e **objectSID** per gli oggetti entità di sicurezza, ad esempio utenti, gruppi e computer. Il \_ \_ controllo OID eliminato del server LDAP indica \_ \_ che i risultati della ricerca includono i dati per gli oggetti eliminati. Tenere presente che questi controlli vengono inclusi automaticamente nell'implementazione di ADSI.

 

 