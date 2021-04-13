---
description: In questo argomento viene illustrato come creare ed eliminare i timer e come utilizzare un timer per intercettare l'input del mouse a intervalli specificati.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Utilizzo di timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c6479aca9d5394c2ad9ade87dd77b1474f31f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348181"
---
# <a name="using-timers"></a>Utilizzo di timer

In questo argomento viene illustrato come creare ed eliminare i timer e come utilizzare un timer per intercettare l'input del mouse a intervalli specificati.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di un timer](#creating-a-timer)
-   [Eliminazione di un timer](#destroying-a-timer)
-   [Utilizzo di funzioni timer per intercettare l'input del mouse](#using-timer-functions-to-trap-mouse-input)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-timer"></a>Creazione di un timer

Nell'esempio seguente viene utilizzata la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) per creare due timer. Il primo timer viene impostato ogni 10 secondi, il secondo per ogni cinque minuti.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Per elaborare i messaggi del [**\_ timer WM**](wm-timer.md) generati da questi timer, aggiungere un'istruzione case del **\_ timer WM** alla routine della finestra per il parametro *HWND* .


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Un'applicazione può anche creare un timer i cui messaggi del [**\_ timer WM**](wm-timer.md) non vengono elaborati dalla routine della finestra principale ma da una funzione di callback definita dall'applicazione, come nell'esempio di codice seguente, che crea un timer e usa la funzione di callback **MyTimerProc** per elaborare i messaggi del **\_ timer WM** del timer.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



La convenzione di chiamata per **MyTimerProc** deve essere basata sulla funzione di callback [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) .

Se l'applicazione crea un timer senza specificare un handle di finestra, l'applicazione deve monitorare la coda di messaggi per i messaggi del [**\_ timer WM**](wm-timer.md) e inviarli alla finestra appropriata.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Eliminazione di un timer

Le applicazioni devono utilizzare la funzione [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) per eliminare i timer che non sono più necessari. Nell'esempio seguente vengono eliminati i timer identificati dalle costanti IDT \_ Timer1, IDT \_ Timer2 e IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Utilizzo di funzioni timer per intercettare l'input del mouse

A volte è necessario impedire un maggiore input mentre è presente un puntatore del mouse sullo schermo. Un modo per eseguire questa operazione consiste nel creare una routine speciale che intrappola l'input del mouse fino a quando non si verifica un evento specifico. Molti sviluppatori fanno riferimento a questa routine come "creazione di una trappola per topi".

Nell'esempio seguente vengono utilizzate le funzioni [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) e [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) per intercettare l'input del mouse. **Setimer** crea un timer che invia un messaggio di [**\_ timer WM**](wm-timer.md) ogni 10 secondi. Ogni volta che l'applicazione riceve un messaggio di **\_ timer WM** , registra la posizione del puntatore del mouse. Se la posizione corrente è uguale a quella precedente e la finestra principale dell'applicazione è ridotta a icona, l'applicazione sposta il puntatore del mouse sull'icona. Quando l'applicazione viene chiusa, **KillTimer** arresta il timer.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Anche se l'esempio seguente illustra come intercettare l'input del mouse, elabora il messaggio del [**\_ timer WM**](wm-timer.md) tramite la funzione di callback definita dall'applicazione **MyTimerProc**, anziché tramite la coda di messaggi dell'applicazione.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui timer](about-timers.md)
</dt> </dl>

 

 
