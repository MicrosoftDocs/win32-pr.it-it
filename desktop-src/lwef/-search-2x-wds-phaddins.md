---
title: Sviluppo di componenti aggiuntivi per gestori di protocollo
description: È possibile estendere Microsoft Windows Desktop Search (WDS) per includere nuovi archivi dati implementando un gestore di protocollo personalizzato.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726501"
---
# <a name="developing-protocol-handler-add-ins"></a>Sviluppo di componenti aggiuntivi per gestori di protocollo

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

È possibile estendere Microsoft Windows Desktop Search (WDS) per includere nuovi archivi dati implementando un gestore di protocollo personalizzato.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indicizzazione di archivi dati con gestori di protocollo

Un archivio dati è un'origine del contenuto (un sistema di database, una directory, un file system) in cui i dati vengono archiviati e possono essere sottoposti a ricerca per indicizzazione dall'indicizzatore wds. L'archivio può essere gerarchico (ad esempio un database) o basato su collegamento (ad esempio un sito Web). Un gestore di protocollo consente alle applicazioni di indicizzazione come WDS di eseguire sistematicamente una ricerca per indicizzazione nei nodi di un archivio dati per estrarre le informazioni rilevanti da includere nell'indice. Ogni gestore di protocollo viene usato per indicizzare un tipo specifico di archivio dati. WDS viene fornito con gestori di protocollo per file system e per gli archivi dati di Microsoft Outlook e Microsoft Outlook Express (archivi di posta elettronica, . file PST e così via). Quando si indicizza Outlook posta elettronica, ad esempio, il gestore del protocollo esegue una ricerca per indicizzazione in tutti i messaggi in tutte le cartelle estraendo informazioni da ogni messaggio e allegato. Queste informazioni vengono passate all'indicizzatore da includere nel catalogo di Servizi di distribuzione Windows.

Spesso gli utenti devono eseguire ricerche in altri archivi dati, ad esempio database legacy, archivi di posta elettronica o strutture di dati non supportate da Servizi di distribuzione Windows. È possibile estendere Servizi di distribuzione Windows per eseguire ricerche per indicizzazione in un nuovo archivio dati usando o implementando un gestore di protocollo specifico per tale archivio dati. Prima di tutto, è necessario determinare se esiste già un gestore di protocollo per l'archivio dati, ad esempio per l'uso con un'altra applicazione come SharePoint Services. In tal caso, è possibile installare il gestore di protocollo nel sistema. Se, tuttavia, non esiste un altro gestore di protocollo, è necessario implementare un gestore. I gestori di protocollo WDS usano le stesse specifiche di progettazione SharePoint Services e spesso possono essere usati in modo intercambiabile.

Inoltre, se l'archivio dati contiene dati o tipi di file diversi da uno dei 200 tipi di file supportati da WDS, è necessario implementare anche un filtro per accedere e indicizzare il contenuto degli elementi nell'archivio. WDS 2.x usa il gestore di protocollo e la [**tecnologia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)usati da SharePoint Services. Se nel sistema da indicizzare sono già installati filtri per un archivio e un tipo di file specifici, WDS usa le interfacce esistenti per indicizzare questi dati.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Roadmap to Adding New Data Stores

Per estendere Servizi di distribuzione Windows per la ricerca per indicizzazione in nuovi archivi dati, è possibile creare un gestore di protocollo e uno o più dei componenti aggiuntivi seguenti: gestore del menu di scelta rapida, gestore dell'icona e componente aggiuntivo SearchProtocolOptions.

1.  Creare e registrare un gestore di protocollo multithreading per l'archivio dati:
    -   **ISearchProtocol:** questa interfaccia accede a un protocollo ed esegue il mapping di un URL a un oggetto IUrlAccessor.
    -   **IUrlAccessor:** interfaccia principale usata per accedere agli elementi dall'origine del contenuto e associare il contenuto al filtro appropriato.
    -   **IProtocolHandlerSite:** questa interfaccia viene usata per richiedere e caricare filtri aggiuntivi.
    -   **IFilter:** questa interfaccia restituisce l'URL di ogni elemento in una cartella come proprietà di valore per l'elaborazione.

    > [!Note]
    >
    > La funzionalità minima del componente aggiuntivo necessaria per restituire i risultati della ricerca da un archivio dati non gerarchico è un'implementazione delle interfacce ISearchProtocol e IUrlAccessor.

     

2.  Implementare l'interfaccia ISearchProtocolOptions per includere opzioni del gestore di protocollo personalizzate, ad esempio le pagine iniziale predefinite:
    -   **ISearchProtocolOptions:** questa interfaccia definisce gli URL predefiniti che il gestore di protocollo deve elaborare, determina quali sono i requisiti per un gestore di protocollo e determina se i requisiti sono stati soddisfatti in un determinato sistema.
3.  Estendere shell per includere elementi dell'interfaccia utente, ad esempio menu di scelta rapida e icone specifiche del file, implementando le interfacce seguenti:
    -   **IShellFolder:** questa interfaccia, usata per gestire le cartelle, è necessaria per fornire le interfacce IContextMenu e IExtractIcon per un URL in un nuovo archivio.
    -   **IPersistFolder:** questa interfaccia è necessaria per indicare a un oggetto cartella shell di inizializzarsi.
    -   **IPersist:** questa interfaccia fornisce l'identificatore di classe (CLSID) di un oggetto che può essere archiviato in modo permanente nel sistema.
    -   **IContextMenu:** questa interfaccia definisce il menu di scelta rapida per un elemento a cui punta l'URL.
    -   **IExtractIcon:** questa interfaccia definisce l'icona da visualizzare per un elemento a cui punta l'URL.
4.  Implementare un meccanismo per notificare all'indicizzatore le modifiche apportate all'archivio dati:
    -   **ISearchItemsChangedSink:** questa interfaccia consente al gestore del protocollo di notificare all'indice le modifiche apportate all'archivio dati. In questo modo si migliorano le prestazioni assicurandosi che l'indicizzatore non eserciti ricerche per indicizzazione nell'intero archivio sugli indici incrementali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Implementazione di un gestore di protocollo per WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Aggiunta di icone, anteprime e menu di scelta rapida con le estensioni della shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notifica delle modifiche all'indice](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 