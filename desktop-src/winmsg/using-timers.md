---
description: Questo argomento illustra come creare ed eliminare i timer e come usare un timer per intercettare l'input del mouse a intervalli specificati.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Uso dei timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028309"
---
# <a name="using-timers"></a>Uso dei timer

Questo argomento illustra come creare ed eliminare i timer e come usare un timer per intercettare l'input del mouse a intervalli specificati.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di un timer](#creating-a-timer)
-   [Eliminazione di un timer](#destroying-a-timer)
-   [Uso di funzioni timer per intercettare l'input del mouse](#using-timer-functions-to-trap-mouse-input)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-timer"></a>Creazione di un timer

Nell'esempio seguente viene [**utilizzata la funzione SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) per creare due timer. Il primo timer viene impostato ogni 10 secondi, il secondo ogni cinque minuti.


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



Per elaborare [**i messaggi \_ WM TIMER**](wm-timer.md) generati da questi timer, aggiungere un'istruzione case WM **\_ TIMER** alla routine della finestra per il *parametro hwnd.*


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



Un'applicazione può anche creare un timer i cui messaggi [**WM \_ TIMER**](wm-timer.md) vengono elaborati non dalla routine della finestra principale, ma da una funzione di callback definita dall'applicazione, come nell'esempio di codice seguente, che crea un timer e usa la funzione di callback **MyTimerProc** per elaborare i messaggi **WM \_ TIMER** del timer.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



La convenzione di chiamata **per MyTimerProc** deve essere basata sulla funzione di callback [*TimerProc.*](/windows/win32/api/winuser/nc-winuser-timerproc)

Se l'applicazione crea un timer senza specificare un handle di finestra, l'applicazione deve monitorare la coda di messaggi per i messaggi [**WM \_ TIMER**](wm-timer.md) e inviare i messaggi alla finestra appropriata.


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

Le applicazioni devono usare [**la funzione KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) per eliminare i timer che non sono più necessari. Nell'esempio seguente vengono distrutti i timer identificati dalle costanti IDT \_ TIMER1, IDT \_ TIMER2 e IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Uso di funzioni timer per intercettare l'input del mouse

In alcuni casi è necessario impedire più input quando si ha un puntatore del mouse sullo schermo. Un modo per eseguire questa operazione è creare una routine speciale che intercetta l'input del mouse fino a quando non si verifica un evento specifico. Molti sviluppatori fanno riferimento a questa routine come "creazione di un mousetrap".

Nell'esempio seguente vengono utilizzate le [**funzioni SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) e [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) per intercettare l'input del mouse. **SetTimer crea** un timer che invia un [**messaggio WM \_ TIMER**](wm-timer.md) ogni 10 secondi. Ogni volta che l'applicazione riceve un **messaggio \_ WM TIMER,** registra la posizione del puntatore del mouse. Se la posizione corrente corrisponde alla posizione precedente e la finestra principale dell'applicazione è ridotta a icona, l'applicazione sposta il puntatore del mouse sull'icona. Alla chiusura dell'applicazione, **KillTimer arresta** il timer.


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



Anche se l'esempio seguente illustra anche come intercettare l'input del mouse, elabora il messaggio [**WM \_ TIMER**](wm-timer.md) tramite la funzione di callback definita dall'applicazione **MyTimerProc** anziché tramite la coda di messaggi dell'applicazione.


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

 

 
