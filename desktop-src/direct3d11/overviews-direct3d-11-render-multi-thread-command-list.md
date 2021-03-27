---
title: Elenco comandi
description: Un elenco di comandi è una sequenza di comandi GPU che possono essere registrati e riprodotti. Un elenco di comandi può migliorare le prestazioni riducendo la quantità di overhead generato dal runtime.
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f8821645588ac7a9b48a4f6ce562c8c48cf96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711542"
---
# <a name="command-list"></a>Elenco comandi

Un elenco di comandi è una sequenza di comandi GPU che possono essere registrati e riprodotti. Un elenco di comandi può migliorare le prestazioni riducendo la quantità di overhead generato dal runtime.

Usare un elenco di comandi negli scenari seguenti:

-   All'interno di un singolo frame, eseguire il rendering di parte della scena in un thread durante la registrazione di un'altra parte della scena in un secondo thread. Alla fine del frame, riprodurre l'elenco dei comandi registrati nel primo thread. Usare questo approccio per ridimensionare attività di rendering complesse tra più thread o Core.
-   Pre-registrare un elenco di comandi prima che sia necessario eseguirne il rendering (ad esempio, durante il caricamento di un livello) e riprodurlo in modo efficiente in un secondo momento nella scena. Questa ottimizzazione funziona correttamente quando è necessario eseguire il rendering di un elemento spesso.

Un elenco di comandi non è modificabile ed è progettato per essere registrato e riprodotto durante una singola esecuzione di un'applicazione. Un elenco di comandi non è progettato per essere pre-registrato prima dell'esecuzione del gioco e caricato dal supporto, perché non è possibile salvare in modo permanente l'elenco.

Un elenco di comandi deve essere registrato da un contesto posticipato, ma è possibile riprodurlo solo in un contesto immediato. I contesti posticipati possono generare elenchi di comandi simultaneamente.

-   Per registrare un elenco di comandi, vedere [procedura: registrare un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-record.md).
-   Per riprodurre un elenco di comandi, vedere [procedura: riprodurre un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-play.md).
-   Quando si usa un elenco di comandi, le prestazioni dipendono dalla quantità di supporto implementata in un driver. Per verificare il supporto dei driver, vedere [procedura: verificare il supporto del driver](overviews-direct3d-11-render-multi-thread-support.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




