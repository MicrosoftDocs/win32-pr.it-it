---
description: Una barriera di sincronizzazione consente a più thread di attendere che tutti i thread raggiungano un determinato punto di esecuzione prima che un thread continui.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barriere di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233488"
---
# <a name="synchronization-barriers"></a>Barriere di sincronizzazione

Una barriera di sincronizzazione consente a più thread di attendere che tutti i thread raggiungano un determinato punto di esecuzione prima che un thread continui. Le barriere di sincronizzazione non possono essere condivise tra i processi.

Le barriere di sincronizzazione sono utili per i calcoli in più fasi, in cui i thread che eseguono lo stesso codice in parallelo devono completare una fase prima di procedere al passaggio successivo.

Per creare una barriera di sincronizzazione, chiamare la funzione [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) e specificare un numero massimo di thread e il numero di volte in cui un thread deve essere ruotato prima di bloccarsi. Avviare quindi i thread che utilizzeranno la barriera. Al termine del lavoro di ogni thread, viene chiamato [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) per attendere la barriera. La funzione **EnterSynchronizationBarrier** blocca ogni thread finché il numero di thread bloccati nella barriera raggiunge il numero massimo di thread per la barriera, a quel punto **EnterSynchronizationBarrier** Sblocca tutti i thread. La funzione **EnterSynchronizationBarrier** restituisce **true** esattamente per uno dei thread che sono stati inseriti nella barriera e restituisce **false** per tutti gli altri thread.

Per rilasciare una barriera di sincronizzazione quando non è più necessaria, chiamare [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). È possibile chiamare questa funzione immediatamente dopo aver chiamato [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) perché tale funzione garantisce che tutti i thread abbiano terminato di usare la barriera prima del rilascio.

Se una barriera di sincronizzazione non viene mai eliminata, i thread possono specificare i **flag della barriera di sincronizzazione senza flag di \_ \_ \_ \_ eliminazione** quando entrano nella barriera. Tutti i thread che usano la barriera devono specificare questo flag; Se un thread non lo è, il flag viene ignorato. Questo flag fa in modo che la funzione ignori il lavoro aggiuntivo necessario per la sicurezza dell'eliminazione, che può migliorare le prestazioni. Si noti che l'eliminazione di una barriera mentre questo flag è attiva può comportare l'accesso a un handle non valido e uno o più thread bloccati in modo permanente.

 

 



