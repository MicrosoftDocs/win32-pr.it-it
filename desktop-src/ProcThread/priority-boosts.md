---
description: Ogni thread ha una priorità dinamica.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Aumenti di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231518"
---
# <a name="priority-boosts"></a>Aumenti di priorità

Ogni thread ha una *priorità dinamica*. Si tratta della priorità utilizzata dall'utilità di pianificazione per determinare il thread da eseguire. Inizialmente, la priorità dinamica di un thread corrisponde alla priorità di base. Il sistema può aumentare e ridurre la priorità dinamica, per assicurarsi che sia reattiva e che nessun thread sia affamato per il tempo del processore. Il sistema non incrementa la priorità dei thread con un livello di priorità di base compreso tra 16 e 31. Solo i thread con priorità di base compresa tra 0 e 15 ricevono Boost di priorità dinamica.

Il sistema aumenta la priorità dinamica di un thread per migliorarne la velocità di risposta, come indicato di seguito.

-   Quando un processo che usa la \_ \_ classe di priorità normale viene portato in primo piano, l'utilità di pianificazione incrementa la classe di priorità del processo associato alla finestra in primo piano, in modo che sia maggiore o uguale alla classe di priorità di qualsiasi processo in background. La classe priority restituisce l'impostazione originale quando il processo non è più in primo piano.
-   Quando una finestra riceve l'input, ad esempio i messaggi del timer, i messaggi del mouse o l'input da tastiera, l'utilità di pianificazione aumenta la priorità del thread che possiede la finestra.
-   Quando vengono soddisfatte le condizioni di attesa per un thread bloccato, l'utilità di pianificazione aumenta la priorità del thread. Quando, ad esempio, viene completata un'operazione di attesa associata all'I/O del disco o della tastiera, il thread riceve un priority boost.

    È possibile disabilitare la funzionalità di incremento priorità chiamando la funzione [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) o [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) . Per determinare se questa funzionalità è stata disabilitata, chiamare la funzione [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) o [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) .

Dopo aver generato la priorità dinamica di un thread, l'utilità di pianificazione riduce la priorità di un livello ogni volta che il thread completa un intervallo di tempo, fino a quando il thread non ritorna alla priorità di base. La priorità dinamica di un thread non è mai inferiore alla priorità di base.

 

 
