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
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="f9c4e-105">Modulo 1.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-105">Module 1.</span></span> <span data-ttu-id="f9c4e-106">Il primo programma windows</span><span class="sxs-lookup"><span data-stu-id="f9c4e-106">Your First Windows Program</span></span>

<span data-ttu-id="f9c4e-107">In questo modulo verrà scritto un programma desktop di Windows minimo.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="f9c4e-108">Tutto ciò che fa è creare e visualizzare una finestra vuota.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="f9c4e-109">Questo primo programma contiene circa 50 righe di codice, senza contare righe vuote e commenti.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="f9c4e-110">Sarà il punto di partenza. Successivamente si aggiungeranno grafica, testo, input utente e altre funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="f9c4e-111">Per altre informazioni su come creare un'applicazione desktop windows tradizionale in Visual Studio, vedere Procedura dettagliata: Creare un'applicazione [desktop di Windows tradizionale (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="f9c4e-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![Screenshot del programma di esempio](images/window01.png)

<span data-ttu-id="f9c4e-113">Ecco il codice completo per il programma:</span><span class="sxs-lookup"><span data-stu-id="f9c4e-113">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="f9c4e-114">È possibile scaricare il progetto Visual Studio completo da [Windows Hello World Sample](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f9c4e-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="f9c4e-115">Può essere utile fornire una breve descrizione delle funzioni di questo codice.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="f9c4e-116">Negli argomenti successivi il codice verrà esaminato in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="f9c4e-117">**wWinMain è** il punto di ingresso del programma.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="f9c4e-118">All'avvio del programma vengono registrate alcune informazioni sul comportamento della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="f9c4e-119">Uno degli elementi più importanti è l'indirizzo di una funzione, denominato `WindowProc` in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="f9c4e-120">Questa funzione definisce il comportamento della finestra, ovvero l'aspetto, il modo in cui interagisce con l'utente e così via.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="f9c4e-121">Successivamente, il programma crea la finestra e riceve un handle che identifica in modo univoco la finestra.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="f9c4e-122">Se la finestra viene creata correttamente, il programma entra in un **ciclo while.**</span><span class="sxs-lookup"><span data-stu-id="f9c4e-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="f9c4e-123">Il programma rimane in questo ciclo finché l'utente non chiude la finestra e esce dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="f9c4e-124">Si noti che il programma non chiama in modo esplicito la funzione, anche se in questo caso è definita la maggior parte della `WindowProc` logica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="f9c4e-125">Windows comunica con il programma passando una serie di *messaggi*.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="f9c4e-126">Il codice all'interno **del ciclo while** determina questo processo.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="f9c4e-127">Ogni volta che il programma chiama la [**funzione DispatchMessage,**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) windows richiama indirettamente la funzione WindowProc, una volta per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="f9c4e-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f9c4e-128">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f9c4e-128">In this section</span></span>

-   [<span data-ttu-id="f9c4e-129">Creazione di una finestra</span><span class="sxs-lookup"><span data-stu-id="f9c4e-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="f9c4e-130">Messaggi finestra</span><span class="sxs-lookup"><span data-stu-id="f9c4e-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="f9c4e-131">Scrittura della routine della finestra</span><span class="sxs-lookup"><span data-stu-id="f9c4e-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="f9c4e-132">Disegno della finestra</span><span class="sxs-lookup"><span data-stu-id="f9c4e-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="f9c4e-133">Chiusura della finestra</span><span class="sxs-lookup"><span data-stu-id="f9c4e-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="f9c4e-134">Gestione dello stato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="f9c4e-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="f9c4e-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9c4e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9c4e-136">Informazioni sul programma per Windows in C++</span><span class="sxs-lookup"><span data-stu-id="f9c4e-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="f9c4e-137">Windows Hello World Sample</span><span class="sxs-lookup"><span data-stu-id="f9c4e-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
