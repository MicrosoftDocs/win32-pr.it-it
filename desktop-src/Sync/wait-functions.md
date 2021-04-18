---
description: Le funzioni Wait consentono a un thread di bloccare la propria esecuzione.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funzioni Wait
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: f5a21b0d95a316b926fcaad037004edc8c418246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316061"
---
# <a name="wait-functions"></a>Funzioni Wait

Le *funzioni Wait* consentono a un thread di bloccare la propria esecuzione. Le funzioni di attesa non vengono restituite fino a quando non vengono soddisfatti i criteri specificati. Il tipo di funzione wait determina il set di criteri utilizzati. Quando viene chiamata una funzione Wait, verifica se i criteri di attesa sono stati soddisfatti. Se i criteri non sono stati soddisfatti, il thread chiamante entra nello stato di attesa fino a quando non sono state soddisfatte le condizioni dei criteri di attesa o non è trascorso l'intervallo di timeout specificato.

-   [Funzioni di attesa a singolo oggetto](#single-object-wait-functions)
-   [Funzioni di attesa di più oggetti](#multiple-object-wait-functions)
-   [Funzioni di attesa alertable](#alertable-wait-functions)
-   [Funzioni di attesa registrate](#registered-wait-functions)
-   [In attesa di un indirizzo](#waiting-on-an-address)
-   [Funzioni Wait e intervalli di timeout](#wait-functions-and-time-out-intervals)
-   [Funzioni di attesa e oggetti di sincronizzazione](#wait-functions-and-synchronization-objects)
-   [Funzioni Wait e creazione di finestre](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funzioni di attesa a singolo oggetto

Le funzioni [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) richiedono un handle per un oggetto di sincronizzazione. Queste funzioni restituiscono quando si verifica una delle condizioni seguenti:

-   L'oggetto specificato è nello stato segnalato.
-   Intervallo di timeout scaduto. L'intervallo di timeout può essere impostato su **infinito** per specificare che il timeout dell'attesa non verrà effettuato.

La funzione [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) consente al thread chiamante di impostare atomicamente lo stato di un oggetto su segnalato e attendere che lo stato di un altro oggetto venga impostato su segnalato.

## <a name="multiple-object-wait-functions"></a>Funzioni di attesa di più oggetti

Le funzioni [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) consentono al thread chiamante di specificare una matrice contenente uno o più handle di oggetti di sincronizzazione. Queste funzioni restituiscono quando si verifica una delle condizioni seguenti:

-   Lo stato di uno degli oggetti specificati è impostato su segnalato oppure gli Stati di tutti gli oggetti sono stati impostati su segnalato. È possibile controllare se nella chiamata di funzione verranno usati uno o tutti gli Stati.
-   Intervallo di timeout scaduto. L'intervallo di timeout può essere impostato su **infinito** per specificare che il timeout dell'attesa non verrà effettuato.

La funzione [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) consentono di specificare oggetti evento di input nella matrice di handle dell'oggetto. Questa operazione viene eseguita quando si specifica il tipo di input da attendere nella coda di input del thread. Ad esempio, un thread può usare **MsgWaitForMultipleObjects** per bloccare l'esecuzione fino a quando lo stato di un oggetto specificato non è stato impostato su segnalato e l'input del mouse è disponibile nella coda di input del thread. Il thread può usare la funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) per recuperare l'input.

Quando si attende che lo stato di tutti gli oggetti sia impostato su segnalato, queste funzioni a più oggetti non modificano gli Stati degli oggetti specificati fino a quando non sono stati impostati segnali per gli Stati di tutti gli oggetti. Ad esempio, lo stato di un oggetto mutex può essere segnalato, ma il thread chiamante non ottiene la proprietà finché gli Stati degli altri oggetti specificati nella matrice non sono stati anche impostati su segnalato. Nel frattempo, un altro thread può ottenere la proprietà dell'oggetto mutex, impostando quindi lo stato su non segnalato.

Quando si attende che lo stato di un singolo oggetto sia impostato su segnalato, queste funzioni a più oggetti controllano gli handle nella matrice in ordine a partire dall'indice 0, fino a quando non viene segnalato uno degli oggetti. Se più oggetti vengono segnalati, la funzione restituisce l'indice del primo handle della matrice il cui oggetto è stato segnalato.

## <a name="alertable-wait-functions"></a>Funzioni di attesa alertable

Le funzioni [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) sono diverse dalle altre funzioni wait in quanto possono facoltativamente eseguire un'operazione di *attesa di avviso*. In un'operazione di attesa di avviso, la funzione può restituire quando vengono soddisfatte le condizioni specificate, ma può anche restituire se il sistema accoda una routine di completamento I/O o un APC per l'esecuzione da parte del thread in attesa. Per altre informazioni sulle operazioni di attesa per avvisi e sulle routine di completamento I/O, vedere [sincronizzazione e input e output sovrapposti](synchronization-and-overlapped-input-and-output.md). Per ulteriori informazioni su APC, vedere la pagina relativa alle [chiamate asincrone alle procedure](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funzioni di attesa registrate

La funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) differisce dalle altre funzioni wait in quanto l'operazione Wait viene eseguita da un thread del pool di [thread](../procthread/thread-pooling.md). Quando vengono soddisfatte le condizioni specificate, la funzione di callback viene eseguita da un thread di lavoro dal pool di thread.

Per impostazione predefinita, un'operazione di attesa registrata è un'operazione di attesa multipla. Il sistema Reimposta il timer ogni volta che l'evento viene segnalato (o scade l'intervallo di timeout) finché non si chiama la funzione [**unregisterwaitex ha provocato**](unregisterwaitex.md) per annullare l'operazione. Per specificare che un'operazione di attesa deve essere eseguita una sola volta, impostare il parametro *dwFlags* di [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) su **WT \_ EXECUTEONLYONCE**.

Se il thread chiama funzioni che usano APC, impostare il parametro *dwFlags* di [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) su **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>In attesa di un indirizzo

Un thread può usare la funzione [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) per attendere che il valore di un indirizzo di destinazione venga modificato da un valore indesiderato a qualsiasi altro valore. Questo consente ai thread di attendere che un valore venga modificato senza dover ruotare o gestire i problemi di sincronizzazione che possono verificarsi quando il thread acquisisce un valore indesiderato, ma il valore viene modificato prima che il thread possa attendere.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) restituisce quando il codice che modifica il valore di destinazione segnala la modifica chiamando [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) per riattivare un singolo thread in attesa o [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) per riattivare tutti i thread in attesa. Se viene specificato un intervallo di timeout con **WaitOnAddress** e nessun thread chiama una funzione Wake, la funzione restituisce quando scade l'intervallo di timeout. Se non viene specificato alcun intervallo di timeout, il thread resta in attesa per un periodo illimitato.

## <a name="wait-functions-and-time-out-intervals"></a>Funzioni Wait e intervalli di timeout

L'accuratezza dell'intervallo di timeout specificato dipende dalla risoluzione del clock di sistema. "Tick" del clock di sistema a una velocità costante. Se l'intervallo di timeout è inferiore alla risoluzione del clock di sistema, il timeout dell'attesa potrebbe essere inferiore al periodo di tempo specificato. Se l'intervallo di timeout è maggiore di un segno di minore di due, l'attesa può trovarsi in qualsiasi punto tra uno e due cicli e così via.

Per aumentare l'accuratezza dell'intervallo di timeout per le funzioni di attesa, chiamare la funzione **timeGetDevCaps** per determinare la risoluzione del timer minima supportata e la funzione **timeBeginPeriod** per impostare il valore minimo per la risoluzione del timer. Prestare attenzione quando si chiama **timeBeginPeriod**, in quanto le chiamate frequenti possono influenzare significativamente il clock di sistema, l'utilizzo dell'alimentazione del sistema e l'utilità di pianificazione. Se si chiama **timeBeginPeriod**, richiamarlo una volta all'inizio dell'applicazione e assicurarsi di chiamare la funzione **timeEndPeriod** alla fine dell'applicazione.

## <a name="wait-functions-and-synchronization-objects"></a>Funzioni di attesa e oggetti di sincronizzazione

Le funzioni Wait possono modificare gli Stati di alcuni tipi di [oggetti di sincronizzazione](synchronization-objects.md). La modifica si verifica solo per l'oggetto o gli oggetti il cui stato segnalato ha causato la restituzione della funzione. Le funzioni Wait possono modificare gli Stati degli oggetti di sincronizzazione come indicato di seguito:

-   Il numero di un oggetto semaforo diminuisce di uno e lo stato del semaforo è impostato su non segnalato se il conteggio è zero.
-   Gli Stati di mutex, l'evento di reimpostazione automatica e gli oggetti di notifica delle modifiche sono impostati su non segnalato.
-   Lo stato di un timer di sincronizzazione è impostato su non segnalato.
-   Gli Stati degli eventi di reimpostazione manuale, timer di reimpostazione manuale, processo, thread e input della console non sono interessati da una funzione di attesa.

## <a name="wait-functions-and-creating-windows"></a>Funzioni Wait e creazione di finestre

È necessario prestare attenzione quando si usano le funzioni di attesa e il codice che crea direttamente o indirettamente Windows. Se un thread crea qualsiasi finestra, deve elaborare i messaggi. Le trasmissioni di messaggi vengono inviate a tutte le finestre nel sistema. Se si dispone di un thread che utilizza una funzione wait senza intervallo di timeout, il sistema si blocca. Due esempi di codice che crea indirettamente Windows sono DDE e la funzione **CoInitialize** . Se pertanto si dispone di un thread che crea Windows, utilizzare [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)anziché le altre funzioni di attesa.

 

 
