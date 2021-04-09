---
description: In questo argomento viene descritto come creare, identificare, impostare ed eliminare i timer.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: Informazioni sui timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968603"
---
# <a name="about-timers"></a>Informazioni sui timer

In questo argomento viene descritto come creare, identificare, impostare ed eliminare i timer. Un'applicazione usa un timer per pianificare un evento per una finestra dopo che è trascorso un periodo di tempo specificato. Ogni volta che scade l'intervallo specificato (o il valore di timeout) per un timer, il sistema invia una notifica alla finestra associata al timer. Poiché l'accuratezza di un timer dipende dalla frequenza di clock del sistema e dalla frequenza con cui l'applicazione recupera i messaggi dalla coda di messaggi, il valore di timeout è solo approssimativo.

In questo argomento sono incluse le sezioni seguenti.

-   [Operazioni timer](#timer-operations)
-   [Timer ad alta risoluzione](#high-resolution-timer)
-   [Oggetti timer waitable](#waitable-timer-objects)
-   [Argomenti correlati](#related-topics)

## <a name="timer-operations"></a>Operazioni timer

Le applicazioni creano timer utilizzando la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Un nuovo timer inizia a cronometrare l'intervallo non appena viene creato. Un'applicazione può modificare il valore di timeout di un timer utilizzando l'oggetto **setimer** e può eliminare un timer utilizzando la funzione [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) . Per utilizzare le risorse di sistema in modo efficiente, le applicazioni devono eliminare i timer che non sono più necessari.

Ogni timer ha un identificatore univoco. Quando si crea un timer, un'applicazione può specificare un identificatore o fare in modo che il sistema crei un valore univoco. Il primo parametro di un messaggio di [**\_ timer WM**](wm-timer.md) contiene l'identificatore del timer che ha pubblicato il messaggio.

Se si specifica un handle di finestra nella chiamata a [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer), l'applicazione associa il timer a tale finestra. Ogni volta che il valore di timeout del timer scade, il sistema invia un messaggio [**di \_ timer WM**](wm-timer.md) alla finestra associata al timer. Se non viene specificato alcun handle di finestra nella chiamata a **setimer**, l'applicazione che ha creato il timer deve monitorare la coda di messaggi per i messaggi del **\_ timer WM** e inviarli alla finestra appropriata. Se si specifica una funzione di callback [**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc) , la routine della finestra predefinita chiama la funzione di callback quando elabora il **\_ timer WM**. Pertanto, è necessario inviare messaggi nel thread chiamante, anche quando si usa **TimerProc** anziché elaborare il **\_ timer WM**.

Se è necessario ricevere una notifica al termine del timer, utilizzare un timer in attesa. Per altre informazioni, vedere [oggetti timer waitable](/windows/desktop/Sync/waitable-timer-objects).

## <a name="high-resolution-timer"></a>Timer High-Resolution

Un contatore è un termine generale utilizzato nella programmazione per fare riferimento a una variabile di incremento. Alcuni sistemi includono un contatore delle prestazioni ad alta risoluzione che offre tempi di risoluzione elevata.

Se nel sistema è presente un contatore delle prestazioni ad alta risoluzione, è possibile utilizzare la funzione [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) per esprimere la frequenza, espressa in conteggi al secondo. Il valore del conteggio è dipendente dal processore. In alcuni processori, ad esempio, il conteggio potrebbe essere la frequenza del ciclo del clock del processore.

La funzione [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) Recupera il valore corrente del contatore delle prestazioni ad alta risoluzione. Chiamando questa funzione all'inizio e alla fine di una sezione di codice, un'applicazione usa essenzialmente il contatore come timer ad alta risoluzione. Si supponga, ad esempio, che [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) indichi che la frequenza del contatore delle prestazioni ad alta risoluzione è di 50.000 conteggi al secondo. Se l'applicazione chiama **QueryPerformanceCounter** immediatamente prima e immediatamente dopo la sezione di codice da cronometrare, i valori del contatore potrebbero essere rispettivamente i conteggi 1500 e 3500. Questi valori indicheranno che .04 secondi (2000 conteggi) sono trascorsi durante l'esecuzione del codice.

## <a name="waitable-timer-objects"></a>Oggetti timer waitable

Un oggetto timer che può essere atteso è un oggetto di sincronizzazione il cui stato è impostato su segnalato quando arriva il tempo di scadenza specificato. È possibile creare due tipi di timer che è possibile attendere, ovvero la reimpostazione manuale e la sincronizzazione. Un timer di uno dei due tipi può anche essere un timer periodico.

Un thread usa la funzione [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) o [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) per creare un oggetto timer. Il thread di creazione specifica se il timer è un timer di reimpostazione manuale o un timer di sincronizzazione. Il thread di creazione può specificare un nome per l'oggetto timer. I thread di altri processi possono aprire un handle per un timer esistente specificandone il nome in una chiamata alla funzione [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Qualsiasi thread con un handle a un oggetto timer può utilizzare una delle funzioni di attesa per attendere che lo stato del timer sia impostato su segnalato.

Per ulteriori informazioni sull'utilizzo di oggetti timer in attesa per la sincronizzazione dei thread, vedere [oggetti timer di attesa](/windows/desktop/Sync/waitable-timer-objects).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di timer](using-timers.md)
</dt> </dl>

 

 
