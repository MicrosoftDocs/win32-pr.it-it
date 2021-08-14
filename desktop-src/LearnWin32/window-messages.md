---
title: Messaggi finestra (Informazioni di base con Win32 e C++)
description: Messaggi finestra (Informazioni di base con Win32 e C++)
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e3655ddbd053cf9f84b4298518c4616679e83fe1eb48fb60011e865ca8a605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387514"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Messaggi finestra (Informazioni di base con Win32 e C++)

Un'applicazione GUI deve rispondere agli eventi dell'utente e del sistema operativo.

- **Gli eventi dell'utente** includono tutti i modi in cui un utente può interagire con il programma: clic del mouse, tasti di scelta, movimenti del touchscreen e così via.
- **Gli eventi del sistema operativo includono** qualsiasi elemento "esterno" al programma che può influire sul comportamento del programma. Ad esempio, l'utente potrebbe collegare un nuovo dispositivo hardware o Windows potrebbe entrare in uno stato di risparmio energia inferiore (sospensione o ibernazione).

Questi eventi possono verificarsi in qualsiasi momento mentre il programma è in esecuzione, in quasi tutti gli ordini. Come si struttura un programma il cui flusso di esecuzione non può essere previsto in anticipo?

Per risolvere questo problema, Windows usa un modello a passaggio di messaggi. Il sistema operativo comunica con la finestra dell'applicazione passando messaggi. Un messaggio è semplicemente un codice numerico che definisce un evento specifico. Ad esempio, se l'utente preme il pulsante sinistro del mouse, la finestra riceve un messaggio con il codice di messaggio seguente.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Ad alcuni messaggi sono associati dati. Ad esempio, il [**messaggio \_ WM LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) include la coordinata x e la coordinata y del cursore del mouse.

Per passare un messaggio a una finestra, il sistema operativo chiama la routine della finestra registrata per tale finestra. Ora si conosce la procedura della finestra.

## <a name="the-message-loop"></a>Ciclo del messaggio

Un'applicazione riceverà migliaia di messaggi durante l'esecuzione. Tenere presente che ogni pressione di tasti e clic con il pulsante del mouse genera un messaggio. Inoltre, un'applicazione può avere più finestre, ognuna con una propria routine della finestra. In che modo il programma riceve tutti questi messaggi e li recapita alla procedura di finestra corretta? L'applicazione richiede un ciclo per recuperare i messaggi e inviare i messaggi alle finestre corrette.

Per ogni thread che crea una finestra, il sistema operativo crea una coda per i messaggi della finestra. Questa coda contiene i messaggi per tutte le finestre create nel thread. La coda stessa è nascosta dal programma. Non è possibile modificare direttamente la coda. Tuttavia, è possibile eseguire il pull di un messaggio dalla coda chiamando la [**funzione GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage)

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Questa funzione rimuove il primo messaggio dall'inizio della coda. Se la coda è vuota, la funzione si blocca fino a quando non viene accodato un altro messaggio. Il fatto che [**i blocchi GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) non rispettino il programma. Se non sono presenti messaggi, il programma non deve eseguire alcuna operazione. Se è necessario eseguire l'elaborazione in background, è possibile creare thread aggiuntivi che continuano a essere eseguiti mentre **GetMessage** attende un altro messaggio. Vedere [Avoiding Bottlenecks in Your Window Procedure (Evitare](writing-the-window-procedure.md)colli di bottiglia nella procedura della finestra).

Il primo parametro di [**GetMessage è**](/windows/desktop/api/winuser/nf-winuser-getmessage) l'indirizzo di una [**struttura MSG.**](/windows/win32/api/winuser/ns-winuser-msg) Se la funzione ha esito positivo, inserisce nella **struttura MSG** le informazioni sul messaggio. Sono inclusi la finestra di destinazione e il codice del messaggio. Gli altri tre parametri consentono di filtrare i messaggi ricevuti dalla coda. In quasi tutti i casi, questi parametri verranno impostati su zero.

Anche se [**la struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) contiene informazioni sul messaggio, quasi mai si esaminerà direttamente questa struttura. Verrà invece passato direttamente ad altre due funzioni.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

La [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) è correlata all'input da tastiera. Converte le sequenze di tasti (tasto giù, tasto su) in caratteri. Non è necessario conoscere il funzionamento di questa funzione. ricordarsi di chiamarlo prima di [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Il collegamento alla documentazione MSDN contiene altre informazioni, se si desidera.

La [**funzione DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) indica al sistema operativo di chiamare la routine della finestra della finestra che rappresenta la destinazione del messaggio. In altre parole, il sistema operativo cerca l'handle di finestra nella relativa tabella di finestre, trova il puntatore a funzione associato alla finestra e richiama la funzione .

Si supponga, ad esempio, che l'utente premo il pulsante sinistro del mouse. Ciò causa una catena di eventi:

1. Il sistema operativo inserisce [**un messaggio \_ LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) nella coda di messaggi.
2. Il programma chiama la [**funzione GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage)
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) estrae [**il messaggio WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) dalla coda e inserisce la [**struttura MSG.**](/windows/win32/api/winuser/ns-winuser-msg)
4. Il programma chiama le [**funzioni TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) [**e DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)
5. [**All'interno di DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), il sistema operativo chiama la routine della finestra.
6. La routine della finestra può rispondere al messaggio o ignorarlo.

Quando la routine della finestra viene restituita, torna a [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Viene restituito al ciclo di messaggi per il messaggio successivo. Finché il programma è in esecuzione, i messaggi continueranno ad arrivare nella coda. Pertanto, è necessario disporre di un ciclo che estrae continuamente i messaggi dalla coda e li invia. È possibile pensare al ciclo come a eseguire le operazioni seguenti:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Come scritto, naturalmente, questo ciclo non terminerebbe mai. A questo punto entra in funzione il valore restituito per la funzione [**GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage) In **genere, GetMessage** restituisce un valore diverso da zero. Per uscire dall'applicazione ed uscire dal ciclo di messaggi, chiamare la [**funzione PostQuitMessage.**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)

```C++
        PostQuitMessage(0);
```

La [**funzione PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) inserisce [**un messaggio WM \_ QUIT**](/windows/desktop/winmsg/wm-quit) nella coda di messaggi. **WM \_ QUIT** è un messaggio speciale: [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) restituisce zero, segnalando la fine del ciclo di messaggi. Ecco il ciclo di messaggi modificato.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Se [**GetMessage restituisce**](/windows/desktop/api/winuser/nf-winuser-getmessage) un valore diverso da zero, l'espressione nel **ciclo while** restituisce true. Dopo aver chiamato [**PostQuitMessage,**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)l'espressione diventa false e il programma esce dal ciclo. Un risultato interessante di questo comportamento è che la routine della finestra non riceve mai un [**messaggio WM \_ QUIT.**](/windows/desktop/winmsg/wm-quit) Pertanto, non è necessario disporre di un'istruzione case per questo messaggio nella routine della finestra.

La domanda ovvia successiva è quando chiamare [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Si tornerà a questa domanda nell'argomento [Chiusura della](closing-the-window.md)finestra , ma prima è necessario scrivere la procedura della finestra.

## <a name="posted-messages-versus-sent-messages"></a>Messaggi inviati e messaggi inviati

La sezione precedente ha parlato di messaggi che vengono inviati a una coda. In alcuni casi, il sistema operativo chiamerà direttamente una routine della finestra, ignorando la coda.

La terminologia di questa distinzione può generare confusione:

-   *L'inserimento* di un messaggio indica che il messaggio viene inviato nella coda di messaggi e viene inviato tramite il ciclo di messaggi ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   *L'invio* di un messaggio significa che il messaggio ignora la coda e il sistema operativo chiama direttamente la routine della finestra.

Per il momento, la differenza non è molto importante. La routine della finestra gestisce tutti i messaggi. Tuttavia, alcuni messaggi ignorano la coda e passano direttamente alla procedura della finestra. Tuttavia, può fare la differenza se l'applicazione comunica tra finestre. È possibile trovare una descrizione più approfondita di questo problema nell'argomento [About Messages and Message Queues](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="next"></a>Prossima

[Scrittura della routine della finestra](writing-the-window-procedure.md)
