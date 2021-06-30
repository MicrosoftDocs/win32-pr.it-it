---
description: Un oggetto evento è un oggetto di sincronizzazione il cui stato può essere impostato in modo esplicito su segnalato tramite la funzione SetEvent. Di seguito sono riportati i due tipi di oggetto evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Oggetti evento (sincronizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ef4f5102df91cabb76529c9d4a9958859418aa
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102135"
---
# <a name="event-objects-synchronization"></a>Oggetti evento (sincronizzazione)

Un *oggetto evento* è un oggetto di sincronizzazione il cui stato può essere impostato in modo esplicito su segnalato tramite la funzione [**SetEvent.**](/windows/win32/api/synchapi/nf-synchapi-setevent) Di seguito sono riportati i due tipi di oggetto evento.



| Oggetto             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento di reimpostazione manuale | Oggetto evento il cui stato rimane segnalato fino a quando non viene reimpostato in modo esplicito su non segnalato dalla [**funzione ResetEvent.**](/windows/win32/api/synchapi/nf-synchapi-resetevent) Mentre viene segnalato, può essere rilasciato qualsiasi numero di thread in attesa [](wait-functions.md)o thread che successivamente specificano lo stesso oggetto evento in una delle funzioni di attesa.                                                                                                        |
| Evento di reimpostazione automatica   | Oggetto evento il cui stato rimane segnalato fino al rilascio di un singolo thread in attesa, in cui il sistema imposta automaticamente lo stato su non segnalato. Se non c'è alcun thread in attesa, lo stato dell'oggetto evento resta segnalato. Se sono in attesa più thread, viene selezionato un thread in attesa. Non presupporre un ordine FIFO (First-In, First Out). Gli eventi esterni, ad esempio le API in modalità kernel, possono modificare l'ordine di attesa.<br/> |



 

L'oggetto evento è utile per inviare un segnale a un thread che indica che si è verificato un evento specifico. Ad esempio, nell'input e nell'output sovrapposti, il sistema imposta un oggetto evento specificato sullo stato segnalato quando l'operazione sovrapposta è stata completata. Un singolo thread può specificare oggetti evento diversi in diverse operazioni simultanee sovrapposte, quindi usare una delle funzioni di attesa a più oggetti per attendere che lo stato di uno degli oggetti evento sia segnalato. [](wait-functions.md)

Un thread usa la [**funzione CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) o [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) per creare un oggetto evento. Il thread di creazione specifica lo stato iniziale dell'oggetto e se si tratta di un oggetto evento di reimpostazione manuale o reimpostazione automatica. Il thread di creazione può anche specificare un nome per l'oggetto evento. I thread in altri processi possono aprire un handle per un oggetto evento esistente specificandone il nome in una chiamata alla [**funzione OpenEvent.**](/windows/win32/api/synchapi/nf-synchapi-openeventa) Per altre informazioni sui nomi per gli oggetti mutex, event, semaphore e timer, vedere [Sincronizzazione interprocesso](interprocess-synchronization.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di oggetti evento](using-event-objects.md)
</dt> </dl>

 

 
