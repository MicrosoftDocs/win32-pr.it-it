---
title: Modulo 1. Il primo programma windows
description: Modulo 1. Il primo programma windows
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110949"
---
# <a name="module-1-your-first-windows-program"></a>Modulo 1. Il primo programma windows

In questo modulo verrà scritto un programma desktop di Windows minimo. Tutto ciò che fa è creare e visualizzare una finestra vuota. Questo primo programma contiene circa 50 righe di codice, senza contare righe vuote e commenti. Sarà il punto di partenza. Successivamente si aggiungeranno grafica, testo, input utente e altre funzionalità.

Per altre informazioni su come creare un'applicazione desktop windows tradizionale in Visual Studio, vedere Procedura dettagliata: Creare un'applicazione [desktop di Windows tradizionale (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)

![Screenshot del programma di esempio](images/window01.png)

Ecco il codice completo per il programma:


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





È possibile scaricare il progetto Visual Studio completo da [Windows Hello World Sample](windows-hello-world-sample.md).

Può essere utile fornire una breve descrizione delle funzioni di questo codice. Negli argomenti successivi il codice verrà esaminato in dettaglio.

1.  **wWinMain è** il punto di ingresso del programma. All'avvio del programma vengono registrate alcune informazioni sul comportamento della finestra dell'applicazione. Uno degli elementi più importanti è l'indirizzo di una funzione, denominato `WindowProc` in questo esempio. Questa funzione definisce il comportamento della finestra, ovvero l'aspetto, il modo in cui interagisce con l'utente e così via.
2.  Successivamente, il programma crea la finestra e riceve un handle che identifica in modo univoco la finestra.
3.  Se la finestra viene creata correttamente, il programma entra in un **ciclo while.** Il programma rimane in questo ciclo finché l'utente non chiude la finestra e esce dall'applicazione.

Si noti che il programma non chiama in modo esplicito la funzione, anche se in questo caso è definita la maggior parte della `WindowProc` logica dell'applicazione. Windows comunica con il programma passando una serie di *messaggi*. Il codice all'interno **del ciclo while** determina questo processo. Ogni volta che il programma chiama la [**funzione DispatchMessage,**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) windows richiama indirettamente la funzione WindowProc, una volta per ogni messaggio.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Creazione di una finestra](creating-a-window.md)
-   [Messaggi finestra](window-messages.md)
-   [Scrittura della routine della finestra](writing-the-window-procedure.md)
-   [Disegno della finestra](painting-the-window.md)
-   [Chiusura della finestra](closing-the-window.md)
-   [Gestione dello stato di un'applicazione](managing-application-state-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul programma per Windows in C++](learn-to-program-for-windows.md)
</dt> <dt>

[Windows Hello World Sample](windows-hello-world-sample.md)
</dt> </dl>

 

 
