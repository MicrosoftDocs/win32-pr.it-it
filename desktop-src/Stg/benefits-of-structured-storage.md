---
title: Vantaggi dell'Archiviazione
description: COM fornisce un set di servizi collettivamente denominati archiviazione strutturata.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Structured Archiviazione Strctd Stg , vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a52159f37b3bf443419beaadbcf9f76aa9c5d7209e04b25506eea850c4d3d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663564"
---
# <a name="benefits-of-structured-storage"></a>Vantaggi dell'Archiviazione

COM fornisce un set di servizi collettivamente denominati archiviazione strutturata. Tra i vantaggi di questi servizi vi è la riduzione delle penalità per le prestazioni e il sovraccarico associato all'archiviazione di oggetti separati in un file flat. Anziché un file flat, COM archivia gli oggetti separati in un singolo file strutturato costituito da due elementi principali: oggetti di archiviazione e oggetti flusso. Insieme, funzionano come una file system all'interno di un file.

L'archiviazione strutturata risolve i problemi di prestazioni eliminando la necessità di riscrivere completamente un file nell'archiviazione ogni volta che un nuovo oggetto viene aggiunto a un file composto o le dimensioni di un oggetto esistente aumentano. I nuovi dati vengono scritti nella posizione successiva disponibile nell'archiviazione permanente e l'oggetto di archiviazione aggiorna la tabella dei puntatori che gestisce per tenere traccia delle posizioni degli oggetti di archiviazione e degli oggetti di flusso. Allo stesso tempo, l'archiviazione strutturata consente agli utenti finali di interagire e gestire un file composto come se fosse un singolo file anziché una gerarchia annidata di oggetti separati.

L'archiviazione strutturata offre anche altri vantaggi:

-   **Accesso incrementale**. Se un utente deve accedere a un oggetto all'interno di un file composto, può caricare e salvare solo tale oggetto, anziché l'intero file.
-   **Uso multiplo di**. Più utenti finali o applicazioni possono leggere e scrivere contemporaneamente informazioni nello stesso file composto.
-   **Elaborazione delle transazioni**. Gli utenti possono leggere o scrivere in file composti COM in modalità transazione, in cui le modifiche apportate al file vengono memorizzate nel buffer e successivamente possono essere salvate nel file o invertte.
-   **La memoria insufficiente consente di risparmiare**. L'archiviazione strutturata offre funzionalità per il salvataggio dei file in situazioni di memoria insufficiente.

 

 




