---
title: Informazioni sugli archivi online di tipo 1
description: Informazioni sugli archivi online di tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online Stores, digitare 1 Store online
- negozi online, digitare 1 negozi online
- digitare 1 Store online, informazioni
- Windows Media Player, digitare 1 negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299428"
---
# <a name="about-type-1-online-stores"></a>Informazioni sugli archivi online di tipo 1

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Microsoft Windows Media Player 11 supporta due tipi di negozi online: tipo 1 e tipo 2. Gli archivi di tipo 1 sono più profondamente integrati in Windows Media Player rispetto ai negozi di tipo 2. Un archivio online di tipo 1 fornisce un catalogo musicale scaricabile, in modo che Windows Media Player possa rendere disponibile il contenuto del negozio all'utente come se il contenuto si trovasse nel Catalogo multimediale locale dell'utente.

Un archivio online di tipo 1 deve fornire un plug-in che implementi l'interfaccia [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Quando l'utente naviga nell'interfaccia utente di Windows Media Player, il lettore chiama il plug-in in modo che lo Store online possa migliorare l'esperienza dell'utente fornendo pagine Web visualizzate nel lettore.

Di seguito sono riportate le funzionalità dei negozi in linea di tipo 1 che li distinguono da quelli di tipo 2:

-   **Semplicità d'uso.** Gli utenti possono cercare musica dal catalogo online Store usando la stessa interfaccia utente Windows Media Player familiare che attualmente usano per gestire la propria libreria personale. Gli utenti possono visualizzare solo un singolo catalogo di Store online nella funzionalità di ricerca in un determinato momento.
-   **Convenienza.** Gli utenti possono campionare o acquistare musica senza passare dalla funzionalità di esplorazione a un'altra parte dell'interfaccia utente di Windows Media Player.
-   **Funzionalità avanzate.** Poiché il catalogo dei negozi online viene archiviato in modo analogo alla libreria dell'utente, molte delle funzionalità della libreria Media Player di Windows possono essere applicate al catalogo. Ad esempio, gli utenti possono utilizzare la rotellina della funzionalità Sfoglia per filtrare il catalogo del negozio online.

Per un provider di negozio online, i vantaggi derivanti dalla fornitura di un archivio di tipo 1 anziché di un archivio di tipo 2 includono i seguenti:

-   Nodo personalizzato a visibilità elevata nell'albero della libreria Media Player di Windows.
-   Sistema progettato per gli acquisti di musica.
-   Connessioni migliorate ai processi dei giocatori.
-   Gestione download migliore e più facile da utilizzare.
-   Possibilità di spostarsi tra le varie funzionalità del lettore, inclusa l'apertura di nodi dell'albero della libreria specifici.
-   Notifiche relative alla scadenza delle licenze per il contenuto della sottoscrizione.
-   Notifiche per l'uso di lettori musicali portatili connessi.

Nelle sezioni seguenti vengono fornite informazioni generali sugli archivi online di tipo 1.



| Sezione                                                                                              | Descrizione                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Catalogo musica](music-catalog.md)                                                                   | Descrive il catalogo musicale fornito dallo Store online. Viene descritto il compilatore del catalogo fornito da Microsoft.                                                                     |
| [Contenitori di contenuto](content-containers.md)                                                         | Viene descritta l'interfaccia del contenitore di contenuti ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), che viene utilizzata per rappresentare una raccolta di elementi multimediali da acquistare o scaricare. |
| [Integrazione della libreria](library-integration.md)                                                       | Descrive il modo in cui il catalogo musicale del negozio online è integrato nella visualizzazione libreria del lettore.                                                                                        |
| [Pagine di individuazione](discovery-pages.md)                                                               | Viene descritta l'interazione tra Media Player Windows e le pagine Web fornite dal negozio online.                                                                                   |
| [Menu di scelta rapida](context-menus.md)                                                                   | Viene descritto in che modo l'archivio online può fornire menu di scelta rapida quando l'utente naviga nell'interfaccia utente del lettore.                                                                         |
| [Flussi audio](audio-streams.md)                                                                   | Viene descritto in che modo l'archivio online fornisce Windows Media Player con l'URL per lo streaming di contenuto audio.                                                                              |
| [Documento ServiceInfo per un negozio online di tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Viene descritto il documento XML ServiceInfo fornito da un archivio online di tipo 1.                                                                                                           |
| [Digitare 1 plug-in di archivio online](type-1-online-store-plug-in.md)                                       | Descrive il plug-in che deve essere fornito da un archivio online di tipo 1.                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Digitare 1 negozi online**](type-1-online-stores.md)
</dt> </dl>

 

 




