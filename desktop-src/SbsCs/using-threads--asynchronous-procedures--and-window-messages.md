---
description: I contesti di attivazione sono visibili nell'intero processo.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Thread, procedure asincrone e messaggi di finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529be75a3bc72679f44dfb69196f9487aa4f1de4f3cdbeada4ec89e26f05d646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141704"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Uso di thread, routine asincrone e messaggi di finestra

I contesti di attivazione sono visibili nell'intero processo. Gli stack del contesto di attivazione sono tuttavia per thread e due thread nello stesso processo possono avere stack di attivazione diversi. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) inserisce automaticamente il contesto di attivazione corrente all'inizio dello stack di attivazione del nuovo thread. Ciò può facilitare l'aggiornamento del codice esistente per l'uso di componenti side-by-side perché il nuovo thread può essere eseguito immediatamente nel contesto di attivazione corrente.

Le chiamate di procedura asincrone, i callback delle porte di completamento e qualsiasi altro callback su altri thread ottengono automaticamente il contesto di attivazione dell'origine. Quando viene chiamato il callback, lo stack di attivazione viene pulito. Ciò significa che l'applicazione può usare chiamate di routine asincrone e callback senza attivare in modo esplicito alcun contesto perché la gestione del contesto verrà eseguita dall'infrastruttura side-by-side sottostante. Per rendere attivi altri contesti durante un callback o un nuovo thread, l'applicazione può eseguire la propria gestione del contesto. In questo caso il programma deve usare la sequenza appropriata di funzioni di attivazione del contesto di attivazione e di disattivazione.

I contesti di attivazione sono indipendenti dal thread. L'attivazione di un contesto modifica solo lo stack del thread corrente e non è possibile attivare un contesto tra thread. Il thread A non può forzare un contesto nel thread B. Anche le funzioni dell'API del contesto di attivazione sono in grado di riconoscere il threading.

Quando si usa [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) o [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per inviare un messaggio di finestra a un'altra routine della finestra nel processo, il contesto di attivazione corrente viene attivato prima che il messaggio venga passato alla procedura di destinazione. Il contesto di attivazione corrente è associato al messaggio. In questo modo, i messaggi che fanno riferimento a oggetti COM, nomi di DLL o altre risorse side-by-side mantengono le informazioni di contesto corrette.

 

 
