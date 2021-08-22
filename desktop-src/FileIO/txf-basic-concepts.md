---
description: Vengono descritti i concetti di coerenza read committed, isolamento Read Committed e blocco transazionale in NTFS transazionale.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Concetti di base di TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71b2ed4e906fab881fac93a686dcf3aff6e8a95fa72d785ef14320ef92c05ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950970"
---
# <a name="basic-txf-concepts"></a>Concetti di base di TxF

## <a name="read-isolation"></a>Isolamento lettura

NTFS transazionale (TxF) offre coerenza read-committed.

Un [*writer transazione fa*](glossary.md) riferimento a un handle di file transazionato aperto con qualsiasi autorizzazione che non fa parte dell'accesso in lettura generico, ma fa parte dell'accesso in scrittura generico. Un *writer transazionale* visualizza la versione più recente di un file che include tutte le modifiche apportate dalla stessa transazione. Può essere presente un solo writer transazione per ogni file. I writer non transazionati vengono sempre bloccati da un writer transazione, anche se il file viene aperto con autorizzazioni di scrittura condivisa.

Un [*lettore transazione*](glossary.md) fa riferimento a un handle di file transazionato aperto con qualsiasi autorizzazione che fa parte dell'accesso in lettura generico, ma non fa parte dell'accesso in scrittura generico. Un *lettore transazione* visualizza una versione di cui è stato eseguito il commit del file esistente al momento dell'apertura dell'handle di file. Il lettore transazione è isolato dagli effetti dei writer transazionati. In questo modo viene fornita una visualizzazione coerente del file solo per la durata dell'handle di file e vengono bloccati i writer non transazionati.

> [!Note]  
> Quando un handle è stato aperto per la modifica con la funzione [**CreateFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) tutte le successive operazioni di apertura del file all'interno della transazione, indipendentemente dal fatto che siano di sola lettura o meno, vengono convertite dal sistema in un writer transazionale ai fini dell'isolamento e di altra semantica transazionale. Ciò significa che successivamente, quando un handle viene aperto per l'accesso in sola lettura, l'handle non riceve una visualizzazione del file prima dell'avvio della transazione; riceve la visualizzazione transazionale attiva del file.

 

Un handle di file non transazionale non visualizza le modifiche apportate all'interno di una transazione fino a quando non viene eseguito il commit della transazione. L'handle di file non transazionale riceve una vista isolata simile a un lettore transazionale, ma a differenza di un lettore transazionale, riceve l'aggiornamento del file quando un writer transazionale esegue il commit della transazione.

## <a name="isolation-levels"></a>Livelli di isolamento

TxF fornisce l'isolamento read-committed. Ciò significa che gli aggiornamenti dei file non vengono visti all'esterno della transazione. Inoltre, se un file viene aperto più di una volta durante la lettura dei file all'interno della transazione, è possibile che a ogni apertura successiva venga visualizzato un risultato diverso. I file disponibili al primo accesso potrebbero non essere disponibili (perché sono stati eliminati) o viceversa.

## <a name="transactional-locking"></a>Blocco transazionale

La creazione di un writer transazionale su un file blocca *il* file in modo transazionale. Dopo che un file è stato bloccato da una transazione, le altre operazioni file system esterne alla transazione di blocco che tentano di modificare il file bloccato a livello di transazione avranno esito negativo con **ERROR \_ SHARING \_ VIOLATION** o **ERROR \_ TRANSACTIONAL \_ CONFLICT**.

Nella tabella seguente viene riepilogato il blocco transazionale.



File attualmente aperto da

Tentativo di apertura del file eseguito da

Con transazione eseguita

Non transazione

Lettore

Lettore/Writer

Lettore

Lettore/Writer

Lettore transazione

Sì

Sì

Sì

No2

Lettore/writer transazione

Sì

No2

Sì

No2

Lettore non transazione

Sì

Sì

Sì

Sì

Lettore/writer non transazionato

No1

No1

Sì

Sì

1. Esito negativo con **ERRORE \_ TRANSACTIONAL \_ CONFLICT**<br/> 2. Non riesce con **ERROR \_ SHARING \_ VIOLATION**<br/>



 

Se si apre un flusso denominato per una modifica che utilizza una transazione, è necessario che l'intero file sia bloccato.

Oltre al blocco transazionale, vengono applicate le regole di condivisione file NTFS tipiche.

È necessario considerare le due modalità di condivisione file seguenti in parallelo:

-   Modalità di blocco transazionale.
-   Normali modalità di condivisione file.

La modalità più restrittiva è quella applicabile.

 

 




