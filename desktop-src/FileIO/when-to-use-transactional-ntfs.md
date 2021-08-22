---
description: Usare NTFS transazionale per mantenere l'integrità dei dati.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Quando usare NTFS transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f7a67fe6960a8754f768956457afbd04a509bbf9a3c18360b4651e4d9ccda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830131"
---
# <a name="when-to-use-transactional-ntfs"></a>Quando usare NTFS transazionale

Un'applicazione può usare NTFS transazionale (TxF) per mantenere l'integrità dei dati su disco in condizioni di errore impreviste. In generale, un'applicazione deve prendere in considerazione l'uso di TxF se l'applicazione scarica i file e usa altre tecniche per mantenere l'integrità dei dati. TxF può migliorare le prestazioni e semplificare il codice di gestione degli errori dell'applicazione, migliorando al tempo stesso il ripristino e l'affidabilità degli errori. Le sezioni seguenti di questo argomento forniscono esempi di scenari per l'uso di TxF.

## <a name="updating-a-file"></a>Aggiornamento di un file

L'aggiornamento di un file è un'operazione comune e in genere semplice. Tuttavia, se il sistema o l'applicazione non riesce durante l'aggiornamento delle informazioni su un disco da parte di un'applicazione, il risultato può essere irreversico, perché i dati utente possono essere danneggiati da un'operazione di aggiornamento file completata parzialmente. Le applicazioni affidabili spesso eseguono sequenze complesse di copie di file e ridenominazioni di file per garantire che i dati non siano danneggiati in caso di errore del sistema.

TxF rende più semplice per un'applicazione proteggere le operazioni di aggiornamento dei file da errori del sistema o dell'applicazione. Per aggiornare un file in modo sicuro, l'applicazione apre il file in modalità transazionale, esegue gli aggiornamenti necessari e quindi esegue il commit della transazione. Se il sistema o l'applicazione non riesce durante l'aggiornamento del file, TxF ripristina automaticamente il file allo stato precedente all'inizio dell'aggiornamento del file, evitando così il danneggiamento del file.

## <a name="multi-file-updates"></a>Aggiornamenti su più file

TxF è ancora più importante quando una singola operazione logica influisce su più file. Ad esempio, se si vuole usare uno strumento per rinominare una delle pagine HTML o ASP in un sito Web, uno strumento ben progettato correggerà anche tutti i collegamenti in modo da usare il nuovo nome file. Tuttavia, un errore durante questa operazione lascia il sito Web in uno stato incoerente, con alcuni collegamenti che fanno ancora riferimento al nome del file precedente. Rendendo l'operazione di ridenominazione dei file e l'operazione di correzione del collegamento una singola transazione, TxF garantisce che la ridenominazione del file e la correzione del collegamento riescano o non riescano come singola operazione.

## <a name="consistent-concurrent-updates"></a>Aggiornamenti simultanei coerenti

TxF isola le transazioni simultanee. Se un'applicazione apre un file per una lettura transazionale mentre un'altra applicazione ha lo stesso file aperto per un aggiornamento transazionale, TxF isola gli effetti delle due transazioni l'una dall'altra. In altre parole, il lettore transazionale visualizza sempre una singola versione coerente del file, anche mentre tale file è in corso di aggiornamento da parte di un'altra transazione.

Un'applicazione può usare questa funzionalità per consentire ai clienti di visualizzare i file mentre altri clienti effettuano aggiornamenti. Ad esempio, un server Web transazionale può fornire una singola visualizzazione coerente dei file, mentre un altro strumento aggiorna contemporaneamente tali file.

> [!Note]  
> TxF non supporta gli aggiornamenti simultanei da parte di più writer in transazioni diverse. TxF supporta un solo writer con più lettori simultanei e coerenti.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordinamento con altri gestori di risorse transazione

Le transazioni utilizzate con i file system transazionale possono essere usate anche con il Registro di sistema transazionale. Gli aggiornamenti al file e al Registro di sistema vengono coordinati con una singola transazione.

Usando [transazioni Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) o System.Transactions, gli aggiornamenti apportati a SQL, MSMQ e ad altre risorse transazionali possono essere coordinati con gli aggiornamenti di file transazionali. Per altre informazioni, vedere [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))di DTC.

## <a name="unsupported-scenarios"></a>Scenari non supportati

TxF non supporta gli scenari di transazione seguenti:

-   Transazioni su volumi di rete, ad esempio su condivisioni file. TxF non è supportato dai protocolli CIFS/SMB.
-   Le transazioni in qualsiasi file system diverse da NTFS.
-   Operazioni transazionali sui file memorizzati nella cache dal lato client.
-   Accesso ai file tramite ID oggetto.
-   Qualsiasi scenario di scrittura condivisa.
-   Qualsiasi situazione in cui un file viene aperto per un lungo periodo di tempo (giorni o settimane).

 

 
