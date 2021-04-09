---
description: Usando i componenti delle API di notifica è possibile notificare all'indicizzatore che un elemento è stato modificato, spostato o eliminato e può aggiungere ambiti di ricerca alla coda degli URL dell'indicizzatore di ricerca di Windows che richiedono l'indicizzazione.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Notifica dell'indice delle modifiche (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a89112da20c4010e1fc23fab16778309195d20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128602"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Notifica dell'indice delle modifiche (Windows Search)

Usando i componenti delle API di notifica è possibile notificare all'indicizzatore che un elemento è stato modificato, spostato o eliminato e può aggiungere ambiti di ricerca alla coda degli URL dell'indicizzatore di ricerca di Windows che richiedono l'indicizzazione.

I componenti possono notificare all'indicizzatore di Windows Search che i dati nel relativo archivio sono stati modificati. In genere, è possibile basarsi sulle ricerche per indicizzazione pianificate dell'indicizzatore. Tuttavia, fornire notifiche all'indicizzatore può migliorare le prestazioni assicurando che l'indicizzatore non indicizzazione dell'intero archivio negli indici incrementali. Ad esempio, questa opzione potrebbe essere consigliata se si prevede che l'archivio dati sia eccezionalmente grande e/o particolarmente occupato, ad esempio un archivio dati di posta elettronica.

-   [Implementazione di notifiche gestite da indicizzatore](#implementing-indexer-managed-notifications)
    -   [Coda notifiche](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementazione di notifiche gestite dal provider](#implementing-provider-managed-notifications)
    -   [Coda notifiche](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementazione di notifiche gestite da indicizzatore

Le notifiche gestite dall'indicizzatore consentono di controllare l'accesso all'archivio dati, evitando in tal modo di mantenere la coda delle notifiche durante l'intero processo di indicizzazione. Il provider di notifiche deve monitorare le modifiche apportate all'archivio dati e creare una coda di notifiche. Periodicamente, il provider invia un batch di notifiche di modifica all'indicizzatore. Quando l'indicizzatore riceve le notifiche, restituisce un riconoscimento ed è possibile rimuovere gli elementi dalla coda. Se dopo un periodo di tempo non si riceve un riconoscimento, è possibile inviare nuovamente le notifiche. In caso di errore, l'indicizzatore ricompila la coda interna degli elementi per eseguire la ricerca per indicizzazione o esegue una ricerca per indicizzazione incrementale dell'archivio.

Per implementare le notifiche gestite dall'indicizzatore, è necessario implementare quanto segue:

-   Meccanismo per il monitoraggio delle modifiche nell'archivio dati.
-   Una struttura di dati per accodare le informazioni (più strutture di [**\_ \_ \_ modifica persistenti degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ) relative a tali modifiche.
-   Interfaccia [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) per inviare le notifiche all'indicizzatore e per ricevere i riconoscimenti delle notifiche dall'indicizzatore.

### <a name="notifications-queue"></a>Coda notifiche

È necessario monitorare e accodare ogni modifica nell'archivio dati da inviare all'indicizzatore come notifica. Il numero di notifiche accodate e la frequenza con cui vengono inviate all'indicizzatore dipendono dalla circostanza. Probabilmente si invia un batch di notifiche per ogni *n* numero di modifiche o dopo un intervallo di tempo *t* o una combinazione dei due.

L'indicizzatore prevede che le notifiche vengano inserite in una matrice di strutture di [**\_ \_ \_ modifica permanenti degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) , pertanto è possibile scegliere di implementare la coda in modo analogo.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Per accedere a questa interfaccia, è innanzitutto necessario creare un'istanza di un oggetto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) per ottenere l'accesso a un oggetto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Da tale oggetto **ISearchCatalogManager** , si crea un'istanza di un oggetto [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) e si notifica all'indicizzatore le modifiche ai dati con una chiamata al metodo **OnItemsChanged** .

Nella chiamata a questo metodo si include il numero di modifiche segnalate e una matrice di strutture di [**\_ \_ \_ modifica permanenti degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) . Viene restituito un array di codici di completamento HR che indica se ogni URL è stato accettato per l'indicizzazione. Questo è il riconoscimento dell'indicizzatore.

## <a name="implementing-provider-managed-notifications"></a>Implementazione di notifiche gestite dal provider

Le notifiche gestite dal provider consentono di controllare l'accesso all'archivio dati e di monitorare lo stato di avanzamento dell'indicizzatore durante l'aggiornamento del catalogo di Windows Search. Il provider deve monitorare le modifiche apportate all'archivio dati e creare una coda di notifiche. Periodicamente, il provider invia un batch di notifiche di modifica all'indicizzatore. Quando l'indicizzatore riceve le notifiche, restituisce un riconoscimento. Se dopo un periodo di tempo non si riceve un riconoscimento, è possibile inviare nuovamente le notifiche. Quando l'indicizzatore esegue la ricerca per indicizzazione nell'archivio dati e aggiorna il catalogo di Windows Search, invia una notifica al provider di ogni aggiornamento del catalogo ed è possibile rimuovere gli elementi dalla coda. Il provider mantiene la coda delle notifiche durante questo processo in modo che, in caso di errore, sia possibile inviare di nuovo le notifiche all'indicizzatore.

Per implementare le notifiche gestite dal provider, è necessario implementare quanto segue:

-   Meccanismo per il monitoraggio delle modifiche nell'archivio dati.
-   Una struttura di dati per accodare le informazioni (più strutture di [**\_ \_ modifica degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ) relative a tali modifiche.
-   Interfaccia [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) per inviare le notifiche all'indicizzatore e per ricevere i riconoscimenti delle notifiche dall'indicizzatore.
-   Interfaccia [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) per la ricezione di aggiornamenti sullo stato dell'indicizzazione.

### <a name="notifications-queue"></a>Coda notifiche

È necessario monitorare e accodare ogni modifica nell'archivio dati da inviare all'indicizzatore come notifica. Il numero di notifiche accodate e la frequenza con cui vengono inviate all'indicizzatore dipendono dalla circostanza. Probabilmente si invia un batch di notifiche per ogni *n* numero di modifiche o dopo un intervallo di tempo *t* o una combinazione dei due.

L'indicizzatore prevede che le notifiche vengano fornite in una matrice di strutture di [**\_ \_ modifica degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) , pertanto è possibile scegliere di archiviare le informazioni sulle modifiche in modo analogo. Tuttavia, è anche necessario essere in grado di associare le notifiche inviate con i riconoscimenti e gli aggiornamenti restituiti dall'indicizzatore. Potrebbe inoltre essere necessario essere in grado di rilevare il tempo necessario per ottenere i riconoscimenti, in modo da poter decidere se/quando inviare nuovamente le notifiche.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Per accedere a questa interfaccia, è innanzitutto necessario creare un'istanza di un oggetto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) per ottenere l'accesso a un oggetto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Da tale oggetto **ISearchCatalogManager** , si crea un'istanza di un oggetto [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) e si notifica all'indicizzatore le modifiche ai dati con una chiamata al metodo **OnItemsChanged** .

Nella chiamata a questo metodo si include il numero di modifiche segnalate e una matrice di strutture di [**\_ \_ modifica degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) . Viene restituita una matrice di DocIds assegnati dall'indicizzatore che rappresentano ogni modifica, oltre a una matrice di codici di completamento delle risorse umane che indica se ogni URL è stato accettato per l'indicizzazione. Questo è il riconoscimento dell'indicizzatore che ha ricevuto le notifiche e si sta preparando a indicizzare gli elementi.

Da quel punto in poi, l'indicizzatore invia gli aggiornamenti usando l'interfaccia [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) .

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Per ottenere gli aggiornamenti sullo stato degli elementi e del catalogo, è necessario registrare l'interfaccia [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) con l'indicizzatore per poter inviare i callback. Ogni aggiornamento inviato tramite [**ISearchNotifyInlineSite:: OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifica gli elementi in base a DocId, lo stato di ogni elemento ([**\_ \_ \_ stato di indicizzazione degli elementi di ricerca**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) e la fase di indicizzazione ([**\_ \_ fase**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)di indicizzazione di ricerca) in cui si trovano gli elementi.

Non solo si ricevono aggiornamenti sullo stato di ogni elemento, come descritto in precedenza, si ottengono anche informazioni importanti sullo stato del catalogo stesso. Il servizio Windows Search può essere interrotto o riavviato dall'utente finale, da un'applicazione di terze parti o da un altro errore. Quando si verifica questo problema, è necessario un modo per determinare quali notifiche inviare nuovamente all'indicizzatore.

Il metodo [**ISearchNotifyInlineSite:: OnCatalogStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) , chiamato dal servizio di ricerca di Windows, informa i client sullo stato del catalogo usando i parametri descritti nella tabella seguente.



| Parametro                 | Descrizione                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | GUID che rappresenta la reimpostazione del catalogo. Se questo GUID viene modificato, tutte le notifiche devono essere inviate nuovamente.                                                        |
| guidCheckPointSignature   | GUID che rappresenta l'ultimo checkpoint ripristinato. Se questo GUID viene modificato, tutte le notifiche accumulate dall'ultimo checkpoint salvato devono essere inviate nuovamente. |
| dwLastCheckPointNumber    | Numero che indica l'ultimo checkpoint salvato.                                                                                                        |



 

 

Quando si verifica un checkpoint del catalogo, il servizio di ricerca aggiorna il *dwLastCheckPointNumber* e tutte le notifiche inviate prima del checkpoint sono sicure e ripristinabili in caso di errore del servizio. I provider di notifiche devono tenere traccia solo delle notifiche inviate tra i checkpoint e il push in caso di ripristino o reimpostazione del catalogo.

Se si verifica un ripristino del catalogo, il servizio di ricerca esegue il rollback del catalogo all'ultimo checkpoint salvato e aggiorna *guidCheckPointSignature*. In questa situazione, i provider di notifiche devono respingere tutte le notifiche accumulate dal checkpoint salvato più recente come identificato da *dwLastCheckPointNumber*.

Se deve essere eseguita la reimpostazione di un catalogo, il servizio di ricerca Reimposta l'intero catalogo e aggiorna *guidCatalogResetSignature*. Il provider di notifiche deve eseguire di nuovo il push dell'intero ambito di ricerca.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
-   Per panoramiche su Catalog Manager e Catalog Search Manager (CSM), vedere [using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [using the Crawl scope Manager](-search-3x-wds-extidx-csm.md).
-   Per informazioni sulla creazione di un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

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

[Esempio di codice: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
