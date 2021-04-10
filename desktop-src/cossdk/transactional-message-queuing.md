---
description: Una transazione è una serie di modifiche apportate a un archivio dati, ad esempio un database o un file system, che devono essere eseguite correttamente o meno.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Accodamento messaggi transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049157"
---
# <a name="transactional-message-queuing"></a>Accodamento messaggi transazionale

Una *transazione* è una serie di modifiche apportate a un archivio dati, ad esempio un database o un file System, che devono essere eseguite correttamente o meno. Per implementare una transazione, un record viene mantenuto nello stato dell'archivio dati prima che la transazione venga avviata e, in caso di esito negativo di una delle modifiche, la transazione restituisce un errore e viene ripristinato o eseguito il rollback dello stato iniziale. Le transazioni vengono utilizzate per mantenere l'integrità dei dati e, di conseguenza, svolgere un ruolo importante nella programmazione di software aziendali.

Spesso, le applicazioni possono essere sviluppate utilizzando una transazione aziendale o un flusso di lavoro suddiviso in più transazioni o attività più piccole. Queste attività sono separate nel tempo e quindi connesse mediante le code di messaggi affidabili.

1.  La prima transazione include il database di immissione dell'ordine. [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) sposta il messaggio da una coda a un'altra coda, esattamente una volta, usando le funzionalità di transazione. Se il database viene aggiornato, viene inserito un messaggio nella coda. Se il messaggio non raggiunge la coda, viene interrotto e viene eseguito il rollback del database.
2.  In un secondo momento, Accodamento messaggi rileva che il server è disponibile. Nessun polling dell'applicazione per l'esistenza del server. Si tratta della seconda transazione.
3.  La terza transazione prevede una query sul database di spedizione e l'aggiornamento del database di spedizione. Se si verifica un errore nel server al centro di questa transazione, viene eseguito il rollback della modifica e il messaggio viene restituito alla coda di input. In questo modo si garantisce che l'integrità dei dati e dei database venga mantenuta durante le transazioni.

 

 



