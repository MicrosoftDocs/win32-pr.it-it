---
description: Le interfacce ISearchCatalogManager e ISearchCatalogManager2 forniscono metodi per gestire un catalogo di ricerca, ad esempio causando la nuova indicizzazione o l'impostazione di timeout.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Uso di Gestione cataloghi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deffc748c504b056e9d3f92dc8dcb127b835bec6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472327"
---
# <a name="using-the-catalog-manager"></a>Uso di Gestione cataloghi

Le [**interfacce ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) forniscono metodi per gestire un catalogo di ricerca, ad esempio causando la nuova indicizzazione o l'impostazione di timeout. Anche Windows ricerca usa attualmente un solo catalogo, questa interfaccia è stata progettata per offrire un maggiore controllo per la gestione indipendente di più cataloghi. L'interfaccia gestisce il catalogo nei modi seguenti:

- Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste dall'Gestione ambito ricerca per indicizzazione, dalle notifiche di modifica dei dati e [**dall'interfaccia ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)
- Contenuto del catalogo: assicura che i nuovi dati siano indicizzati e che altri componenti e applicazioni funzionino correttamente forzando una nuova indicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.
- Proprietà del catalogo: impostazione di proprietà che determinano il modo in cui il catalogo gestisce i timeout durante la connessione ai gestori di protocollo e il modo in cui i contrassegni diacritici vengono gestiti nelle ricerche.
- Stato del catalogo: recupero di informazioni sul catalogo, inclusi lo stato, le dimensioni e lo stato dell'attività corrente.

Questo argomento è organizzato come segue:

- [Accesso alle interfacce correlate](#accessing-related-interfaces)
- [Gestione del contenuto del catalogo](#managing-the-catalog-contents)
- [Gestione dello stato del catalogo](#managing-catalog-status)
- [Gestione delle proprietà del catalogo](#managing-catalog-properties)
- [Esecuzione in modalità con privilegi elevati](#running-in-elevated-mode)
- [Argomenti correlati](#related-topics)

## <a name="accessing-related-interfaces"></a>Accesso alle interfacce correlate

Alcune interfacce utili nella piattaforma Windows ricerca richiedono un'istanza di Catalog Manager prima di poter essere usate. Per creare un gestore del catalogo per un catalogo specificato, chiamare il [**metodo ISearchManager::GetCatalog.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) I metodi di Gestione cataloghi possono quindi essere usati per creare un'istanza e restituire interfacce basate sul catalogo specificato.

| Metodo                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Ottiene un'istanza [**dell'interfaccia ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per il catalogo corrente, per consentire di compilare facilmente le query.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Ottiene un'istanza di [**ISearch CrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per questo catalogo di ricerca, per consentire agli sviluppatori di modificare l'ambito della ricerca per indicizzazione Windows Indexer di ricerca.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Ottiene un'istanza dell'interfaccia [**ISearchItemsChangedSink,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) utilizzata dalle applicazioni client per notificare all'indicizzatore le modifiche quando il client desidera che le informazioni sullo stato dell'indicizzazione sull'elemento supportino le notifiche gestite dal provider. Per [altre informazioni, vedere Notifica dell'indice](-search-3x-wds-notifyingofchanges.md) delle modifiche. |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Ottiene un'istanza di [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)che le applicazioni client usano per notificare all'indicizzatore le modifiche quando il client non desidera indicizzare le informazioni sullo stato (notifiche gestite dall'indicizzatore). Per [altre informazioni, vedere Notifica dell'indice](-search-3x-wds-notifyingofchanges.md) delle modifiche.            |

## <a name="managing-the-catalog-contents"></a>Gestione del contenuto del catalogo

La gestione del catalogo comporta due attività principali: la reimpostazione di tutti o alcuni URL nell'ambito della ricerca per indicizzazione dell'indicizzatore e la reimpostazione dell'intero catalogo sottostante. Quando si indicizzano nuovamente gli URL, i dati meno datati rimangono nel catalogo fino a quando o non vengono sostituiti da nuovi dati. Quando si reimposta il catalogo, l'intero catalogo viene ricompilato e tutti gli URL nell'ambito della ricerca per indicizzazione vengono indicizzati nuovamente. Questo processo può richiedere molto tempo e deve essere usato solo come ultima risorsa per risolvere problemi come un indice probabilmente danneggiato.

Quando si installa una nuova applicazione, un gestore di protocollo o un filtro, l'applicazione di installazione deve aggiungere la directory o la radice all'ambito della ricerca per indicizzazione per assicurarsi che l'indicizzatore includa il percorso dei dati dell'applicazione. Se i dati non vengono visualizzati nel catalogo dopo che l'indicizzatore ha sottoposto a ricerca per indicizzazione l'ambito della ricerca per indicizzazione, è prima necessario assicurarsi che il percorso dei dati sia incluso nell'ambito della ricerca per indicizzazione. È possibile aggiungerlo usando l'interfaccia utente per le Windows di ricerca o [Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md). Se il percorso sembra essere nell'ambito della ricerca per indicizzazione, è possibile forzare manualmente una nuova indicizzazione di tutti gli URL nell'ambito della ricerca per indicizzazione dell'indicizzatore o in un subset, usando i metodi seguenti [**dell'interfaccia ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

| Metodo di indicizzazione di nuovo                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager::Reindex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Indicizza nuovamente tutti gli URL nel catalogo. Le informazioni non aggiornate rimarranno finché non vengono sostituite da nuove informazioni.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Indicizza nuovamente gli URL che corrispondono al modello o iniziano da una determinata radice (ad esempio, file:///C: \\ Nome \\ CartellaNome sottocartella \\ ). Ciò è utile per riecrivare tutti gli elementi in una determinata directory o con una determinata estensione, come quando viene installata un'applicazione. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Indica all'indicizzatore di assegnare priorità agli elementi di indicizzazione con URL che corrispondono a un modello specificato rispetto al completamento di altre attività di indicizzazione.                                                                                                                                    |

**Reimpostazione dell'indice.** È possibile reimpostare l'intero indice con una chiamata a [**ISearchCatalogManager::Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). In questo modo viene reimpostato il catalogo sottostante ricompilando i database ed eseguendo un indice completo di tutti gli URL nell'ambito della ricerca per indicizzazione. Questo processo può richiedere molto tempo e deve essere usato solo come ultima risorsa per risolvere problemi come un indice probabilmente danneggiato.

> [!IMPORTANT]
> A causa del rallentamento dell'indicizzazione che questi metodi possono causare, è consigliabile usare questi metodi con attenzione quando si tenta di identificare i problemi di indicizzazione o catalogo. Assicurarsi prima di tutto che le radici di ricerca e le regole di ambito siano aggiunte nel Gestione ambito ricerca per indicizzazione e quindi assicurarsi che il bit FANCI (Attributo file non indicizzato) sia impostato correttamente per file e cartelle. Se è stato confermato che sono corretti, provare prima ReindexSearchRoot e Reindicizzare per ultimo. Se nessuna di queste operazioni funziona, provare a reimpostare come ultima risorsa.

Per informazioni correlate, vedere [Notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)ed Esecuzione di query [sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Gestione dello stato del catalogo

È possibile usare Gestione cataloghi per ottenere lo stato del catalogo per le applicazioni che desiderano personalizzare la modalità di gestione del catalogo, ad esempio un'applicazione di monitoraggio "Stato catalogo" personalizzata. Tuttavia, Catalog Manager non è in genere necessario per la maggior parte degli scenari di sviluppo correlati alla ricerca. Gli usi comuni sono per un'applicazione di monitoraggio dello stato del catalogo o per un Pannello di controllo di tipo catalogo.

La tabella seguente descrive i metodi di ISearchCatalogManager usati per la gestione dello stato del catalogo.


| Metodo | Descrizione | 
|--------|-------------|
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a> | Ottiene l'URL attualmente indicizzato. Questo metodo sarebbe utile se si tentasse di identificare se l'indicizzatore era "bloccato" su un elemento. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a> | Ottiene il numero di elementi nel catalogo. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a> | Recupera le informazioni seguenti sugli elementi da indicizzare:<ul><li>plIncrementalCount: numero di elementi da indicizzare nel successivo indice incrementale</li><li>plNotificationQueue: numero di elementi nella coda di notifica. Queste informazioni sono utili per un'applicazione di notifica che deve controllare se l'indicizzatore sta ricevendo le notifiche inviate dall'applicazione.</li><li>plHighPriorityQueue: numero di elementi nella coda con priorità alta. Gli elementi in plHighPriorityQueue vengono indicizzati per primi.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a> | Ottiene lo stato del catalogo e restituisce un valore di enumerazione che fornisce lo stato corrente. Di seguito sono riportati i possibili stati del catalogo:<ul><li>Inattivo: non è necessaria alcuna indicizzazione.</li><li>In pausa: l'indicizzazione è sospesa,ad esempio a causa di batteria in esaurimento o utilizzo elevato della CPU.</li><li>Recupero: l'indicizzazione è in esecuzione.</li><li>Ricerca per indicizzazione completa: l'indicizzatore sta eseguendo una ricerca per indicizzazione completa nell'ambito della ricerca per indicizzazione.</li><li>Ricerca per indicizzazione incrementale: l'indicizzatore sta eseguendo una ricerca per indicizzazione incrementale.</li><li>Elaborazione delle notifiche: l'indicizzatore sta elaborando le notifiche.</li><li>Arresto in fase di arresto: l'indicizzatore è in fase di arresto.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a> | Ottiene il nome del catalogo corrente specificato nel <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>metodo ISearchManager::GetCatalog.</strong></a> Attualmente, l'unico catalogo supportato è SystemIndex. | 


## <a name="managing-catalog-properties"></a>Gestione delle proprietà del catalogo

Esistono tre proprietà del catalogo che è possibile gestire con Gestione cataloghi:

- **Distinzione dei segni diacritici.** I segni diacritici sono accenti aggiunti alle lettere per indicare il significato o la pronuncia di una parola. Questa proprietà determina se il catalogo è sensibile ai segni diacritici ed è importante quando l'utente cerca e indicizza il testo in più lingue. Ad esempio, con questa proprietà impostata su **FALSE,** il catalogo considererebbe "resume" e "resumé" come se fossero la stessa parola.
- **Timeout della connessione.** Questa proprietà rappresenta la quantità di tempo di attesa per una risposta di connessione da un server o da un archivio dati, come rappresentato in una [**struttura TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) È possibile usare questa proprietà per ottimizzare Windows ricerca.
- **Timeout dei dati** Questa proprietà rappresenta la quantità di tempo di attesa per una transazione di dati tra l'indicizzatore e un gestore di protocollo o un filtro, come rappresentato in una [**struttura TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) Se questo tempo è trascorso, il processo dal daemon di filtri viene terminato per evitare deadlock e altri problemi di risorse.

Le ultime due proprietà sono destinate principalmente a un uso futuro. Ognuna di queste proprietà include `get` i metodi `put` e .

| Metodo                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE se il catalogo deve distinguere le parole con segni diacritici. **FALSE** se il catalogo deve ignorare i segni diacritici. La modifica di questa proprietà richiede la ricompilazione dell'indice perché le chiavi dell'indice potrebbero non essere più valide.                       |
| [**get \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**put \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Tempo di attesa, in secondi, dell'indicizzatore per una risposta di connessione da un server o da un archivio dati. L'impostazione di un valore troppo alto può causare ritardi se molti siti non rispondono. L'impostazione di un valore troppo basso può causare la ricerca per indicizzazione di alcuni siti. |
| [**get \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Tempo, in secondi, di attesa da parte dell'indicizzatore per una transazione di dati.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Esecuzione in modalità con privilegi elevati

Qualsiasi chiamata al metodo che aggiorna SystemIndex richiede che l'applicazione sia eseguita con privilegi elevati. In caso contrario, l'applicazione avrà esito negativo con un errore di accesso negato.

## <a name="related-topics"></a>Argomenti correlati


[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Interfacce per la gestione dell'indice](interfaces-for-managing-the-index.md)

[Uso di Gestione ricerca](-search-3x-wds-mngidx-searchmanager.md)

[Uso del Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
