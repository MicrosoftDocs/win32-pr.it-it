---
description: I progettisti di provider di servizi devono tentare di mantenere breve il tempo di esecuzione delle operazioni sincrone.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Richieste sincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e399fcef1ffba574305b70aee05d7430bcd84746458198b3d33ed6bb0848747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760689"
---
# <a name="synchronous-requests"></a>Richieste sincrone

I progettisti di provider di servizi devono tentare di mantenere breve il tempo di esecuzione delle operazioni sincrone. Ad esempio, è presente un'operazione "Open" chiamata in fase di inizializzazione che prepara il provider di servizi e TAPI per le operazioni successive in un dispositivo. Un provider di servizi la cui implementazione è suddivisa tra il computer client e un server dedicato può avere una ragionevole certezza di poter comunicare con il server remoto. L'implementazione di "Open" potrebbe semplicemente allocare e inizializzare strutture di dati per rappresentare il dispositivo e restituire, rinviando la comunicazione end-to-end fino a quando non viene richiesta un'operazione reale.

Qualsiasi implementazione "ottimistica" di un'operazione sincrona può in seguito riscontrare limitazioni delle risorse o errori di comunicazione remota. In generale, anche un approccio "conservativo" non può impedire completamente questi problemi; I progettisti di provider di servizi devono scegliere il miglior compromesso tra affidabilità e prestazioni. Un errore di questo tipo deve essere gestito normalmente laddove possibile. Dal punto di vista dei dispositivi TSPI, devono rimanere validi per scopi di "bookkeeping" anche se restituiscono lo stato di errore per qualsiasi operazione richiesta.

L'implementazione di un approccio ottimistico per le richieste sincrone non deve essere eseguita a scapito della semantica corretta per l'operazione. Tornando all'esempio "Open", se l'apertura di un dispositivo deve essere in competizione e riservare una risorsa scarsa e non gestibile, ad esempio le porte di comunicazione, è probabile che lo faccia anche se richiede molto tempo.

**TAPI 2.x:** Un'operazione che viene completata in modo sincrono esegue tutta l'elaborazione nella chiamata di funzione eseguita dall'applicazione. La funzione restituisce valori diversi a seconda dell'esito positivo o negativo:

-   **Operazione riuscita sincrona.** Se la richiesta o il servizio corrispondente alla funzione è stato eseguito correttamente, la funzione restituisce zero, che indica l'esito positivo. Tutti i valori scritti come risultato della chiamata di funzione sono affidabili e possono essere usati immediatamente.
-   **Errore sincrono.** Se la funzione rileva un errore e la richiesta non viene eseguita, viene restituito un numero di errore negativo per identificare l'errore.

 

 



