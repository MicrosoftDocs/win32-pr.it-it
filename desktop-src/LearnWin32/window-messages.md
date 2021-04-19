---
title: Messaggi finestra (introduzione a Win32 e C++)
description: .
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ea533a89cb0ccf7053945cd693cc6e1ef5c28
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320253"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Messaggi finestra (introduzione a Win32 e C++)

Un'applicazione GUI deve rispondere agli eventi dell'utente e del sistema operativo.

- Gli **eventi dell'utente** includono tutti i modi in cui un utente può interagire con il programma: clic del mouse, tratti chiave, movimenti dello schermo touchscreen e così via.
- **Gli eventi del sistema operativo** includono qualsiasi elemento "esterno" del programma che può influire sul comportamento del programma. Ad esempio, l'utente potrebbe inserire un nuovo dispositivo hardware oppure è possibile che Windows entri in uno stato di alimentazione inferiore (sospensione o ibernazione).

Questi eventi possono verificarsi in qualsiasi momento mentre il programma è in esecuzione, in quasi tutti gli ordini. In che modo è possibile strutturare un programma il cui flusso di esecuzione non può essere previsto in anticipo?

Per risolvere questo problema, Windows utilizza un modello di passaggio dei messaggi. Il sistema operativo comunica con la finestra dell'applicazione passandovi messaggi. Un messaggio è semplicemente un codice numerico che designa un evento specifico. Se, ad esempio, l'utente preme il pulsante sinistro del mouse, la finestra riceve un messaggio con il seguente codice di messaggio.

```C++
#define WM_LBUTTONDOWN    0x0201
```

A alcuni messaggi è associato un dato. Il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , ad esempio, include la coordinata x e la coordinata y del cursore del mouse.

Per passare un messaggio a una finestra, il sistema operativo chiama la routine della finestra registrata per tale finestra. E ora si conosce la procedura per la finestra.

## <a name="the-message-loop"></a>Ciclo del messaggio

Un'applicazione riceverà migliaia di messaggi durante l'esecuzione. Tenere presente che tutti i tasti di sequenza e clic del pulsante del mouse generano un messaggio. Inoltre, un'applicazione può disporre di più finestre, ognuna con la propria routine della finestra. In che modo il programma riceve tutti i messaggi e li recapita alla procedura della finestra corretta? L'applicazione richiede un ciclo per recuperare i messaggi e inviarli alle finestre corrette.

Per ogni thread che crea una finestra, il sistema operativo crea una coda per i messaggi della finestra. Questa coda include i messaggi per tutte le finestre create in tale thread. La coda stessa è nascosta dal programma. Non è possibile modificare direttamente la coda. Tuttavia, è possibile effettuare il pull di un messaggio dalla coda chiamando la funzione [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Questa funzione rimuove il primo messaggio dall'inizio della coda. Se la coda è vuota, la funzione si blocca fino a quando non viene accodato un altro messaggio. Il fatto che i blocchi [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) non rispondano al programma. Se non sono presenti messaggi, il programma non deve eseguire alcuna operazione. Se è necessario eseguire l'elaborazione in background, è possibile creare thread aggiuntivi che continuano a essere eseguiti mentre **GetMessage** resta in attesa di un altro messaggio. (Vedere [evitare colli di bottiglia nella routine della finestra](writing-the-window-procedure.md)).

Il primo parametro di [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) è l'indirizzo di una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) . Se la funzione ha esito positivo, compila la struttura **msg** con le informazioni sul messaggio. Sono incluse la finestra di destinazione e il codice del messaggio. Gli altri tre parametri consentono di filtrare i messaggi che si ottengono dalla coda. In quasi tutti i casi, questi parametri vengono impostati su zero.

Sebbene la struttura del messaggio contenga informazioni sul messaggio, [**la struttura non**](/windows/win32/api/winuser/ns-winuser-msg) verrà mai esaminata direttamente. Al contrario, verrà passato direttamente ad altre due funzioni.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

La funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) è correlata all'input da tastiera. Converte le sequenze di tasti (tasto giù, tasto su) in caratteri. Non è necessario comprendere il funzionamento di questa funzione; Ricordarsi di chiamarlo prima di [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Il collegamento alla documentazione MSDN fornirà ulteriori informazioni, se si è curiosi.

La funzione [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) indica al sistema operativo di chiamare la routine della finestra che rappresenta la destinazione del messaggio. In altre parole, il sistema operativo cerca l'handle della finestra nella relativa tabella di finestre, trova il puntatore a funzione associato alla finestra e richiama la funzione.

Si supponga, ad esempio, che l'utente prema il pulsante sinistro del mouse. Causa una catena di eventi:

1. Il sistema operativo inserisce un messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) nella coda di messaggi.
2. Il programma chiama la funzione [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) estrae il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) dalla coda e compila la struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) .
4. Il programma chiama le funzioni [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .
5. All'interno di [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), il sistema operativo chiama la routine della finestra.
6. La procedura della finestra può rispondere al messaggio o ignorarla.

Quando la routine della finestra viene restituita, torna a [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Viene restituito al ciclo di messaggi per il messaggio successivo. Finché il programma è in esecuzione, i messaggi continueranno ad arrivare alla coda. Pertanto, è necessario disporre di un ciclo che esegue continuamente il pull dei messaggi dalla coda e li invii. È possibile considerare il ciclo come segue:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Come scritto, ovviamente, questo ciclo non dovrebbe mai terminare. Qui viene restituito il valore restituito per la funzione [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) . In genere, **GetMessage** restituisce un valore diverso da zero. Quando si desidera uscire dall'applicazione e interrompere il ciclo di messaggi, chiamare la funzione [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) .

```C++
        PostQuitMessage(0);
```

La funzione [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) inserisce un messaggio [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) nella coda di messaggi. **WM \_ QUIT** è un messaggio speciale: fa in modo che [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) restituisca zero, segnalando la fine del ciclo di messaggi. Ecco il ciclo di messaggi modificato.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Finché [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) restituisce un valore diverso da zero, l'espressione nel ciclo **while** restituisce true. Dopo aver chiamato [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage), l'espressione diventa false e il programma si interrompe dal ciclo. Un risultato interessante di questo comportamento è che la routine della finestra non riceve mai un messaggio [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) . Pertanto, non è necessario disporre di un'istruzione case per questo messaggio nella routine della finestra.

La prossima domanda ovvia è quando chiamare [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Si tornerà a questa domanda nell'argomento [chiusura della finestra](closing-the-window.md), ma prima di tutto è necessario scrivere la routine della finestra.

## <a name="posted-messages-versus-sent-messages"></a>Messaggi inviati e messaggi inviati

La sezione precedente ha parlato dei messaggi in una coda. In alcuni casi, il sistema operativo chiamerà direttamente una routine della finestra, ignorando la coda.

La terminologia per questa distinzione può essere confusa:

-   La *pubblicazione* di un messaggio indica che il messaggio viene inserito nella coda di messaggi e viene inviato tramite il ciclo di messaggi ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   *Inviando* un messaggio significa che il messaggio ignora la coda e il sistema operativo chiama direttamente la procedura della finestra.

Per il momento, la differenza non è molto importante. La routine della finestra gestisce tutti i messaggi. Tuttavia, alcuni messaggi ignorano la coda e passano direttamente alla routine della finestra. Tuttavia, può fare una differenza se l'applicazione comunica tra le finestre. È possibile trovare una descrizione più approfondita di questo problema nell'argomento [relativo a messaggi e code](/windows/desktop/winmsg/about-messages-and-message-queues)di messaggi.

## <a name="next"></a>Prossima

[Scrittura della routine della finestra](writing-the-window-procedure.md)
