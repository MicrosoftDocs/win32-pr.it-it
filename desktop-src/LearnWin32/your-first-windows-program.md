---
title: Modulo 1. Il primo programma Windows
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104568403"
---
# <a name="module-1-your-first-windows-program"></a>Modulo 1. Il primo programma Windows

In questo modulo verrà scritto un programma desktop di Windows minimo. Viene creata e visualizzata una finestra vuota. Il primo programma contiene circa 50 righe di codice, senza contare le righe vuote e i commenti. Si tratta del punto di partenza. in seguito verranno aggiunti elementi grafici, testo, input utente e altre funzionalità.

Per altri dettagli su come creare un'applicazione desktop di Windows tradizionale in Visual Studio, vedere  [procedura dettagliata: creare un'applicazione desktop di Windows tradizionale (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![screenshot del programma di esempio](images/window01.png)

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





È possibile scaricare il progetto di Visual Studio completo dall' [esempio di Windows Hello World](windows-hello-world-sample.md).

Può essere utile fornire una breve descrizione dell'operazione eseguita dal codice. Negli argomenti successivi il codice viene esaminato in dettaglio.

1.  **wWinMain** è il punto di ingresso del programma. Quando il programma viene avviato, registra alcune informazioni sul comportamento della finestra dell'applicazione. Uno degli elementi più importanti è l'indirizzo di una funzione, denominato `WindowProc` in questo esempio. Questa funzione definisce il comportamento della finestra, ovvero l'aspetto, il modo in cui interagisce con l'utente e così via.
2.  Successivamente, il programma crea la finestra e riceve un handle che identifica in modo univoco la finestra.
3.  Se la finestra viene creata correttamente, il programma entra in un ciclo **while** . Il programma rimane in questo ciclo fino a quando l'utente non chiude la finestra e non esce dall'applicazione.

Si noti che il programma non chiama in modo esplicito la `WindowProc` funzione, anche se è stato detto che la maggior parte della logica dell'applicazione è definita. Windows comunica con il programma passandogli una serie di *messaggi*. Il codice all'interno del ciclo **while** aziona questo processo. Ogni volta che il programma chiama la funzione [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , induce indirettamente Windows a richiamare la funzione WindowProc, una volta per ogni messaggio.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Creazione di una finestra](creating-a-window.md)
-   [Messaggi finestra](window-messages.md)
-   [Scrittura della routine della finestra](writing-the-window-procedure.md)
-   [Disegno della finestra](painting-the-window.md)
-   [Chiusura della finestra](closing-the-window.md)
-   [Gestione dello stato di un'applicazione](managing-application-state-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impara a programmare per Windows in C++](learn-to-program-for-windows.md)
</dt> <dt>

[Esempio di Hello World Windows](windows-hello-world-sample.md)
</dt> </dl>

 

 
