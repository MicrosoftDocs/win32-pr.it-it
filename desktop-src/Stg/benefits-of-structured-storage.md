---
title: Vantaggi dell'archiviazione strutturata
description: COM fornisce un set di servizi chiamati collettivamente archiviazione strutturata.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Archiviazione strutturata Strctd STG, vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708209"
---
# <a name="benefits-of-structured-storage"></a>Vantaggi dell'archiviazione strutturata

COM fornisce un set di servizi chiamati collettivamente archiviazione strutturata. Tra i vantaggi di questi servizi è la riduzione del sovraccarico delle prestazioni e del sovraccarico associato all'archiviazione di oggetti separati in un file flat. Invece di un file flat, COM archivia gli oggetti distinti in un singolo file strutturato costituito da due elementi principali: oggetti di archiviazione e oggetti flusso. Insieme, funzionano come un file system all'interno di un file.

L'archiviazione strutturata risolve i problemi di prestazioni eliminando la necessità di riscrivere completamente un file nell'archivio ogni volta che un nuovo oggetto viene aggiunto a un file composto o un oggetto esistente aumenta di dimensione. I nuovi dati vengono scritti nel successivo percorso disponibile nell'archivio permanente e l'oggetto di archiviazione aggiorna la tabella dei puntatori che gestisce per tenere traccia dei percorsi degli oggetti di archiviazione e degli oggetti flusso. Allo stesso tempo, l'archiviazione strutturata consente agli utenti finali di interagire e gestire un file composto come se si trattasse di un singolo file anziché di una gerarchia nidificata di oggetti separati.

L'archiviazione strutturata offre anche altri vantaggi:

-   **Accesso incrementale**. Se un utente deve accedere a un oggetto all'interno di un file composto, l'utente può caricare e salvare solo tale oggetto, anziché l'intero file.
-   **Uso multiplo**. Più di un utente finale o un'applicazione può leggere e scrivere contemporaneamente le informazioni nello stesso file composto.
-   **Elaborazione delle transazioni**. Gli utenti possono leggere o scrivere in file composti COM in modalità transazionale, in cui le modifiche apportate al file vengono memorizzate nel buffer e possono essere successivamente sottoposte a commit nel file o invertite.
-   **Salvataggi a memoria insufficiente**. L'archiviazione strutturata fornisce funzionalità per il salvataggio di file in situazioni di memoria insufficiente.

 

 




