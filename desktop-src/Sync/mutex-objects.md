---
description: Un oggetto mutex è un oggetto di sincronizzazione il cui stato è impostato su segnalato quando non è di proprietà di alcun thread e non segnalato quando è di proprietà.
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Oggetti mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883261"
---
# <a name="mutex-objects"></a>Oggetti mutex

Un *oggetto mutex* è un oggetto di sincronizzazione il cui stato è impostato su segnalato quando non è di proprietà di alcun thread e non segnalato quando è di proprietà. Un solo thread alla volta può essere proprietario di un oggetto mutex, il cui nome deriva dal fatto che è utile per il coordinamento dell'accesso a una risorsa condivisa in modo reciprocamente esclusivo. Per impedire, ad esempio, a due thread di scrivere nella memoria condivisa allo stesso tempo, ogni thread attende la proprietà di un oggetto mutex prima di eseguire il codice che accede alla memoria. Dopo la scrittura nella memoria condivisa, il thread rilascia l'oggetto mutex.

Un thread usa la funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) o [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) per creare un oggetto mutex. Il thread di creazione può richiedere la proprietà immediata dell'oggetto mutex ed è anche possibile specificare un nome per l'oggetto mutex. Può anche creare un mutex senza nome. Per ulteriori informazioni sui nomi per gli oggetti mutex, Event, Semaphore e timer, vedere [sincronizzazione interprocesso](interprocess-synchronization.md).

I thread di altri processi possono aprire un handle per un oggetto mutex denominato esistente specificandone il nome in una chiamata alla funzione [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Per passare un handle a un mutex senza nome a un altro processo, usare la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) o l'ereditarietà dell'handle padre-figlio.

Qualsiasi thread con un handle a un oggetto mutex può utilizzare una delle [funzioni Wait](wait-functions.md) per richiedere la proprietà dell'oggetto mutex. Se l'oggetto mutex è di proprietà di un altro thread, la funzione wait blocca il thread di richiesta fino a quando il thread proprietario rilascia l'oggetto mutex usando la funzione [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) . Il valore restituito della funzione Wait indica se la funzione restituita per un motivo diverso da quello del mutex impostato su segnalato.

Se più di un thread è in attesa su un mutex, viene selezionato un thread in attesa. Non presupporre un ordine FIFO (First-in, First-out). Gli eventi esterni, ad esempio APC in modalità kernel, possono modificare l'ordine di attesa.

Quando un thread ottiene la proprietà di un mutex, può specificare lo stesso mutex nelle chiamate ripetute alle [funzioni Wait](wait-functions.md) senza bloccarne l'esecuzione. In questo modo si impedisce a un thread di verificarsi un deadlock durante l'attesa di un mutex di cui è già proprietario. Per rilasciare la proprietà in tali circostanze, il thread deve chiamare [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) una volta per ogni volta che il mutex soddisfa le condizioni di una funzione di attesa.

Se un thread termina senza rilasciare la proprietà di un oggetto mutex, l'oggetto mutex viene considerato abbandonato. Un thread in attesa può acquisire la proprietà di un oggetto mutex abbandonato, ma la funzione wait restituirà **Wait \_ Abandoned** per indicare che l'oggetto mutex è stato abbandonato. Un oggetto mutex abbandonato indica che si è verificato un errore e che tutte le risorse condivise protette dall'oggetto mutex sono in uno stato non definito. Se il thread continua come se l'oggetto mutex non fosse stato abbandonato, non viene più considerato abbandonato dopo che il thread rilascia la proprietà. In questo modo viene ripristinato il comportamento normale se in una funzione Wait viene successivamente specificato un handle per l'oggetto mutex.

Si noti che [gli oggetti sezione critici](critical-section-objects.md) forniscono una sincronizzazione simile a quella fornita dagli oggetti mutex, ad eccezione del fatto che gli oggetti sezione critici possono essere utilizzati solo dai thread di un singolo processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di oggetti mutex](using-mutex-objects.md)
</dt> </dl>

 

 
