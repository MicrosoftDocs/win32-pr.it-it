---
description: Descrive la coerenza Read Committed, l'isolamento Read committed e i concetti di blocco transazionale in Transactional NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Concetti di base di TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347821"
---
# <a name="basic-txf-concepts"></a>Concetti di base di TxF

## <a name="read-isolation"></a>Isolamento di lettura

Transactional NTFS (TxF) fornisce la coerenza Read Committed.

Un [*writer transazionale*](glossary.md) fa riferimento a un handle di file transazionale aperto con qualsiasi autorizzazione che non fa parte di un accesso in lettura generico, ma fa parte di un accesso in scrittura generico. Un *writer transazionale* Visualizza la versione più recente di un file che include tutte le modifiche apportate dalla stessa transazione. Può essere presente un solo Writer transazionale per ogni file. I writer non sottoposti a transazione sono sempre bloccati da un writer transazionale, anche se il file viene aperto con autorizzazioni di scrittura condivise.

Un [*lettore transazionale*](glossary.md) fa riferimento a un handle di file transazionale aperto con qualsiasi autorizzazione che fa parte di un accesso in lettura generico, ma non fa parte dell'accesso in scrittura generico. Un *lettore transazionale* Visualizza una versione di cui è stato eseguito il commit del file esistente al momento dell'apertura dell'handle di file. Il lettore transazionale è isolato dagli effetti dei writer transazionali. Questo fornisce una visualizzazione coerente del file solo per la durata dell'handle di file e blocca i writer non sottoposti a transazione.

> [!Note]  
> Quando un handle è stato aperto per la modifica con la funzione [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , tutte le aperture successive del file all'interno di tale transazione, se di sola lettura o non vengono convertite dal sistema come writer transazionale a scopo di isolamento e di altra semantica transazionale. Ciò significa che in seguito, quando un handle viene aperto per l'accesso in sola lettura, l'handle non riceve una visualizzazione del file prima dell'inizio della transazione. riceve la visualizzazione delle transazioni attive del file.

 

Un handle di file non transazionale non Visualizza le modifiche apportate all'interno di una transazione fino a quando non viene eseguito il commit della transazione. L'handle di file non transazionale riceve una visualizzazione isolata che è simile a un lettore sottoposto a transazione, ma a differenza di un reader transazionale, riceve l'aggiornamento del file quando un writer transazionale esegue il commit della transazione.

## <a name="isolation-levels"></a>Livelli di isolamento

TxF fornisce un isolamento Read Committed. Questo significa che gli aggiornamenti dei file non vengono visualizzati all'esterno della transazione. Inoltre, se un file viene aperto più volte durante la lettura dei file all'interno della transazione, è possibile che vengano visualizzati risultati diversi a ogni apertura successiva. I file che erano disponibili la prima volta che si accedevano potrebbero non essere disponibili, perché sono stati eliminati, o viceversa.

## <a name="transactional-locking"></a>Blocco transazionale

La creazione di un writer transazionale in un file blocca il file in modo *transazionale* . Dopo che un file è stato bloccato da una transazione, altre file system operazioni esterne alla transazione di blocco che tentano di modificare il file bloccato a livello transazionale avranno esito negativo con **\_ \_ violazione della condivisione degli errori** o **\_ \_ conflitti transazionali**.

Nella tabella seguente viene riepilogato il blocco transazionale.



File attualmente aperto da

File aperto tentato da

Con transazione eseguita

Non transazionale

Lettore

Reader/Writer

Lettore

Reader/Writer

Lettore sottoposto a transazione

Sì

Sì

Sì

No2

Lettura/scrittura transazionale

Sì

No2

Sì

No2

Lettore non sottoposto a transazione

Sì

Sì

Sì

Sì

Lettura/scrittura non in transazioni

No1

No1

Sì

Sì

1. Esito negativo con **errore di \_ transazione \_ transazionale**<br/> 2. esito negativo con **\_ \_ violazione della condivisione degli errori**<br/>



 

Se si apre un flusso denominato per una modifica che utilizza una transazione, è necessario bloccare l'intero file.

Oltre al blocco transazionale, vengono applicate le normali regole di condivisione file NTFS.

In parallelo è necessario considerare le due modalità di condivisione file seguenti:

-   Modalità di blocco transazionale.
-   Modalità di condivisione file normali.

Qualunque sia la modalità più restrittiva è quella che si applica.

 

 




