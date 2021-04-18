---
description: I progettisti del provider di servizi devono provare a tenere corto il tempo di esecuzione delle operazioni sincrone.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Richieste sincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318927"
---
# <a name="synchronous-requests"></a>Richieste sincrone

I progettisti del provider di servizi devono provare a tenere corto il tempo di esecuzione delle operazioni sincrone. Ad esempio, è presente un'operazione "Open" chiamata al momento dell'inizializzazione che prepara il provider di servizi e TAPI per le operazioni successive in un dispositivo. Un provider di servizi la cui implementazione è suddivisa tra il computer client e un server dedicato può avere una ragionevole confidenza per poter comunicare con il server remoto. La relativa implementazione di "Open" potrebbe solo allocare e inizializzare le strutture di dati per rappresentare il dispositivo e restituire, posticipando la comunicazione end-to-end fino a quando non viene richiesta un'operazione reale.

Qualsiasi implementazione "ottimistica" di un'operazione sincrona può in seguito riscontrare limitazioni delle risorse o errori di comunicazione remota. In generale, anche un approccio "conservativo" non può impedire completamente questi problemi. i progettisti del provider di servizi devono scegliere il migliore compromesso tra affidabilità e prestazioni. Un errore di questo tipo deve essere gestito normalmente laddove possibile. Dal punto di vista dei dispositivi TSPI, devono rimanere validi per gli scopi di "contabilità" anche se restituiscono lo stato di errore per qualsiasi operazione richiesta.

L'implementazione di un approccio ottimistico per le richieste sincrone non deve essere eseguita a scapito della semantica corretta per l'operazione. Tornando all'esempio "Open", se l'apertura di un dispositivo deve competere e riservare una risorsa scarsa e non condivisibile, ad esempio le porte di comunicazione, è consigliabile eseguire questa operazione anche se è dispendiosa in termini di tempo.

**TAPI 2. x:** Un'operazione che viene completata in modo sincrono esegue tutta la relativa elaborazione nella chiamata di funzione eseguita dall'applicazione. La funzione restituisce valori diversi a seconda dell'esito positivo o negativo:

-   **Esito positivo sincrono.** Se la richiesta o il servizio corrispondente alla funzione è stato eseguito correttamente, la funzione restituisce zero, che indica l'esito positivo. Tutti i valori scritti come risultato della chiamata di funzione sono affidabili e possono essere usati immediatamente.
-   **Errore sincrono.** Se la funzione rileva un errore e la richiesta non viene eseguita, per identificare l'errore viene restituito un numero di errore negativo.

 

 



