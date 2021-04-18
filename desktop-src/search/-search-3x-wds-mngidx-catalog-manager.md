---
description: Le interfacce ISearchCatalogManager e ISearchCatalogManager2 forniscono metodi per la gestione di un catalogo di ricerca, ad esempio causando la reindicizzazione o l'impostazione di timeout.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Utilizzo di gestione cataloghi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1295cc9cc76fb334b4687b876fa1959a22e33235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306184"
---
# <a name="using-the-catalog-manager"></a>Utilizzo di gestione cataloghi

Le interfacce [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) forniscono metodi per la gestione di un catalogo di ricerca, ad esempio causando la reindicizzazione o l'impostazione di timeout. Sebbene Windows Search usi attualmente un solo catalogo, questa interfaccia è stata progettata per fornire un maggiore controllo sulla gestione di più cataloghi in modo indipendente. L'interfaccia gestisce il catalogo nei modi seguenti:

- Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste da gestione dell'ambito di ricerca per indicizzazione, notifiche delle modifiche dei dati e interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .
- Contenuto del catalogo: garantire che i nuovi dati vengano indicizzati e che le applicazioni e i componenti funzionino correttamente forzando la reindicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.
- Proprietà del catalogo: impostazione delle proprietà che determinano il modo in cui il catalogo gestisce i timeout durante la connessione ai gestori di protocollo e il modo in cui i segni diacritici vengono trattati nelle ricerche.
- Stato del catalogo: ottenere informazioni sul catalogo, tra cui lo stato, le dimensioni e lo stato dell'attività corrente.

Questo argomento è organizzato nel modo seguente:

- [Accesso alle interfacce correlate](#accessing-related-interfaces)
- [Gestione del contenuto del catalogo](#managing-the-catalog-contents)
- [Gestione dello stato del catalogo](#managing-catalog-status)
- [Gestione delle proprietà del catalogo](#managing-catalog-properties)
- [Esecuzione in modalità con privilegi elevati](#running-in-elevated-mode)
- [Argomenti correlati](#related-topics)

## <a name="accessing-related-interfaces"></a>Accesso alle interfacce correlate

Per poter usare alcune interfacce utili nella piattaforma di ricerca Windows, è necessario disporre di un'istanza del gestore del catalogo. Per creare un gestore di cataloghi per un catalogo specificato, chiamare il metodo [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) . I metodi di gestione del catalogo possono quindi essere utilizzati per creare un'istanza e restituire interfacce basate sul catalogo specificato.

| Metodo                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Ottiene un'istanza dell'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per il catalogo corrente, per consentire la compilazione di query in modo semplice.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Ottiene un'istanza di [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per il catalogo di ricerca, per consentire agli sviluppatori di modificare l'ambito di ricerca per indicizzazione dell'indicizzatore di ricerca di Windows.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Ottiene un'istanza dell'interfaccia [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) , che le applicazioni client utilizzano per notificare all'indicizzatore le modifiche quando il client desidera ottenere informazioni sullo stato di indicizzazione dell'elemento per supportare le notifiche gestite dal provider. Per ulteriori informazioni, vedere [notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md) . |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Ottiene un'istanza di [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), che le applicazioni client utilizzano per notificare all'indicizzatore le modifiche quando il client non desidera informazioni sullo stato di indicizzazione (notifiche gestite dall'indicizzatore). Per ulteriori informazioni, vedere [notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md) .            |

## <a name="managing-the-catalog-contents"></a>Gestione del contenuto del catalogo

Per la gestione del catalogo sono necessarie due attività principali, ovvero la reindicizzazione di tutti gli URL nell'ambito della ricerca per indicizzazione dell'indicizzatore e la reimpostazione dell'intero catalogo sottostante. Quando si reindicizzano gli URL, i dati precedenti rimangono nel catalogo fino a o a meno che non vengano sostituiti da nuovi dati. Quando si reimposta il catalogo, viene ricompilato l'intero catalogo e tutti gli URL nell'ambito della ricerca per indicizzazione vengono nuovamente indicizzati. Questo processo può richiedere molto tempo e deve essere usato solo come ultima risorsa per la risoluzione dei problemi, ad esempio un indice potenzialmente danneggiato.

Quando si installa una nuova applicazione, un gestore di protocollo o un filtro, l'applicazione di installazione deve aggiungere la directory o la radice all'ambito di ricerca per assicurarsi che l'indicizzatore includa il percorso dei dati dell'applicazione. Se i dati non vengono visualizzati nel catalogo dopo che l'indicizzatore ha effettuato la ricerca per indicizzazione nell'ambito della ricerca per indicizzazione, è necessario innanzitutto assicurarsi che il percorso dei dati sia incluso nell'ambito della ricerca per indicizzazione. È possibile aggiungerla usando l'interfaccia utente per le opzioni di ricerca di Windows o il gestore dell'ambito di ricerca per [indicizzazione](-search-3x-wds-extidx-csm.md). Se il percorso sembra trovarsi nell'ambito della ricerca per indicizzazione, è possibile forzare manualmente una reindicizzazione di tutti gli URL nell'ambito della ricerca per indicizzazione dell'indicizzatore o in un subset, usando i metodi seguenti dell'interfaccia [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .

| Metodo di reindicizzazione                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager:: REINDEX**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Indicizza nuovamente tutti gli URL nel catalogo. Le informazioni precedenti rimarranno fino a quando non vengono sostituite con nuove informazioni.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Indicizza nuovamente gli URL che corrispondono al modello o iniziano in corrispondenza di una particolare radice, ad esempio file:///C: \\ FolderName \\ SubfolderName \\ . Questa operazione è utile per rieseguire la ricerca per indicizzazione di tutti gli elementi in una particolare directory o con un'estensione specifica, ad esempio quando viene installata un'applicazione. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Indica all'indicizzatore di classificare in ordine di priorità gli elementi di indicizzazione con URL che corrispondono a un modello specificato rispetto al completamento di altre attività di indicizzazione.                                                                                                                                    |

**Reimpostazione dell'indice.** È possibile reimpostare l'intero indice con una chiamata a [**ISearchCatalogManager:: Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Il catalogo sottostante viene reimpostato ricompilando i database ed eseguendo un indice completo di tutti gli URL nell'ambito della ricerca per indicizzazione. Questo processo può richiedere molto tempo e deve essere usato solo come ultima risorsa per la risoluzione dei problemi, ad esempio un indice potenzialmente danneggiato.

> [!IMPORTANT]
> A causa del rallentamento nell'indicizzazione che questi metodi possono causare, devono essere usati con cautela quando si tenta di identificare i problemi di indicizzazione o di catalogo. Assicurarsi prima di tutto che le radici di ricerca e le regole di ambito vengano aggiunte in Gestione ambito ricerca per indicizzazione e quindi assicurarsi che il bit appropriato (attributo file non contenuto indicizzato) sia impostato correttamente per file e cartelle. Se è stato confermato che questi sono corretti, provare prima ReindexSearchRoot e reindicizzare per ultimo. Se nessuno di questi lavori, provare a reimpostare come ultima risorsa.

Per informazioni correlate, vedere [notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)ed esecuzione di [query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Gestione dello stato del catalogo

Il gestore del catalogo può essere utilizzato per ottenere lo stato del catalogo per le applicazioni che desiderano personalizzare la modalità di gestione del catalogo (ad esempio, un'applicazione di monitoraggio "stato catalogo" personalizzata). Tuttavia, la gestione del catalogo non è in genere necessaria per la maggior parte degli scenari di sviluppo correlati alla ricerca. Gli usi comuni si riferiscono a un'applicazione di monitoraggio "stato del catalogo" o a un'applicazione di tipo pannello di controllo.

Nella tabella seguente vengono descritti i metodi di ISearchCatalogManager utilizzati per la gestione dello stato del catalogo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a></td>
<td>Ottiene l'URL attualmente indicizzato. Questo metodo è utile se si tenta di identificare se l'indicizzatore è stato &quot; bloccato &quot; su un elemento.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a></td>
<td>Ottiene il numero di elementi nel catalogo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a></td>
<td>Recupera le informazioni seguenti sugli elementi da indicizzare:
<ul>
<li>plIncrementalCount: numero di elementi da indicizzare nell'indice incrementale successivo</li>
<li>plNotificationQueue: numero di elementi nella coda di notifiche. Queste informazioni sono utili per un'applicazione di notifica che ha dovuto controllare se l'indicizzatore riceve le notifiche che l'applicazione sta inviando.</li>
<li>plHighPriorityQueue: numero di elementi nella coda ad alta priorità. Gli elementi in plHighPriorityQueue vengono indicizzati per primi.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a></td>
<td>Ottiene lo stato del catalogo e restituisce un valore di enumerazione che fornisce lo stato corrente. Di seguito sono riportati i possibili stati del catalogo:
<ul>
<li>Idle: non è necessaria alcuna indicizzazione.</li>
<li>Paused: l'indicizzazione viene sospesa (ad esempio a causa di una batteria insufficiente o di un utilizzo elevato della CPU).</li>
<li>Ripristino: l'indicizzazione è in ripristino.</li>
<li>Ricerca per indicizzazione completa: l'indicizzatore sta eseguendo una ricerca per indicizzazione completa dell'ambito.</li>
<li>Ricerca per indicizzazione incrementale: l'indicizzatore esegue una ricerca per indicizzazione incrementale.</li>
<li>Notifiche di elaborazione: l'indicizzatore sta elaborando le notifiche.</li>
<li>Chiusura: è in corso l'arresto dell'indicizzatore.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>Ottiene il nome del catalogo corrente specificato nel metodo <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager:: getCatalog</strong></a> . Attualmente, l'unico catalogo supportato è SystemIndex.</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>Gestione delle proprietà del catalogo

Con gestione catalogo è possibile gestire tre proprietà del catalogo:

- **Distinzione segni diacritici.** I segni diacritici sono contrassegni accentati aggiunti a lettere per indicare il significato o la pronuncia di una parola. Questa proprietà determina se il catalogo è sensibile ai segni diacritici ed è importante quando l'utente o gli utenti ricercano e indicizzano testo in più lingue. Con questa proprietà impostata su **false**, ad esempio, il catalogo considera "Resume" e "curriculum" come se fossero la stessa parola.
- **Timeout della connessione.** Questa proprietà rappresenta la quantità di tempo di attesa per una risposta di connessione da un server o un archivio dati, come rappresentato in una struttura di [**\_ informazioni sul timeout**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . È possibile utilizzare questa proprietà per ottimizzare la ricerca di Windows.
- **Timeout dei dati** Questa proprietà rappresenta la quantità di tempo di attesa per una transazione dati tra l'indicizzatore e un gestore di protocollo o un filtro, come rappresentato in una struttura di [**\_ informazioni sul timeout**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Se questo tempo è scaduto, il processo dal daemon di filtri viene terminato per evitare deadlock e altri problemi di risorse.

Le ultime due proprietà sono destinate principalmente a un uso futuro. Ognuna di queste proprietà include `get` i `put` metodi e.

| Metodo                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**Inserisci \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE se il catalogo deve distinguere le parole con i segni diacritici. **False** se il catalogo deve ignorare i segni diacritici. Per modificare questa proprietà, è necessario ricompilare l'indice perché le chiavi dell'indice potrebbero diventare non valide.                       |
| [**ottenere \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**Inserisci \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Tempo, in secondi, durante il quale l'indicizzatore deve attendere una risposta di connessione da un server o da un archivio dati. L'impostazione di un valore troppo alto può causare ritardi se molti siti non rispondono. L'impostazione di un valore troppo basso può comportare l'indicizzazione di alcuni siti. |
| [**Ottieni \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**Inserisci \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Tempo, in secondi, durante il quale l'indicizzatore deve attendere una transazione di dati.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Esecuzione in modalità con privilegi elevati

Tutte le chiamate al metodo che aggiornano SystemIndex richiedono l'esecuzione dell'applicazione con privilegi elevati. In caso contrario, l'applicazione avrà esito negativo con un errore di accesso negato.

## <a name="related-topics"></a>Argomenti correlati


[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Interfacce per la gestione dell'indice](interfaces-for-managing-the-index.md)

[Utilizzo di gestione ricerche](-search-3x-wds-mngidx-searchmanager.md)

[Utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
