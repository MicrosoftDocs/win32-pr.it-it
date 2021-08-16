---
description: Le funzioni di attesa consentono a un thread di bloccare la propria esecuzione.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funzioni di attesa
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764965"
---
# <a name="wait-functions"></a>Funzioni di attesa

*Le funzioni di* attesa consentono a un thread di bloccare la propria esecuzione. Le funzioni di attesa non restituiscono finché non vengono soddisfatti i criteri specificati. Il tipo di funzione di attesa determina il set di criteri usati. Quando viene chiamata una funzione di attesa, verifica se i criteri di attesa sono stati soddisfatti. Se i criteri non sono stati soddisfatti, il thread chiamante entra nello stato di attesa fino a quando non vengono soddisfatte le condizioni dei criteri di attesa o non è trascorso l'intervallo di timeout specificato.

-   [Funzioni di attesa a oggetto singolo](#single-object-wait-functions)
-   [Funzioni di attesa a più oggetti](#multiple-object-wait-functions)
-   [Funzioni di attesa avvisabili](#alertable-wait-functions)
-   [Funzioni di attesa registrate](#registered-wait-functions)
-   [In attesa di un indirizzo](#waiting-on-an-address)
-   [Funzioni di attesa e intervalli di timeout](#wait-functions-and-time-out-intervals)
-   [Funzioni di attesa e oggetti di sincronizzazione](#wait-functions-and-synchronization-objects)
-   [Funzioni di attesa e creazione di Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funzioni di attesa a oggetto singolo

Le [**funzioni SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) richiedono un handle per un oggetto di sincronizzazione. Queste funzioni restituiscono quando si verifica una delle condizioni seguenti:

-   L'oggetto specificato è nello stato segnalato.
-   L'intervallo di timeout è trascorso. L'intervallo di timeout può essere impostato su **INFINITE** per specificare che l'attesa non si timeout.

La [**funzione SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) consente al thread chiamante di impostare in modo atomico lo stato di un oggetto su segnalato e attendere che lo stato di un altro oggetto sia impostato su segnalato.

## <a name="multiple-object-wait-functions"></a>Funzioni di attesa a più oggetti

Le funzioni [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) consentono al thread chiamante di specificare una matrice contenente uno o più handle di oggetto di sincronizzazione. Queste funzioni restituiscono quando si verifica una delle condizioni seguenti:

-   Lo stato di uno degli oggetti specificati è impostato su segnalato o gli stati di tutti gli oggetti sono stati impostati su segnalato. È possibile controllare se uno o tutti gli stati verranno usati nella chiamata di funzione.
-   L'intervallo di timeout è trascorso. L'intervallo di timeout può essere impostato su **INFINITE** per specificare che l'attesa non si timeout.

Le [**funzioni MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) consentono di specificare oggetti evento di input nella matrice di handle di oggetto. Questa operazione viene eseguita quando si specifica il tipo di input da attendere nella coda di input del thread. Ad esempio, un thread può usare **MsgWaitForMultipleObjects** per bloccare l'esecuzione fino a quando lo stato di un oggetto specificato non è stato impostato su segnalato e non è disponibile l'input del mouse nella coda di input del thread. Il thread può usare la [**funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) per recuperare l'input.

Quando si attende che gli stati di tutti gli oggetti siano impostati su segnalato, queste funzioni a più oggetti non modificano gli stati degli oggetti specificati fino a quando non vengono impostati gli stati di tutti gli oggetti. Ad esempio, lo stato di un oggetto mutex può essere segnalato, ma il thread chiamante non ottiene la proprietà finché non sono stati impostati anche gli stati degli altri oggetti specificati nella matrice su segnalato. Nel frattempo, un altro thread può ottenere la proprietà dell'oggetto mutex, impostandone lo stato su non associato.

Quando si attende che lo stato di un singolo oggetto sia impostato su segnalato, queste funzioni a più oggetti controllano gli handle nella matrice in ordine a partire dall'indice 0, fino a quando uno degli oggetti non viene segnalato. Se più oggetti vengono segnalati, la funzione restituisce l'indice del primo handle nella matrice il cui oggetto è stato segnalato.

## <a name="alertable-wait-functions"></a>Funzioni di attesa avvisabili

Le funzioni [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) differiscono dalle altre funzioni di attesa in quanto facoltativamente possono eseguire un'operazione di attesa *avvisabile.* In un'operazione di attesa avvisabile, la funzione può restituire quando vengono soddisfatte le condizioni specificate, ma può anche restituire se il sistema accoda una routine di completamento I/O o un APC per l'esecuzione da parte del thread in attesa. Per altre informazioni sulle operazioni di attesa avvisabili e sulle routine di completamento di I/O, vedere Sincronizzazione e [input e output sovrapposti.](synchronization-and-overlapped-input-and-output.md) Per altre informazioni sulle API, vedere [Chiamate di procedura asincrone](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funzioni di attesa registrate

La [**funzione RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) è diversa dalle altre funzioni di attesa in cui l'operazione di attesa viene eseguita da un thread del [pool di thread](../procthread/thread-pooling.md). Quando vengono soddisfatte le condizioni specificate, la funzione di callback viene eseguita da un thread di lavoro dal pool di thread.

Per impostazione predefinita, un'operazione di attesa registrata è un'operazione con più attese. Il sistema reimposta il timer ogni volta che l'evento viene segnalato (o l'intervallo di timeout è scaduto) fino a quando non si chiama la funzione [**UnregisterWaitEx**](unregisterwaitex.md) per annullare l'operazione. Per specificare che un'operazione di attesa deve essere eseguita una sola volta, impostare il *parametro dwFlags* di [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) su **WT \_ EXECUTEONLYONCE**.

Se il thread chiama funzioni che usano API, impostare il *parametro dwFlags* di [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) su **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>In attesa di un indirizzo

Un thread può usare la [**funzione WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) per attendere che il valore di un indirizzo di destinazione cambi da un valore indesiderato a qualsiasi altro valore. Ciò consente ai thread di attendere la modifica di un valore senza dover attivare o gestire i problemi di sincronizzazione che possono verificarsi quando il thread acquisisce un valore indesiderato, ma il valore cambia prima che il thread possa attendere.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) restituisce quando il codice che modifica il valore di destinazione segnala la modifica chiamando [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) per riattivare un singolo thread in attesa o [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) per riattivare tutti i thread in attesa. Se viene specificato un intervallo di timeout con **WaitOnAddress** e nessun thread chiama una funzione di riattivazione, la funzione restituisce quando l'intervallo di timeout è trascorso. Se non viene specificato alcun intervallo di timeout, il thread attende a tempo indeterminato.

## <a name="wait-functions-and-time-out-intervals"></a>Funzioni di attesa e intervalli di timeout

L'accuratezza dell'intervallo di timeout specificato dipende dalla risoluzione dell'orologio di sistema. L'orologio di sistema "tick" a una velocità costante. Se l'intervallo di timeout è minore della risoluzione dell'orologio di sistema, il timeout dell'attesa potrebbe essere inferiore al periodo di tempo specificato. Se l'intervallo di timeout è maggiore di un tick ma minore di due, l'attesa può essere compresa tra uno e due tick e così via.

Per aumentare l'accuratezza dell'intervallo di timeout per le funzioni di attesa, chiamare la funzione **timeGetDevCaps** per determinare la risoluzione minima del timer supportata e la funzione **timeBeginPeriod** per impostare la risoluzione del timer sul valore minimo. Prestare attenzione quando si chiama **timeBeginPeriod**, in quanto le chiamate frequenti possono influire in modo significativo sull'orologio di sistema, sull'utilizzo dell'alimentazione del sistema e sull'utilità di pianificazione. Se si chiama **timeBeginPeriod**, chiamarlo una volta all'inizio dell'applicazione e assicurarsi di chiamare la funzione **timeEndPeriod** alla fine dell'applicazione.

## <a name="wait-functions-and-synchronization-objects"></a>Funzioni di attesa e oggetti di sincronizzazione

Le funzioni di attesa possono modificare gli stati di alcuni tipi di oggetti [di sincronizzazione.](synchronization-objects.md) La modifica viene eseguita solo per l'oggetto o gli oggetti il cui stato segnalato ha causato la restituzione della funzione. Le funzioni di attesa possono modificare gli stati degli oggetti di sincronizzazione come indicato di seguito:

-   Il conteggio di un oggetto semaforo diminuisce di uno e lo stato del semaforo viene impostato su non associato se il conteggio è zero.
-   Gli stati di mutex, evento di reimpostazione automatica e oggetti di notifica di modifica sono impostati su senza assegnazione.
-   Lo stato di un timer di sincronizzazione è impostato su Nonsignaled.
-   Gli stati degli oggetti evento di reimpostazione manuale, timer di reimpostazione manuale, processo, thread e input della console non sono interessati da una funzione di attesa.

## <a name="wait-functions-and-creating-windows"></a>Funzioni di attesa e creazione di Windows

È necessario prestare attenzione quando si usano le funzioni di attesa e il codice che crea direttamente o indirettamente le finestre. Se un thread crea finestre, deve elaborare i messaggi. Le trasmissioni di messaggi vengono inviate a tutte le finestre del sistema. Se si dispone di un thread che usa una funzione di attesa senza intervallo di timeout, il sistema verrà deadlock. Due esempi di codice che crea indirettamente finestre sono DDE e **la funzione CoInitialize.** Pertanto, se si dispone di un thread che crea finestre, usare [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)anziché le altre funzioni di attesa.

 

 
