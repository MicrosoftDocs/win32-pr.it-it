---
title: Posizione e elemento selezionato
description: Posizione e elemento selezionato
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player negozi online, località
- negozi online, località
- tipo 1 negozi online, località
- Windows Media Player negozi online, posizioni delle librerie
- negozi online, posizioni delle librerie
- tipo 1 negozi online, posizioni delle librerie
- Windows Media Player negozi online,elementi selezionati
- negozi online,elementi selezionati
- tipo 1 negozi online, elementi selezionati
- Windows Media Player, percorsi
- Windows Media Player, elementi selezionati
- libreria,percorsi
- libreria,elementi selezionati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6532c6417b6e95632aa21fa8d4a3a9ed943ad844eb1324f34eb80191043eeb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003380"
---
# <a name="location-and-selected-item"></a>Posizione e elemento selezionato

Windows Media Player usa i cinque elementi seguenti per caratterizzare la visualizzazione corrente del contenuto del negozio online:

-   attività
-   tipo di percorso della libreria
-   ID percorso della libreria
-   tipo di elemento selezionato
-   ID elemento selezionato

In genere, è possibile pensare alla visualizzazione in Windows Media Player come a un contenitore di elementi. Il contenitore ha un tipo e un elemento ha un tipo . Tutti gli elementi in un contenitore hanno lo stesso tipo. I tipi di posizione e i tipi di elemento vengono entrambi specificati dalle costanti [di percorso della libreria](library-location-constants.md). Ad esempio, se la visualizzazione corrente mostra un singolo album, il tipo di percorso della libreria è CPAlbumID e, poiché un album contiene tracce, il tipo di elemento selezionato è CPTrackID.

La tabella seguente illustra la posizione e i tipi di elemento per diversi contenitori.



| Descrizione del contenitore                              | Tipo di percorso della libreria | Tipo di elemento selezionato |
|-------------------------------------------------------|-----------------------|--------------------|
| Un album che è un contenitore di tracce                | CPAlbumID             | CPTrackID          |
| Elenco che è un contenitore di tracce                  | CPListID              | CPTrackID          |
| Elenco che è un contenitore di album                  | CPListID              | CPAlbumID          |
| Una stazione radio che è un contenitore di elenchi          | CPRadioID             | CPListID           |
| Set di tutti gli album, che è un contenitore di album | AllCPAlbumIDs         | CPAlbumID          |
| Set di tutti i generi, che è un contenitore di generi | AllCPGenreIDs         | CPGenreID          |



 

Le schede in Windows Media Player rappresentano attività diverse. Il lettore visualizza il contenuto del negozio online in tre riquadri attività diversi: **Libreria**, **Masterizza** e **Sincronizza**. Il riquadro attività Libreria è denominato anche **riquadro attività** Sfoglia. In alcuni casi, un riquadro attività è denominato *funzionalità*, quindi in questa documentazione potrebbero essere visualizzati termini come la funzionalità *di masterizzazione* e la funzionalità di sincronizzazione. 

Gli esempi seguenti illustrano Windows Media Player le cinque informazioni (attività, tipo di posizione della libreria, ID percorso libreria, tipo di elemento selezionato, ID elemento selezionato) per caratterizzare visualizzazioni diverse.

Nel riquadro **attività Masterizza** il lettore visualizza un album come contenitore di tracce. L'id dell'album è 250. Nella visualizzazione l'elemento selezionato è la traccia con ID 800. Si noti che 800 è l'ID della traccia nel catalogo del negozio online, non il numero della traccia nell'album.



| Elemento                  | valore     |
|-----------------------|-----------|
| attività                  | Bruciare      |
| tipo di percorso della libreria | CPAlbumID |
| ID percorso della libreria   | 250       |
| tipo di elemento selezionato    | CPTrackID |
| ID elemento selezionato      | 800       |



 

Nel riquadro **attività** Sincronizza il lettore visualizza il set di tutti gli album, ovvero un contenitore di album. Nella visualizzazione l'elemento selezionato è l'album con ID 300. Si noti che l'ID percorso della libreria non è applicabile a questa vista.



| Elemento                  | valore         |
|-----------------------|---------------|
| attività                  | Sincronizza          |
| tipo di percorso della libreria | AllCPAlbumIDs |
| ID percorso della libreria   | N/A           |
| tipo di elemento selezionato    | CPAlbumID     |
| ID elemento selezionato      | 300           |



 

Nel controllo di visualizzazione albero viene selezionato il nodo radice per il negozio online. In questo caso, non è presente alcun contenitore e di conseguenza non sono presenti elementi. **L'intero riquadro** attività Libreria visualizza una pagina di individuazione.



| Elemento                  | valore           |
|-----------------------|-----------------|
| attività                  | Esplora          |
| tipo di percorso della libreria | RootLocation    |
| ID percorso della libreria   | N/A             |
| tipo di elemento selezionato    | UnknownLocation |
| ID elemento selezionato      | N/A             |



 

Nel riquadro **attività Sincronizza** il lettore visualizza l'anno 2002 come contenitore di tracce. Nella visualizzazione l'elemento selezionato è la traccia con ID 450.



| Elemento                  | valore           |
|-----------------------|-----------------|
| attività                  | Sincronizza            |
| tipo di percorso della libreria | ReleaseDateYear |
| ID percorso della libreria   | 2002            |
| tipo di elemento selezionato    | CPTrackID       |
| ID elemento selezionato      | 450             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Pagine di individuazione**](discovery-pages.md)
</dt> </dl>

 

 




