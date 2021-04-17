---
title: Scrittura della routine della finestra
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299680"
---
# <a name="writing-the-window-procedure"></a>Scrittura della routine della finestra

La funzione [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chiama la routine della finestra che rappresenta la destinazione del messaggio. La procedura della finestra ha la firma seguente:

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Sono disponibili quattro parametri:

- *HWND* è un handle per la finestra.
- *uMsg* è il codice del messaggio. ad esempio, il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) indica che la finestra è stata ridimensionata.
- *wParam* e *lParam* contengono dati aggiuntivi relativi al messaggio. Il significato esatto dipende dal codice del messaggio.

**LRESULT** è un valore intero che il programma restituisce a Windows. Contiene la risposta del programma a un particolare messaggio. Il significato di questo valore dipende dal codice del messaggio. Il **callback** è la convenzione di chiamata per la funzione.

Una tipica routine della finestra è semplicemente un'istruzione switch di grandi dimensioni che attiva il codice del messaggio. Aggiungere i case per ogni messaggio che si desidera gestire.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

I dati aggiuntivi per il messaggio sono contenuti nei parametri *lParam* e *wParam* . Entrambi i parametri sono valori integer le cui dimensioni corrispondono a una larghezza del puntatore (32 bit o 64 bit). Il significato di ogni dipende dal codice del messaggio (*uMsg*). Per ogni messaggio, sarà necessario cercare il codice del messaggio su MSDN ed eseguire il cast dei parametri al tipo di dati corretto. In genere i dati sono un valore numerico o un puntatore a una struttura. Alcuni messaggi non contengono dati.

Ad esempio, la documentazione per il [**messaggio \_ dimensioni WM**](/windows/desktop/winmsg/wm-size) dichiara che:

- *wParam* è un flag che indica se la finestra è stata ridotta a icona, ingrandita o ridimensionata.
- *lParam* contiene la nuova larghezza e l'altezza della finestra come valori a 16 bit compressi in un numero di 1 32 o 64 bit. Per ottenere questi valori, è necessario eseguire uno spostamento di bit. Fortunatamente, il file di intestazione WinDef. h include le macro helper che eseguono questa operazione.

Una routine di finestra tipica gestisce dozzine di messaggi, pertanto può aumentare molto tempo. Un modo per rendere più modulare il codice consiste nell'inserire la logica per la gestione di ogni messaggio in una funzione separata. Nella procedura della finestra eseguire il cast dei parametri *wParam* e *lParam* al tipo di dati corretto e passare tali valori alla funzione. Per gestire il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) , ad esempio, la routine della finestra avrà un aspetto simile al seguente:

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

Le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ottengono i valori di larghezza e altezza a 16 bit da *lParam*. È possibile cercare questi tipi di dettagli nella documentazione di MSDN per ogni codice del messaggio. La routine della finestra estrae la larghezza e l'altezza, quindi passa questi valori alla `OnSize` funzione.

## <a name="default-message-handling"></a>Gestione dei messaggi predefinita

Se non si gestisce un messaggio specifico nella routine della finestra, passare i parametri del messaggio direttamente alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Questa funzione esegue l'azione predefinita per il messaggio, che varia in base al tipo di messaggio.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Evitare colli di bottiglia nella routine della finestra

Mentre viene eseguita la routine della finestra, blocca tutti gli altri messaggi per Windows creati sullo stesso thread. Pertanto, evitare una lunga elaborazione all'interno della routine della finestra. Si supponga, ad esempio, che il programma apra una connessione TCP e attenda indefinitamente che il server risponda. Se si esegue questa operazione all'interno della routine della finestra, l'interfaccia utente non risponderà finché non verrà completata la richiesta. Durante questo intervallo di tempo, la finestra non può elaborare l'input del mouse o della tastiera, ridisegnare o addirittura chiudere.

È invece consigliabile spostare il lavoro in un altro thread, usando una delle funzionalità multitasking predefinite in Windows:

- Creare un nuovo thread.
- Usare un pool di thread.
- Utilizzare chiamate di I/O asincrone.
- Utilizzare chiamate di procedura asincrone.

## <a name="next"></a>Prossima

[Disegno della finestra](painting-the-window.md)