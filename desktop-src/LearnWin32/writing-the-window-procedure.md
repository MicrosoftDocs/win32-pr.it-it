---
title: Scrittura della routine della finestra
description: Scrittura della routine della finestra
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105719"
---
# <a name="writing-the-window-procedure"></a>Scrittura della routine della finestra

La [**funzione DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chiama la routine della finestra della finestra che rappresenta la destinazione del messaggio. La routine della finestra ha la firma seguente.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Sono disponibili quattro parametri:

- *hwnd* è un handle per la finestra.
- *uMsg è* il codice del messaggio. Ad esempio, il [**messaggio WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica che la finestra è stata ridimensionata.
- *wParam* e *lParam* contengono dati aggiuntivi relativi al messaggio. Il significato esatto dipende dal codice del messaggio.

**LRESULT** è un valore intero che il programma restituisce a Windows. Contiene la risposta del programma a un messaggio specifico. Il significato di questo valore dipende dal codice del messaggio. **CALLBACK** è la convenzione di chiamata per la funzione.

Una routine di finestra tipica è semplicemente un'istruzione switch di grandi dimensioni che attiva il codice del messaggio. Aggiungere case per ogni messaggio che si vuole gestire.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

I dati aggiuntivi per il messaggio sono contenuti nei *parametri lParam* *e wParam.* Entrambi i parametri sono valori interi delle dimensioni di una larghezza del puntatore (32 bit o 64 bit). Il significato di ogni oggetto dipende dal codice del messaggio (*uMsg*). Per ogni messaggio, è necessario cercare il codice del messaggio in MSDN ed eseguire il cast dei parametri al tipo di dati corretto. In genere i dati sono un valore numerico o un puntatore a una struttura . Alcuni messaggi non hanno dati.

Ad esempio, la documentazione per il [**messaggio WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica che:

- *wParam* è un flag che indica se la finestra è stata ridotta a icona, ingrandita o ridimensionata.
- *lParam* contiene la nuova larghezza e altezza della finestra come valori a 16 bit imballati in un numero a 32 o 64 bit. Per ottenere questi valori, è necessario eseguire uno spostamento di bit. Fortunatamente, il file di intestazione WinDef.h include macro helper a tale scopo.

Una tipica procedura finestra gestisce decine di messaggi, in modo che possa aumentare abbastanza a lungo. Un modo per rendere il codice più modulare è inserire la logica per la gestione di ogni messaggio in una funzione separata. Nella routine della finestra eseguire il cast dei *parametri wParam* *e lParam* al tipo di dati corretto e passare tali valori alla funzione. Ad esempio, per gestire il [**messaggio WM \_ SIZE,**](/windows/desktop/winmsg/wm-size) la routine della finestra sarà simile alla seguente:

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

Le [**macro LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) [**e HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ottengono i valori di larghezza e altezza a 16 bit da *lParam*. È possibile cercare questi tipi di dettagli nella documentazione MSDN per ogni codice del messaggio. La routine della finestra estrae la larghezza e l'altezza e quindi passa questi valori alla `OnSize` funzione .

## <a name="default-message-handling"></a>Gestione dei messaggi predefinita

Se non si gestisce un messaggio specifico nella routine della finestra, passare i parametri del messaggio direttamente alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Questa funzione esegue l'azione predefinita per il messaggio, che varia in base al tipo di messaggio.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Evitare colli di bottiglia nella procedura della finestra

Durante l'esecuzione della routine della finestra, blocca tutti gli altri messaggi per le finestre create nello stesso thread. Pertanto, evitare una lunga elaborazione all'interno della routine della finestra. Si supponga, ad esempio, che il programma apra una connessione TCP e attenda a tempo indeterminato che il server risponda. Se lo si fa all'interno della procedura della finestra, l'interfaccia utente non risponderà fino al completamento della richiesta. Durante questo periodo, la finestra non può elaborare l'input del mouse o della tastiera, ridisegnarsi o persino chiudersi.

È invece consigliabile spostare il lavoro in un altro thread, usando una delle funzionalità di multitasking integrate in Windows:

- Creare un nuovo thread.
- Usare un pool di thread.
- Usare chiamate di I/O asincrone.
- Usare chiamate di routine asincrone.

## <a name="next"></a>Prossima

[Disegno della finestra](painting-the-window.md)
