---
description: Una transazione è una serie di modifiche di un archivio dati (ad esempio un database o un file system) garantite per essere tutte eseguite correttamente o non essere eseguite affatto.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Accodamento messaggi transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3282a95d4f9a3ba451e78fe4d9f17acf007b0007abea4fdb4951de9c1540383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636731"
---
# <a name="transactional-message-queuing"></a>Accodamento messaggi transazionale

Una *transazione* è una serie di modifiche di un archivio dati (ad esempio un database o un file system) garantite per essere tutte eseguite correttamente o non essere eseguite affatto. Per implementare una transazione, un record viene mantenuto dello stato dell'archivio dati prima dell'inizio della transazione e, se una delle modifiche ha esito negativo, la transazione restituisce un errore e lo stato iniziale viene ripristinato (o ne viene eseguito il rollback). Le transazioni vengono usate per mantenere l'integrità dei dati e di conseguenza svolgono un ruolo importante nella programmazione del software aziendale.

Spesso, le applicazioni possono essere sviluppate usando una transazione aziendale o un flusso di lavoro suddiviso in diverse transazioni o attività più piccole. Queste attività vengono separate nel tempo e quindi connesse tramite code di messaggi affidabili.

1.  La prima transazione riguarda il database di immissione degli ordini. [Accodamento messaggi sposta](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) il messaggio da una coda a un'altra, esattamente una volta, usando le funzionalità di transazione. Se il database viene aggiornato, nella coda è presente un messaggio. Se il messaggio non raggiunge la coda, viene interrotto e viene eseguito il rollback del database.
2.  Successivamente, Accodamento messaggi rileva che il server è disponibile. Non è disponibile alcun polling dell'applicazione per l'esistenza del server. Si tratta della seconda transazione.
3.  La terza transazione prevede una query del database di spedizione e l'aggiornamento del database di spedizione. Se il server ha esito negativo durante la transazione, viene eseguito il rollback della modifica e il messaggio viene restituito alla coda di input. Ciò garantisce che l'integrità dei dati e dei database sia mantenuta durante le transazioni.

 

 



