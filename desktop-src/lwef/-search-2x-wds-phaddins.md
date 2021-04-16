---
title: Sviluppo di componenti aggiuntivi per gestori di protocollo
description: È possibile estendere Microsoft Windows Desktop Search (WDS) per includere nuovi archivi dati implementando un gestore di protocollo personalizzato.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a8688621f7d2fda653d769c0e1dfdadd240f49
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516786"
---
# <a name="developing-protocol-handler-add-ins"></a>Sviluppo di componenti aggiuntivi per gestori di protocollo

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile estendere Microsoft Windows Desktop Search (WDS) per includere nuovi archivi dati implementando un gestore di protocollo personalizzato.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indicizzazione di archivi dati con gestori di protocollo

Un archivio dati è un'origine di contenuto (un sistema di database, una directory, un file system) in cui i dati vengono archiviati e possono essere sottoposti a ricerca per indicizzazione nell'indicizzatore di WDS. L'archivio può essere gerarchico (ad esempio un database) o basato sul collegamento (ad esempio un sito Web). Un gestore di protocollo consente alle applicazioni di indicizzazione come WDS di eseguire sistematicamente la ricerca per indicizzazione dei nodi di un archivio dati per estrarre le informazioni rilevanti da includere nell'indice. Ogni gestore di protocollo viene utilizzato per indicizzare un tipo specifico di archivio dati. WDS viene fornito con i gestori di protocollo per gli archivi file system e per gli archivi dati Microsoft Outlook e Microsoft Outlook Express (archivi di posta elettronica,. File PST e così via). Quando si indicizza la posta elettronica di Outlook, ad esempio, il gestore di protocollo esegue la ricerca per indicizzazione di tutti i messaggi in tutte le cartelle estraendo informazioni da ogni messaggio e allegato. Queste informazioni vengono passate all'indicizzatore da includere nel catalogo WDS.

Spesso gli utenti devono cercare altri archivi dati, ad esempio database legacy, archivi di posta elettronica o strutture di dati non supportati da WDS. È possibile estendere WDS per eseguire la ricerca per indicizzazione in un nuovo archivio dati utilizzando o implementando un gestore di protocollo specifico per l'archivio dati. Prima di tutto, è necessario determinare se un gestore di protocollo esiste già per l'archivio dati, ad esempio per l'uso con un'altra applicazione come SharePoint Services. In tal caso, è possibile installare il gestore di protocollo nel sistema. Se, tuttavia, non esiste un altro gestore di protocollo, è necessario implementarne uno. I gestori del protocollo WDS utilizzano le stesse specifiche di progettazione dei servizi di SharePoint e spesso possono essere utilizzati in modo interscambiabile.

Inoltre, se l'archivio dati contiene dati o tipi di file diversi da uno dei tipi di file 200 supportati da WDS, è necessario implementare anche un filtro per accedere e indicizzare il contenuto degli elementi nell'archivio. WDS 2. x utilizza il gestore di protocollo e la tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)utilizzata da SharePoint Services. Se sono già presenti filtri per un archivio specifico e un tipo di file installati nel sistema indicizzato, WDS usa le interfacce esistenti per indicizzare questi dati.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Guida di orientamento per l'aggiunta di nuovi archivi dati

Per estendere WDS alla ricerca per indicizzazione di nuovi archivi dati, è possibile creare un gestore di protocollo e uno o più dei seguenti componenti aggiuntivi: gestore menu di scelta rapida, gestore icone e un componente aggiuntivo SearchProtocolOptions.

1.  Creare e registrare un gestore di protocollo multithreading per l'archivio dati:
    -   **ISearchProtocol** : questa interfaccia accede a un protocollo ed esegue il mapping di un URL a un IUrlAccessor.
    -   **IUrlAccessor** : si tratta dell'interfaccia principale usata per accedere agli elementi dall'origine del contenuto e associare il contenuto al filtro appropriato.
    -   **IProtocolHandlerSite** : questa interfaccia viene usata per richiedere e caricare filtri aggiuntivi.
    -   **IFilter** : questa interfaccia restituisce l'URL di ogni elemento in una cartella come proprietà del valore per l'elaborazione.

    > [!Note]
    >
    > La funzionalità minima dei componenti aggiuntivi necessaria per restituire i risultati della ricerca da un archivio dati non gerarchico è un'implementazione delle interfacce ISearchProtocol e IUrlAccessor.

     

2.  Implementare l'interfaccia ISearchProtocolOptions per includere le opzioni personalizzate del gestore di protocollo, ad esempio le pagine iniziali predefinite:
    -   **ISearchProtocolOptions** : questa interfaccia definisce gli URL predefiniti per il gestore di protocollo da elaborare, determina quali sono i requisiti per un gestore di protocollo e determina se i requisiti sono stati soddisfatti in un determinato sistema.
3.  Estendere Shell per includere gli elementi dell'interfaccia utente, ad esempio i menu di scelta rapida e le icone specifiche del file, implementando le interfacce seguenti:
    -   **IShellFolder** : questa interfaccia, che viene usata per gestire le cartelle, è necessaria per fornire le interfacce IContextMenu e IExtractIcon per un URL in un nuovo archivio.
    -   **IPersistFolder** : questa interfaccia è necessaria per indicare a un oggetto cartella della shell di inizializzarsi automaticamente.
    -   **IPersist** : questa interfaccia fornisce l'identificatore di classe (CLSID) di un oggetto che può essere archiviato in modo permanente nel sistema.
    -   **IContextMenu** : questa interfaccia definisce il menu di scelta rapida per un elemento a cui fa riferimento l'URL.
    -   **IExtractIcon** : questa interfaccia definisce l'icona da visualizzare per un elemento a cui punta l'URL.
4.  Implementare un meccanismo per notificare all'indicizzatore le modifiche apportate all'archivio dati:
    -   **ISearchItemsChangedSink** : questa interfaccia consente al gestore del protocollo di inviare una notifica all'indice delle modifiche apportate all'archivio dati. Ciò consente di migliorare le prestazioni assicurando che l'indicizzatore non esegue la ricerca per indici incrementali nell'intero archivio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Implementazione di un gestore di protocollo per WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Aggiunta di icone, anteprime e menu di scelta rapida con le estensioni della shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notifica dell'indice delle modifiche](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 