---
title: Informazioni sui negozi online di tipo 1
description: Informazioni sui negozi online di tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player online, digitare 1 store online
- online stores,type 1 online stores
- type 1 online stores,about
- Windows Media Player, digitare 1 negozio online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bc84311bb61c71fdcaf57b584b5c595a62be5c80d406f71ef36c8d1ad8e655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903061"
---
# <a name="about-type-1-online-stores"></a>Informazioni sui negozi online di tipo 1

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

Microsoft Windows Media Player 11 supporta due tipi di negozi online: tipo 1 e tipo 2. I negozi di tipo 1 sono più integrati in Windows Media Player rispetto agli archivi di tipo 2. Uno store online di tipo 1 fornisce un catalogo musicale scaricabile in modo che Windows Media Player possa rendere disponibile il contenuto dello Store all'utente come se il contenuto fosse presente nel catalogo multimediale locale dell'utente.

Uno store online di tipo 1 deve fornire un plug-in che implementa [l'interfaccia IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Quando l'utente si sposta nell'interfaccia utente di Windows Media Player, il lettore chiama il plug-in in modo che lo store online possa migliorare l'esperienza dell'utente fornendo pagine Web visualizzate nel lettore.

Di seguito sono riportate le funzionalità dei negozi online di tipo 1 che li distinguono dai negozi di tipo 2:

-   **Facilità d'uso.** Gli utenti possono cercare musica dal catalogo dei negozi online usando la stessa interfaccia utente familiare Windows Media Player che attualmente usano per gestire la libreria personale. Gli utenti possono visualizzare un solo catalogo di negozi online nella funzionalità Sfoglia in un determinato momento.
-   **Comodità.** Gli utenti possono campionare o acquistare musica senza passare dalla funzionalità Sfoglia a un'altra parte Windows Media Player'interfaccia utente.
-   **Funzionalità avanzate.** Poiché il catalogo dei negozi online è archiviato in modo simile alla libreria dell'utente, molte delle funzionalità della libreria Windows Media Player possono essere applicate al catalogo. Ad esempio, gli utenti possono usare la rotellina della funzionalità Sfoglia per filtrare il catalogo dei negozi online.

Per un provider di negozi online, i vantaggi della fornitura di uno store di tipo 1 anziché di uno di tipo 2 includono i seguenti:

-   Nodo personalizzato altamente visibile nell'Windows Media Player della libreria.
-   Un sistema progettato per gli acquisti di musica.
-   Connessioni migliorate ai processi del lettore.
-   Un download manager migliore e più facile da usare.
-   Possibilità di spostarsi tra le varie funzionalità del lettore (inclusa l'apertura di nodi specifici dell'albero della libreria).
-   Notifiche sulla scadenza della licenza per il contenuto della sottoscrizione.
-   Notifiche per l'uso di lettori musicali portatili connessi.

Le sezioni seguenti forniscono informazioni generali sui negozi online di tipo 1.



| Sezione                                                                                              | Descrizione                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Musica Catalogo](music-catalog.md)                                                                   | Descrive il catalogo musicale fornito dallo store online. Descrive il compilatore del catalogo fornito da Microsoft.                                                                     |
| [Contenitori di contenuto](content-containers.md)                                                         | Descrive l'interfaccia del contenitore di contenuti ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), usata per rappresentare una raccolta di elementi multimediali da acquistare o scaricare. |
| [Integrazione di librerie](library-integration.md)                                                       | Descrive come il catalogo musicale dello store online è integrato nella visualizzazione libreria del lettore.                                                                                        |
| [Pagine di individuazione](discovery-pages.md)                                                               | Descrive l'interazione tra Windows Media Player e le pagine Web fornite dallo store online.                                                                                   |
| [Menu di scelta rapida](context-menus.md)                                                                   | Descrive in che modo lo store online può fornire menu di scelta rapida mentre l'utente passa all'interfaccia utente del lettore.                                                                         |
| [Audio Flussi](audio-streams.md)                                                                   | Descrive in che modo lo store online fornisce Windows Media Player con l'URL per lo streaming di contenuto audio.                                                                              |
| [Documento ServiceInfo per uno Store online di tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Descrive il documento XML ServiceInfo fornito da un negozio online di tipo 1.                                                                                                           |
| [Plug-in del negozio online di tipo 1](type-1-online-store-plug-in.md)                                       | Descrive il plug-in che deve essere fornito da uno store online di tipo 1.                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Tipo 1 Punti vendita online**](type-1-online-stores.md)
</dt> </dl>

 

 




