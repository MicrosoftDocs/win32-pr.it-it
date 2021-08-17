---
description: Usando le API di notifica, i componenti possono notificare all'indicizzatore che un elemento è stato modificato, spostato o eliminato e possono aggiungere ambiti di ricerca alla coda di URL dell'indicizzatore di ricerca di Windows che richiedono l'indicizzazione.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Notifica all'indice delle modifiche (Windows ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb386763be5192851368b1f46b69f94576fbe261a57d215d649d38ac5a19ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052228"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Notifica all'indice delle modifiche (Windows ricerca)

Usando le API di notifica, i componenti possono notificare all'indicizzatore che un elemento è stato modificato, spostato o eliminato e possono aggiungere ambiti di ricerca alla coda di URL dell'indicizzatore di ricerca di Windows che richiedono l'indicizzazione.

I componenti possono notificare all Windows indicizzatore di ricerca che i dati nell'archivio sono stati modificati. In genere, è possibile basarsi sulle ricerche per indicizzazione pianificate dell'indicizzatore. Tuttavia, l'invio di notifiche all'indicizzatore può migliorare le prestazioni assicurandosi che l'indicizzatore non eserciti ricerche per indicizzazione nell'intero archivio sugli indici incrementali. Ad esempio, questa scelta può essere consigliata se si prevede che l'archivio dati sia estremamente grande e/o estremamente occupato, ad esempio un archivio dati di posta elettronica.

-   [Implementazione di notifiche gestite dall'indicizzatore](#implementing-indexer-managed-notifications)
    -   [Coda notifiche](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementazione di notifiche gestite dal provider](#implementing-provider-managed-notifications)
    -   [Coda notifiche](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementazione di notifiche gestite dall'indicizzatore

Le notifiche gestite dall'indicizzatore consentono di controllare l'accesso all'archivio dati, liberando al tempo stesso la gestione della coda di notifiche durante l'intero processo di indicizzazione. Il provider di notifiche deve monitorare le modifiche apportate all'archivio dati e creare una coda di notifiche. Periodicamente, il provider invia un batch di notifiche di modifica all'indicizzatore. Quando l'indicizzatore riceve le notifiche, restituisce un acknowledgement ed è possibile rimuovere gli elementi dalla coda. Se dopo un periodo di tempo non si riceve un acknowledgement, è possibile inviare nuovamente le notifiche. In caso di errore, l'indicizzatore ricompila la coda interna di elementi per la ricerca per indicizzazione o esegue una ricerca per indicizzazione incrementale dell'archivio.

Per implementare le notifiche gestite dall'indicizzatore, è necessario implementare quanto segue:

-   Meccanismo per il monitoraggio delle modifiche nell'archivio dati.
-   Struttura di dati per accodare le informazioni (più [**strutture SEARCH ITEM PERSISTENT \_ \_ \_ CHANGE)**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) su tali modifiche.
-   [**Interfaccia ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) per inviare le notifiche all'indicizzatore e ottenere gli acknowledgement di notifica dall'indicizzatore.

### <a name="notifications-queue"></a>Coda notifiche

È necessario monitorare e accodare ogni modifica nell'archivio dati da inviare all'indicizzatore come notifica. Il numero di notifiche accodato e la frequenza con cui vengono inviate all'indicizzatore dipendono dalla circostanza. È possibile inviare un batch di notifiche per ogni *n* numero di modifiche o dopo un *intervallo di tempo t* o una combinazione delle due.

L'indicizzatore prevede che le notifiche si presentino in una matrice di strutture [**SEARCH \_ ITEM PERSISTENT \_ \_ CHANGE,**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) pertanto è possibile scegliere di implementare la coda in modo analogo.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Per accedere a questa interfaccia, creare prima un'istanza di un [**oggetto ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) per ottenere l'accesso a [**un oggetto ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Da tale **oggetto ISearchCatalogManager** si crea un'istanza di un oggetto [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) e si notifica all'indicizzatore le modifiche ai dati con una chiamata al metodo **OnItemsChanged.**

Nella chiamata a questo metodo si include il numero di modifiche segnalate e una matrice di strutture [**SEARCH \_ ITEM PERSISTENT \_ \_ CHANGE.**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) Viene restituita una matrice di codici di completamento hr che indica se ogni URL è stato accettato per l'indicizzazione. Si tratta dell'acknowledgement dell'indicizzatore.

## <a name="implementing-provider-managed-notifications"></a>Implementazione di notifiche gestite dal provider

Le notifiche gestite dal provider consentono di controllare l'accesso all'archivio dati e di monitorare lo stato di avanzamento dell'indicizzatore durante l'aggiornamento Windows catalogo di ricerca. Il provider deve monitorare le modifiche apportate all'archivio dati e creare una coda di notifiche. Periodicamente, il provider invia un batch di notifiche di modifica all'indicizzatore. Quando l'indicizzatore riceve le notifiche, restituisce un acknowledgement. Se dopo un periodo di tempo non si riceve un acknowledgement, è possibile inviare nuovamente le notifiche. Quando l'indicizzatore esegue una ricerca per indicizzazione nell'archivio dati e aggiorna il catalogo di ricerca Windows, notifica al provider ogni aggiornamento del catalogo ed è possibile rimuovere gli elementi dalla coda. Il provider mantiene la coda delle notifiche durante tutto il processo in modo che, in caso di errore, sia possibile inviare di nuovo le notifiche all'indicizzatore.

Per implementare le notifiche gestite dal provider, è necessario implementare quanto segue:

-   Meccanismo per il monitoraggio delle modifiche nell'archivio dati.
-   Struttura di dati per accodare le informazioni (più [**strutture SEARCH \_ ITEM \_ CHANGE)**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) su tali modifiche.
-   [**Interfaccia ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) per inviare le notifiche all'indicizzatore e ottenere gli acknowledgement di notifica dall'indicizzatore.
-   [**Interfaccia ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) per ricevere aggiornamenti sullo stato dell'indicizzazione.

### <a name="notifications-queue"></a>Coda notifiche

È necessario monitorare e accodare ogni modifica nell'archivio dati da inviare all'indicizzatore come notifica. Il numero di notifiche accodato e la frequenza con cui vengono inviate all'indicizzatore dipendono dalla circostanza. È possibile inviare un batch di notifiche per ogni *n* numero di modifiche o dopo un *intervallo di tempo t* o una combinazione delle due.

L'indicizzatore prevede che le notifiche si presentino in una matrice di strutture [**SEARCH \_ ITEM \_ CHANGE,**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) pertanto è possibile scegliere di archiviare le informazioni sulle modifiche in modo analogo. Tuttavia, è anche necessario essere in grado di associare le notifiche inviate con gli acknowledgement e gli aggiornamenti restituiti dall'indicizzatore. È anche possibile rilevare il tempo necessario per ottenere i riconoscimenti, in modo da decidere se/quando inviare di nuovo le notifiche.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Per accedere a questa interfaccia, creare prima un'istanza di un [**oggetto ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) per ottenere l'accesso a [**un oggetto ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Da tale **oggetto ISearchCatalogManager,** si crea un'istanza di un oggetto [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) e si notifica all'indicizzatore le modifiche dei dati con una chiamata al metodo **OnItemsChanged.**

Nella chiamata a questo metodo si include il numero di modifiche segnalate e una matrice di [**strutture SEARCH \_ ITEM \_ CHANGE.**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) Si ottiene una matrice di DocId assegnati dall'indicizzatore che rappresentano ogni modifica, nonché una matrice di codici di completamento hr che indica se ogni URL è stato accettato per l'indicizzazione. Si tratta dell'acknowledgement ricevuto dall'indicizzatore che ha ricevuto le notifiche e si sta preparando per indicizzare gli elementi.

Da quel momento in poi l'indicizzatore invia gli aggiornamenti [**usando l'interfaccia ISearchNotifyInlineSite.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite)

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Per ottenere aggiornamenti sullo stato degli elementi e del catalogo, è necessario registrare l'interfaccia [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) con l'indicizzatore in modo che possa inviare callback. Ogni aggiornamento inviato tramite [**ISearchNotifyInlineSite::OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifica gli elementi in base a DocId, allo stato di ogni elemento ([**SEARCH ITEM \_ \_ INDEXING \_ STATUS**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) e alla fase di indicizzazione [**(SEARCH \_ INDEXING \_ PHASE)**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)in cui si verificano gli elementi.

Non solo si ricevono aggiornamenti sullo stato di ogni elemento, come descritto in precedenza, ma si ottengono anche informazioni importanti sullo stato del catalogo stesso. Il Windows servizio di ricerca può essere interrotto o riavviato dall'utente finale, da un'applicazione di terze parti o da un altro errore. In questo caso, è necessario un modo per determinare quali notifiche inviare all'indicizzatore.

Il [**metodo ISearchNotifyInlineSite::OnCatalogStatusChange,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) chiamato dal Windows servizio di ricerca, informa i client sullo stato del catalogo usando i parametri descritti nella tabella seguente.



| Parametro                 | Descrizione                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | GUID che rappresenta la reimpostazione del catalogo. Se questo GUID cambia, tutte le notifiche devono essere inviate nuovamente.                                                        |
| guidCheckPointSignature   | GUID che rappresenta l'ultimo checkpoint ripristinato. Se questo GUID cambia, tutte le notifiche accumulate dopo l'ultimo checkpoint salvato devono essere inviate nuovamente. |
| dwLastCheckPointNumber    | Numero che indica l'ultimo checkpoint salvato.                                                                                                        |



 

 

Quando si verifica un checkpoint del catalogo, il servizio di ricerca aggiorna *dwLastCheckPointNumber* e tutte le notifiche inviate prima di tale checkpoint sono sicure e recuperabili in caso di errore del servizio. I provider di notifiche devono tenere traccia solo delle notifiche inviate tra checkpoint e riposizioni in caso di ripristino o reimpostazione del catalogo.

Se si verifica un ripristino del catalogo, il servizio di ricerca esegue il rollback del catalogo all'ultimo checkpoint salvato e aggiorna *guidCheckPointSignature*. In questo caso, i provider di notifiche devono riposizionare tutte le notifiche accumulate dopo il checkpoint salvato più recente, come identificato da *dwLastCheckPointNumber*.

Se deve essere eseguita una reimpostazione del catalogo, il servizio di ricerca reimposta l'intero catalogo e aggiorna *guidCatalogResetSignature*. Il provider di notifiche deve riposizionire l'intero ambito della ricerca per indicizzazione.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)
-   Per una panoramica di Gestione cataloghi e di Catalog Search Manager (CSM), vedere Using the Catalog Manager (Uso di [Catalog Manager)](-search-3x-wds-mngidx-catalog-manager.md) e [Using the Gestione ambito ricerca per indicizzazione (Uso di Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)).
-   Per informazioni sulla creazione di un archivio dati shell, vedere [Implementazione delle interfacce dell'oggetto cartella di base.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Informazioni sui gestori di protocollo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Aggiunta di icone e menu di scelta rapida](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Esempio di codice: estensioni della shell per gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
