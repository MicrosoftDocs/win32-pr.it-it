---
description: Utilizzare Transactional NTFS per mantenere l'integrità dei dati.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Quando utilizzare Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313869"
---
# <a name="when-to-use-transactional-ntfs"></a>Quando utilizzare Transactional NTFS

Un'applicazione può utilizzare Transactional NTFS (TxF) per mantenere l'integrità dei dati su disco durante le condizioni di errore impreviste. In generale, un'applicazione deve prendere in considerazione l'uso di TxF se l'applicazione Scarica i file e usa altre tecniche per mantenere l'integrità dei dati. TxF può migliorare e semplificare il codice di gestione degli errori dell'applicazione, migliorando al tempo stesso il ripristino e l'affidabilità degli errori. Nelle sezioni seguenti di questo argomento vengono forniti esempi di scenari per l'utilizzo di TxF.

## <a name="updating-a-file"></a>Aggiornamento di un file

L'aggiornamento di un file è un'operazione comune e in genere semplice. Tuttavia, se il sistema o l'applicazione ha esito negativo mentre un'applicazione aggiorna le informazioni su un disco, il risultato può essere irreversibile, perché i dati utente possono essere danneggiati da un'operazione di aggiornamento dei file parzialmente completata. Le applicazioni affidabili eseguono spesso sequenze complesse di copie di file e rinominazioni di file per garantire che i dati non siano danneggiati in caso di errore di un sistema.

TxF rende semplice per un'applicazione proteggere le operazioni di aggiornamento dei file da errori di sistema o di applicazione. Per aggiornare un file in modo sicuro, l'applicazione apre il file in modalità transazionale, esegue gli aggiornamenti necessari e quindi esegue il commit della transazione. Se il sistema o l'applicazione ha esito negativo durante l'aggiornamento del file, TxF ripristina automaticamente il file nello stato in cui si trovava prima dell'avvio dell'aggiornamento del file, evitando così il danneggiamento del file.

## <a name="multi-file-updates"></a>Aggiornamenti su più file

TxF è ancora più importante quando una singola operazione logica interessa più file. Se ad esempio si vuole usare uno strumento per rinominare una delle pagine HTML o ASP in un sito Web, uno strumento ben progettato correggerà anche tutti i collegamenti per usare il nuovo nome file. Tuttavia, un errore durante questa operazione lascia il sito Web in uno stato incoerente, con alcuni collegamenti che fanno riferimento al nome del file precedente. Eseguendo l'operazione di ridenominazione dei file e l'operazione di correzione del collegamento di una singola transazione, TxF garantisce che la ridenominazione e il collegamento del file vengano risolti o non superati come un'unica operazione.

## <a name="consistent-concurrent-updates"></a>Aggiornamenti simultanei coerenti

TxF isola le transazioni simultanee. Se un'applicazione apre un file per una lettura transazionale mentre un'altra applicazione ha lo stesso file aperto per un aggiornamento transazionale, TxF isola gli effetti delle due transazioni una dall'altra. In altre parole, il lettore transazionale Visualizza sempre un'unica versione coerente del file, anche quando il file è in fase di aggiornamento da parte di un'altra transazione.

Un'applicazione può usare questa funzionalità per consentire ai clienti di visualizzare i file mentre altri clienti effettuano aggiornamenti. Un server Web transazionale, ad esempio, può fornire un'unica visualizzazione coerente dei file, mentre un altro strumento Aggiorna contemporaneamente tali file.

> [!Note]  
> TxF non supporta gli aggiornamenti simultanei da più writer in transazioni diverse. TxF supporta solo un singolo writer con più lettori simultanei e coerenti.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordinamento con altri gestori di risorse transazionali

È inoltre possibile utilizzare le transazioni utilizzate con i file system transazionali con il registro di sistema transazionale. Gli aggiornamenti al file e al registro di sistema vengono coordinati con una singola transazione.

Utilizzando le transazioni [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) o System. Transactions, gli aggiornamenti apportati a SQL, MSMQ e altre risorse transazionali possono essere coordinati con gli aggiornamenti di file transazionali. Per ulteriori informazioni, vedere [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))di DTC.

## <a name="unsupported-scenarios"></a>Scenari non supportati

TxF non supporta gli scenari di transazione seguenti:

-   Transazioni sui volumi di rete, ad esempio sulle condivisioni file. TxF non è supportato dai protocolli CIFS/SMB.
-   Transazioni in qualsiasi file system diverso da NTFS.
-   Operazioni transazionali sui file memorizzati nella cache dalla memorizzazione nella cache sul lato client.
-   Accesso ai file tramite ID oggetto.
-   Qualsiasi scenario di writer condiviso.
-   Qualsiasi situazione in cui un file viene aperto per un lungo periodo di tempo (giorni o settimane).

 

 
