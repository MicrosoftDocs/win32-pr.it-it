---
description: L'utilità di pianificazione gestisce una coda di thread eseguibili per ogni livello di priorità.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambi di contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c15f5d762525fd4a80030ea10e128e2c30a1ab914e9f17d0f954d80ecfd2e204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143134"
---
# <a name="context-switches"></a>Cambi di contesto

L'utilità di pianificazione gestisce una coda di thread eseguibili per ogni livello di priorità. Questi sono noti come *thread pronti.* Quando un processore diventa disponibile, il sistema esegue un cambio *di contesto.* I passaggi in un cambio di contesto sono:

1.  Salvare il contesto del thread che ha appena terminato l'esecuzione.
2.  Posizionare il thread che ha appena terminato l'esecuzione alla fine della coda per la relativa priorità.
3.  Trovare la coda con la priorità più alta che contiene thread pronti.
4.  Rimuovere il thread all'inizio della coda, caricarne il contesto ed eseguirlo.

Le classi di thread seguenti non sono thread pronti.

-   Thread creati con il flag CREATE \_ SUSPENDED
-   Thread arrestati durante l'esecuzione [**con la funzione SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**o SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Thread in attesa di un oggetto di sincronizzazione o di un input.

Finché i thread sospesi o bloccati non diventano pronti per l'esecuzione, l'utilità di pianificazione non alloca alcun tempo del processore, indipendentemente dalla priorità.

I motivi più comuni per un cambio di contesto sono:

-   L'intervallo di tempo è trascorso.
-   Un thread con priorità più alta è pronto per l'esecuzione.
-   Un thread in esecuzione deve attendere.

Quando un thread in esecuzione deve attendere, rinuncia al resto della relativa sezione temporale.

 

 
