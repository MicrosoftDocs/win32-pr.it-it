---
title: Polling delle modifiche tramite il controllo DirSync
description: Il controllo Sincronizzazione directory Active Directory (DirSync) è un'estensione del server LDAP che consente a un'applicazione di cercare in una partizione di directory gli oggetti modificati dopo uno stato precedente.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Polling delle modifiche tramite il controllo DirSync ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b95e9fed93a962ef95e8cdbe08c202bd8e46df21959d9e1fcabe8eac033b6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185408"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Polling delle modifiche tramite il controllo DirSync

Il controllo Sincronizzazione directory Active Directory (DirSync) è un'estensione del server LDAP che consente a un'applicazione di cercare in una partizione di directory gli oggetti modificati dopo uno stato precedente.

Usare il controllo DirSync tramite ADSI specificando la preferenza di ricerca **\_ ADS SEARCHPREF \_ DIRSYNC** quando si [**usa IDirectorySearch.**](/windows/desktop/api/iads/nn-iads-idirectorysearch) Per altre informazioni e un esempio di codice, vedere [Codice di esempio con ADS \_ SEARCHPREF \_ DIRSYNC.](example-code-using-ads-searchpref-dirsync.md) È anche possibile eseguire una ricerca DirSync usando l'API LDAP. Di seguito viene descritta l'implementazione di ADSI, la maggior parte delle quali si applica anche all'uso diretto di LDAP, ad eccezione di quanto descritto alla fine di questo argomento.

Quando si esegue una ricerca DirSync, si passa un elemento dati specifico del provider (cookie) che identifica lo stato della directory al momento della ricerca di DirSync precedente. Per la prima ricerca, si passa un cookie Null e la ricerca restituisce tutti gli oggetti che corrispondono al filtro. La ricerca restituisce anche un cookie valido. Archiviare il cookie nella stessa archiviazione che si sta sincronizzando con il server Active Directory. Nelle ricerche successive ottenere il cookie dalla memoria e passarlo con la richiesta di ricerca. I risultati della ricerca ora includono solo gli oggetti e gli attributi modificati dopo lo stato precedente identificato dal cookie. La ricerca restituisce anche un nuovo cookie da archiviare per la ricerca successiva.

Nella tabella seguente sono elencati i parametri di ricerca che possono essere specificati dalla richiesta di ricerca del client.



| Parametro          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base della ricerca | La base di una ricerca DirSync deve essere la radice di una partizione di directory, che può essere una partizione di dominio, la partizione di configurazione o la partizione dello schema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Ambito              | L'ambito di una ricerca DirSync deve essere **ADS \_ SCOPE \_ SUBTREE,** che è l'intero sottoalbero della partizione. Tenere presente che per una ricerca di una partizione di dominio, il sottoalbero include le testine, ma non il contenuto, delle partizioni di configurazione e dello schema. Per eseguire il polling delle modifiche in un ambito più piccolo, usare la **tecnica USNChanged** anziché DirSync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtra             | È possibile specificare qualsiasi filtro di ricerca valido. Per una ricerca iniziale con un cookie Null, i risultati includono tutti gli oggetti che corrispondono al filtro. Per le ricerche successive con un cookie valido, i risultati della ricerca includono solo i dati relativi agli oggetti che corrispondono al filtro e sono cambiati dopo lo stato indicato dal cookie. Per altre informazioni sui filtri di ricerca, vedere [Creazione di un filtro query.](creating-a-query-filter.md)                                                                                                                                                                                                                                                                                                                |
| Attributi         | È possibile specificare un elenco di attributi da restituire quando si verifica una modifica. Per ogni oggetto, i risultati iniziali includono tutti gli attributi richiesti impostati sull'oggetto. I risultati della ricerca successivi includono solo gli attributi specificati che sono stati modificati. Gli attributi non modificati non vengono inclusi nei risultati della ricerca. Nell'implementazione di ADSI i risultati della ricerca includono sempre **objectGUID** **e instanceType** di ogni oggetto. Inoltre, l'elenco di attributi specificato funge da filtro aggiuntivo: i risultati della ricerca iniziali includono solo gli oggetti con almeno uno degli attributi specificati impostati; Le ricerche successive includono solo gli oggetti in cui uno o più attributi sono stati modificati (valori aggiunti o eliminati). |



 

Tenere inoltre presente che:

-   Per le ricerche incrementali, è consigliabile eseguire l'associazione allo stesso controller di dominio usato nella ricerca precedente, ovvero il controller di dominio che ha generato il cookie. Se lo stesso controller di dominio non è disponibile, attendere fino a quando non lo è oppure eseguire l'associazione a un nuovo controller di dominio ed eseguire una sincronizzazione completa. Archiviare il nome DNS del controller di dominio nella memoria secondaria con il cookie.

    È possibile passare un cookie generato da un controller di dominio a un controller di dominio diverso che ospita una replica della stessa partizione di directory. Non è possibile che un client non superi le modifiche usando un cookie di un controller di dominio in un altro controller di dominio. Tuttavia, è possibile che i risultati della ricerca dal nuovo controller di dominio includano le modifiche segnalate dal controller di dominio precedente; In alcuni casi, il nuovo controller di dominio può restituire tutti gli oggetti e gli attributi, come con una sincronizzazione completa. Il client deve semplicemente rendere il database coerente con i risultati della ricerca segnalati per qualsiasi chiamata DirSync specificata, in altre informazioni, gestire tutti i risultati incrementali come se fossero lo stato più recente. Non è importante se la modifica è stata osservata in precedenza o se si torna a uno stato precedente, perché le sincronizzazioni incrementali ripetute convergono sulla coerenza.

-   Quando un oggetto viene rinominato o spostato, gli eventuali oggetti figlio non vengono inclusi nei risultati della ricerca, anche se i nomi distinti degli oggetti figlio sono stati modificati. Analogamente, quando una ACE ereditabile viene modificata in un descrittore di sicurezza dell'oggetto, gli oggetti figlio dell'oggetto non vengono inclusi nei risultati della ricerca, anche se i descrittori di sicurezza degli oggetti figlio sono stati modificati.
-   Usare **l'attributo objectGUID** per identificare gli oggetti tracciati. **L'objectGUID di** ogni oggetto rimane invariato indipendentemente dalla posizione in cui l'oggetto viene spostato all'interno della foresta.
-   Tenere presente che i risultati della ricerca di dirSync indicano lo stato degli oggetti in una replica della partizione di directory al momento della ricerca. Ciò significa che le modifiche apportate in altri controller di dominio non verranno incluse se non sono state replicate nel controller di dominio di destinazione. Significa anche che gli attributi di un oggetto potrebbero essere cambiati più volte rispetto alla ricerca di DirSync precedente, ma la ricerca mostrerà solo lo stato finale, non la sequenza di modifiche.
-   Nell'implementazione di ADSI, l'applicazione deve gestire il cookie come opaco e non fare ipotesi sull'organizzazione o sul valore interno.
-   Tenere presente che il client archivia il cookie, la lunghezza del cookie e il nome DNS del controller di dominio nella stessa archiviazione che contiene i dati dell'oggetto sincronizzati. Ciò garantisce che il cookie e altri parametri rimangano sincronizzati con i dati dell'oggetto se l'archiviazione viene ripristinata da un backup.
-   Per recuperare [**l'attributo parentGUID,**](/windows/desktop/ADSchema/a-parentguid) costruito per il controllo DirSync, è anche necessario richiedere [**l'attributo name.**](/windows/desktop/ADSchema/a-name)

Per usare il controllo DirSync, il chiamante deve avere il diritto "directory get changes" assegnato alla radice della partizione monitorata. Per impostazione predefinita, questo diritto viene assegnato agli account Administrator e LocalSystem nei controller di dominio. Il chiamante deve anche disporre del diritto di accesso di controllo esteso [**DS-Replication-Get-Changes.**](/windows/desktop/ADSchema/r-ds-replication-get-changes) Per altre informazioni sull'implementazione di un meccanismo di rilevamento delle modifiche per le applicazioni che devono essere eseguite con un account che non dispone di questo diritto, vedere Polling delle modifiche tramite [USNChanged.](polling-for-changes-using-usnchanged.md) Per altre informazioni sui privilegi, vedere [Privilegi](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Recupero di oggetti eliminati con una ricerca DirSync

I **risultati della ricerca \_ ADS SEARCHPREF \_ DIRSYNC** includono automaticamente gli oggetti eliminati (oggetti contrassegnati per la rimozione definitiva) che corrispondono al filtro di ricerca specificato. Tuttavia, un filtro di ricerca che corrisponderà a un oggetto quando è live potrebbe non corrispondere all'oggetto dopo l'eliminazione. Ciò è dovuto al fatto che gli oggetti contrassegnati per la rimozione definitiva mantengono solo un subset degli attributi presenti nell'oggetto originale. Ad esempio, in genere si usa il filtro seguente per gli oggetti utente.


```C++
(&(objectClass=user)(objectCategory=person))
```



**L'attributo objectCategory** viene rimosso quando viene eliminato un oggetto, quindi il filtro precedente non corrisponde ad alcun oggetto contrassegnato per la rimozione definitiva. Al contrario, **l'attributo objectClass** viene mantenuto per gli oggetti contrassegnati per la rimozione definitiva, quindi un filtro "(objectClass=user)" corrisponde agli oggetti utente eliminati.

L'elenco di attributi specificato con una ricerca DirSync funge anche da filtro. I risultati della ricerca includono solo gli oggetti in cui uno o più attributi specificati sono stati modificati dopo la ricerca DirSync precedente. Se l'elenco di attributi non include attributi mantenuti per gli elementi contrassegnati per la rimozione definitiva, i risultati della ricerca non includeranno gli elementi contrassegnati per la rimozione definitiva. Per gestire questo problema, richiedere tutti gli attributi specificando un elenco di attributi Null. in caso contrario, è possibile richiedere **l'attributo isDeleted,** impostato su **TRUE** per tutti gli elementi contrassegnati per la rimozione definitiva. Gli attributi di rimozione definitiva 0x8 bit impostato **nell'attributo searchFlags** della **definizione attributeSchema.**

Per altre informazioni, vedere [Recupero di oggetti eliminati.](retrieving-deleted-objects.md)

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implementazione LDAP del controllo DirSync

È anche possibile eseguire una ricerca DirSync usando l'API LDAP con il controllo LDAP [ \_ SERVER \_ DIRSYNC \_ OID.](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) Se si usa l'API LDAP, specificare anche i controlli [LDAP \_ SERVER EXTENDED \_ \_ DN \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) e [LDAP SERVER SHOW DELETED \_ \_ \_ \_ OID.](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) Il controllo OID LDAP SERVER EXTENDED DN fa in modo che una ricerca LDAP restituirà una forma estesa del nome distinto che include objectGUID e \_ \_ \_ \_ **objectSID**  per gli oggetti entità di sicurezza, ad esempio utenti, gruppi e computer. Il controllo LDAP SERVER SHOW DELETED OID fa \_ sì che i risultati della ricerca \_ \_ \_ includano i dati per gli oggetti eliminati. Tenere presente che questi controlli vengono inclusi automaticamente nell'implementazione di ADSI.

 

 