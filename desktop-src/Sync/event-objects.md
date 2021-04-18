---
description: Un oggetto evento è un oggetto di sincronizzazione il cui stato può essere impostato in modo esplicito su segnalato dall'utilizzo della funzione seevent. Di seguito sono riportati i due tipi di oggetto evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Oggetti evento (sincronizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365b42bb7550507fe3522f07d950dac74c88843d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315306"
---
# <a name="event-objects-synchronization"></a>Oggetti evento (sincronizzazione)

Un *oggetto evento* è un oggetto di sincronizzazione il cui stato può essere impostato in modo esplicito su segnalato dall'utilizzo della funzione [**seevent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Di seguito sono riportati i due tipi di oggetto evento.



| Oggetto             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento di reimpostazione manuale | Oggetto evento il cui stato rimane segnalato fino a quando non viene reimpostato in modo esplicito su non segnalato dalla funzione [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Mentre viene segnalato, può essere rilasciato un numero qualsiasi di thread in attesa o thread che specificano successivamente lo stesso oggetto evento in una delle [funzioni di attesa](wait-functions.md).                                                                                                        |
| Evento di reimpostazione automatica   | Un oggetto evento il cui stato rimane segnalato fino al rilascio di un singolo thread in attesa, a quel punto il sistema imposta automaticamente lo stato su non segnalato. Se non c'è alcun thread in attesa, lo stato dell'oggetto evento resta segnalato. Se più di un thread è in attesa, viene selezionato un thread in attesa. Non presupporre un ordine FIFO (First-in, First-out). Gli eventi esterni, ad esempio APC in modalità kernel, possono modificare l'ordine di attesa.<br/> |



 

L'oggetto evento è utile per l'invio di un segnale a un thread che indica che si è verificato un determinato evento. Ad esempio, nell'input e nell'output sovrapposti, il sistema imposta un oggetto evento specificato sullo stato segnalato quando l'operazione sovrapposta è stata completata. Un thread singolo può specificare oggetti evento diversi in diverse operazioni sovrapposte simultanee, quindi utilizzare una delle funzioni di [attesa](wait-functions.md) di più oggetti per attendere che lo stato di uno qualsiasi degli oggetti evento venga segnalato.

Un thread usa la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) o [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) per creare un oggetto evento. Il thread di creazione specifica lo stato iniziale dell'oggetto e indica se si tratta di un oggetto evento di reimpostazione manuale o di reimpostazione automatica. Il thread di creazione può inoltre specificare un nome per l'oggetto evento. I thread di altri processi possono aprire un handle per un oggetto evento esistente specificandone il nome in una chiamata alla funzione [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) . Per ulteriori informazioni sui nomi per gli oggetti mutex, Event, Semaphore e timer, vedere [sincronizzazione interprocesso](interprocess-synchronization.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di oggetti evento](using-event-objects.md)
</dt> </dl>

 

 
