---
description: I contesti di attivazione sono visibili nell'intero processo.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Thread, procedure asincrone e messaggi della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878973"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Utilizzo di thread, procedure asincrone e messaggi della finestra

I contesti di attivazione sono visibili nell'intero processo. Gli stack del contesto di attivazione sono tuttavia per thread e due thread nello stesso processo possono avere stack di attivazione diversi. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) inserisce automaticamente il contesto di attivazione corrente all'inizio dello stack di attivazione del nuovo thread. Questo può facilitare l'aggiornamento del codice esistente per l'uso di componenti affiancati perché il nuovo thread può essere eseguito immediatamente nel contesto di attivazione corrente.

Le chiamate di procedure asincrone, i callback della porta di completamento e qualsiasi altro callback su altri thread ottengono automaticamente il contesto di attivazione dell'origine. Quando viene chiamato il callback, lo stack di attivazione viene eliminato. Ciò significa che l'applicazione può utilizzare chiamate di procedure asincrone e callback senza attivare in modo esplicito i contesti perché la gestione del contesto verrà eseguita dall'infrastruttura side-by-side sottostante. Per rendere attivi altri contesti durante un callback o un nuovo thread, l'applicazione può eseguire la propria gestione del contesto. In questo caso il programma deve usare la sequenza appropriata di funzioni attive del contesto di attivazione e disattivare le funzioni.

I contesti di attivazione sono indipendenti dal thread. L'attivazione di un contesto cambia solo lo stack del thread corrente e non è possibile attivare un contesto tra i thread. Il thread A non può forzare un contesto sul thread B. Anche le funzioni dell'API del contesto di attivazione sono compatibili con il Threading.

Quando si utilizza [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) o [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per inviare un messaggio della finestra a un'altra routine della finestra nel processo, il contesto di attivazione corrente viene attivato prima che il messaggio venga passato alla procedura di destinazione. Il contesto di attivazione corrente viene inserito insieme al messaggio. In questo modo si garantisce che i messaggi che fanno riferimento a oggetti COM, nomi DLL o altre risorse affiancate mantengano le informazioni di contesto corrette.

 

 
