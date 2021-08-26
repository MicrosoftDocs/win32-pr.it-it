---
description: Ogni thread ha una priorità dinamica.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Boost di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe04bcd1df27c2456a06d35d83b894243c9871b3799f04bdc3c3df190ef251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032021"
---
# <a name="priority-boosts"></a>Boost di priorità

Ogni thread ha una *priorità dinamica*. Questa è la priorità utilizzata dall'utilità di pianificazione per determinare il thread da eseguire. Inizialmente, la priorità dinamica di un thread è la stessa della priorità di base. Il sistema può aumentare e ridurre la priorità dinamica, per assicurarsi che sia reattivo e che nessun thread sia affamato per il tempo del processore. Il sistema non aumenta la priorità dei thread con un livello di priorità di base compreso tra 16 e 31. Solo i thread con una priorità di base compresa tra 0 e 15 ricevono boost di priorità dinamica.

Il sistema aumenta la priorità dinamica di un thread per migliorarne la velocità di risposta, come indicato di seguito.

-   Quando un processo che usa NORMAL PRIORITY CLASS viene portato in primo piano, l'utilità di pianificazione aumenta la classe di priorità del processo associato alla finestra in primo piano, in modo che sia maggiore o uguale alla classe di priorità di tutti i processi \_ \_ in background. La classe di priorità torna all'impostazione originale quando il processo non è più in primo piano.
-   Quando una finestra riceve input, ad esempio messaggi timer, messaggi del mouse o input da tastiera, l'utilità di pianificazione aumenta la priorità del thread proprietario della finestra.
-   Quando vengono soddisfatte le condizioni di attesa per un thread bloccato, l'utilità di pianificazione aumenta la priorità del thread. Ad esempio, al termine di un'operazione di attesa associata all'I/O su disco o tastiera, il thread riceve un priority boost.

    È possibile disabilitare la funzionalità di aumento della priorità chiamando la [**funzione SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) o [**SetThreadPriorityBoost.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) Per determinare se questa funzionalità è stata disabilitata, chiamare la [**funzione GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) o [**GetThreadPriorityBoost.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)

Dopo aver alzato la priorità dinamica di un thread, l'utilità di pianificazione riduce tale priorità di un livello ogni volta che il thread completa un intervallo di tempo, fino a quando il thread non torna alla priorità di base. La priorità dinamica di un thread non è mai inferiore alla priorità di base.

 

 
