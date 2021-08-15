---
description: Una barriera di sincronizzazione consente a più thread di attendere fino a quando tutti i thread non hanno raggiunto un determinato punto di esecuzione prima che un thread continui.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barriere di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1247d7ab3b20d4fe89763aea0429d742e8ce1c4d11030088316d4e9f3272556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885983"
---
# <a name="synchronization-barriers"></a>Barriere di sincronizzazione

Una barriera di sincronizzazione consente a più thread di attendere fino a quando tutti i thread non hanno raggiunto un determinato punto di esecuzione prima che un thread continui. Le barriere di sincronizzazione non possono essere condivise tra processi.

Le barriere di sincronizzazione sono utili per i calcoli in più fasi, in cui i thread che eseguono lo stesso codice in parallelo devono completare tutte una fase prima di passare alla successiva.

Per creare una barriera di sincronizzazione, chiamare la funzione [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) e specificare un numero massimo di thread e il numero di volte in cui un thread deve essere ruotato prima del blocco. Avviare quindi i thread che useranno la barriera. Al termine del lavoro, ogni thread chiama [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) per attendere la barriera. La **funzione EnterSynchronizationBarrier** blocca ogni thread fino a quando il numero di thread bloccati nella barriera non raggiunge il numero massimo di thread per la barriera, a quel punto **EnterSynchronizationBarrier** sblocca tutti i thread. La **funzione EnterSynchronizationBarrier** restituisce **TRUE** per esattamente uno dei thread che sono stati inseriti nella barriera e restituisce **FALSE** per tutti gli altri thread.

Per rilasciare una barriera di sincronizzazione quando non è più necessaria, chiamare [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). È possibile chiamare questa funzione immediatamente dopo la chiamata a [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) perché tale funzione garantisce che tutti i thread hanno terminato di usare la barriera prima che venga rilasciata.

Se una barriera di sincronizzazione non verrà mai eliminata, i thread possono specificare il flag **SYNCHRONIZATION BARRIER FLAGS NO \_ \_ \_ \_ DELETE** quando entrano nella barriera. Tutti i thread che usano la barriera devono specificare questo flag. In caso contrario, il flag viene ignorato. Questo flag fa in modo che la funzione salti il lavoro aggiuntivo necessario per la sicurezza dell'eliminazione, migliorando così le prestazioni. Si noti che l'eliminazione di una barriera mentre questo flag è attivo può comportare un accesso handle non valido e uno o più thread bloccati in modo permanente.

 

 



