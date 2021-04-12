---
title: Posizione e elemento selezionato
description: Posizione e elemento selezionato
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player Online Stores, località
- negozi online, località
- digitare 1 negozi online, località
- Windows Media Player Online Stores, percorsi di libreria
- archivi online, percorsi di libreria
- digitare 1 archivi online, percorsi di libreria
- Windows Media Player Online Stores, elementi selezionati
- archivi online, elementi selezionati
- digitare 1 archivi online, elementi selezionati
- Windows Media Player Library, posizioni
- Libreria Media Player di Windows, elementi selezionati
- libreria, località
- libreria, elementi selezionati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221343"
---
# <a name="location-and-selected-item"></a>Posizione e elemento selezionato

Windows Media Player usa i cinque elementi seguenti per caratterizzare la visualizzazione corrente del contenuto del negozio online:

-   attività
-   tipo di percorso della libreria
-   ID percorso libreria
-   tipo di elemento selezionato
-   ID elemento selezionato

In genere, è possibile considerare la vista in Windows Media Player come contenitore di elementi. Il contenitore dispone di un tipo e un elemento ha un tipo. Tutti gli elementi in un contenitore hanno lo stesso tipo. I tipi di percorso e i tipi di elemento sono entrambi specificati dalle [costanti del percorso della libreria](library-location-constants.md). Se, ad esempio, nella visualizzazione corrente viene visualizzato un singolo album, il tipo di percorso della libreria è CPAlbumID e, poiché un album contiene tracce, il tipo di elemento selezionato è CPTrackID.

La tabella seguente illustra il percorso e i tipi di elemento per diversi contenitori.



| Descrizione del contenitore                              | Tipo di percorso della libreria | Tipo di elemento selezionato |
|-------------------------------------------------------|-----------------------|--------------------|
| Un album che è un contenitore di tracce                | CPAlbumID             | CPTrackID          |
| Elenco che è un contenitore di tracce                  | CPListID              | CPTrackID          |
| Elenco che è un contenitore di album                  | CPListID              | CPAlbumID          |
| Una stazione di radio che è un contenitore di elenchi          | CPRadioID             | CPListID           |
| Il set di tutti gli album, che è un contenitore di album | AllCPAlbumIDs         | CPAlbumID          |
| Il set di tutti i generi, che è un contenitore di generi | AllCPGenreIDs         | CPGenreID          |



 

Le schede in Windows Media Player rappresentano attività diverse. Il lettore Visualizza il contenuto dell'archivio online in tre riquadri attività diversi: **libreria**, **masterizzazione** e **sincronizzazione**. Il riquadro attività libreria è denominato anche riquadro attività **Sfoglia** . In alcuni casi, un riquadro attività è denominato *funzionalità*, quindi è possibile che nella documentazione siano presenti termini come la funzionalità di *masterizzazione* e la funzionalità di *sincronizzazione* .

Gli esempi seguenti illustrano come Windows Media Player usa le cinque informazioni (attività, tipo di percorso della libreria, ID del percorso della libreria, tipo di elemento selezionato, ID elemento selezionato) per caratterizzare visualizzazioni diverse.

Nel riquadro attività **Burn** , il lettore Visualizza un album come contenitore di tracce. L'ID dell'album è 250. Nella visualizzazione l'elemento selezionato corrisponde alla traccia con ID 800. Si noti che 800 è l'ID della traccia nel catalogo del negozio online, non il numero della traccia sull'album.



| Elemento                  | valore     |
|-----------------------|-----------|
| attività                  | Bruciare      |
| tipo di percorso della libreria | CPAlbumID |
| ID percorso libreria   | 250       |
| tipo di elemento selezionato    | CPTrackID |
| ID elemento selezionato      | 800       |



 

Nel riquadro attività di **sincronizzazione** , il lettore Visualizza il set di tutti gli album, che è un contenitore di album. Nella visualizzazione, l'elemento selezionato è l'album con ID 300. Si noti che l'ID del percorso della libreria non è applicabile a questa visualizzazione.



| Elemento                  | valore         |
|-----------------------|---------------|
| attività                  | Sincronizza          |
| tipo di percorso della libreria | AllCPAlbumIDs |
| ID percorso libreria   | N/D           |
| tipo di elemento selezionato    | CPAlbumID     |
| ID elemento selezionato      | 300           |



 

Nel controllo di visualizzazione albero è selezionato il nodo radice per l'archivio online. In questo caso, non è presente alcun contenitore e, di conseguenza, non sono presenti elementi. Il riquadro attività intera **libreria** Visualizza una pagina di individuazione.



| Elemento                  | valore           |
|-----------------------|-----------------|
| attività                  | Esplora          |
| tipo di percorso della libreria | RootLocation    |
| ID percorso libreria   | N/D             |
| tipo di elemento selezionato    | UnknownLocation |
| ID elemento selezionato      | N/D             |



 

Nel riquadro attività di **sincronizzazione** , il lettore Visualizza l'anno 2002 come contenitore di tracce. Nella visualizzazione l'elemento selezionato corrisponde alla traccia con ID 450.



| Elemento                  | valore           |
|-----------------------|-----------------|
| attività                  | Sincronizza            |
| tipo di percorso della libreria | ReleaseDateYear |
| ID percorso libreria   | 2002            |
| tipo di elemento selezionato    | CPTrackID       |
| ID elemento selezionato      | 450             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Pagine di individuazione**](discovery-pages.md)
</dt> </dl>

 

 




