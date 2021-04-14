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
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="1e46a-104">Modulo 1.</span><span class="sxs-lookup"><span data-stu-id="1e46a-104">Module 1.</span></span> <span data-ttu-id="1e46a-105">Il primo programma Windows</span><span class="sxs-lookup"><span data-stu-id="1e46a-105">Your First Windows Program</span></span>

<span data-ttu-id="1e46a-106">In questo modulo verrà scritto un programma desktop di Windows minimo.</span><span class="sxs-lookup"><span data-stu-id="1e46a-106">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="1e46a-107">Viene creata e visualizzata una finestra vuota.</span><span class="sxs-lookup"><span data-stu-id="1e46a-107">All it does is create and show a blank window.</span></span> <span data-ttu-id="1e46a-108">Il primo programma contiene circa 50 righe di codice, senza contare le righe vuote e i commenti.</span><span class="sxs-lookup"><span data-stu-id="1e46a-108">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="1e46a-109">Si tratta del punto di partenza. in seguito verranno aggiunti elementi grafici, testo, input utente e altre funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1e46a-109">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="1e46a-110">Per altri dettagli su come creare un'applicazione desktop di Windows tradizionale in Visual Studio, vedere  [procedura dettagliata: creare un'applicazione desktop di Windows tradizionale (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="1e46a-110">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![screenshot del programma di esempio](images/window01.png)

<span data-ttu-id="1e46a-112">Ecco il codice completo per il programma:</span><span class="sxs-lookup"><span data-stu-id="1e46a-112">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="1e46a-113">È possibile scaricare il progetto di Visual Studio completo dall' [esempio di Windows Hello World](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1e46a-113">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="1e46a-114">Può essere utile fornire una breve descrizione dell'operazione eseguita dal codice.</span><span class="sxs-lookup"><span data-stu-id="1e46a-114">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="1e46a-115">Negli argomenti successivi il codice viene esaminato in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="1e46a-115">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="1e46a-116">**wWinMain** è il punto di ingresso del programma.</span><span class="sxs-lookup"><span data-stu-id="1e46a-116">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="1e46a-117">Quando il programma viene avviato, registra alcune informazioni sul comportamento della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e46a-117">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="1e46a-118">Uno degli elementi più importanti è l'indirizzo di una funzione, denominato `WindowProc` in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="1e46a-118">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="1e46a-119">Questa funzione definisce il comportamento della finestra, ovvero l'aspetto, il modo in cui interagisce con l'utente e così via.</span><span class="sxs-lookup"><span data-stu-id="1e46a-119">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="1e46a-120">Successivamente, il programma crea la finestra e riceve un handle che identifica in modo univoco la finestra.</span><span class="sxs-lookup"><span data-stu-id="1e46a-120">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="1e46a-121">Se la finestra viene creata correttamente, il programma entra in un ciclo **while** .</span><span class="sxs-lookup"><span data-stu-id="1e46a-121">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="1e46a-122">Il programma rimane in questo ciclo fino a quando l'utente non chiude la finestra e non esce dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e46a-122">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="1e46a-123">Si noti che il programma non chiama in modo esplicito la `WindowProc` funzione, anche se è stato detto che la maggior parte della logica dell'applicazione è definita.</span><span class="sxs-lookup"><span data-stu-id="1e46a-123">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="1e46a-124">Windows comunica con il programma passandogli una serie di *messaggi*.</span><span class="sxs-lookup"><span data-stu-id="1e46a-124">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="1e46a-125">Il codice all'interno del ciclo **while** aziona questo processo.</span><span class="sxs-lookup"><span data-stu-id="1e46a-125">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="1e46a-126">Ogni volta che il programma chiama la funzione [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , induce indirettamente Windows a richiamare la funzione WindowProc, una volta per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e46a-126">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e46a-127">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1e46a-127">In this section</span></span>

-   [<span data-ttu-id="1e46a-128">Creazione di una finestra</span><span class="sxs-lookup"><span data-stu-id="1e46a-128">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="1e46a-129">Messaggi finestra</span><span class="sxs-lookup"><span data-stu-id="1e46a-129">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="1e46a-130">Scrittura della routine della finestra</span><span class="sxs-lookup"><span data-stu-id="1e46a-130">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="1e46a-131">Disegno della finestra</span><span class="sxs-lookup"><span data-stu-id="1e46a-131">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="1e46a-132">Chiusura della finestra</span><span class="sxs-lookup"><span data-stu-id="1e46a-132">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="1e46a-133">Gestione dello stato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="1e46a-133">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="1e46a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e46a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e46a-135">Impara a programmare per Windows in C++</span><span class="sxs-lookup"><span data-stu-id="1e46a-135">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="1e46a-136">Esempio di Hello World Windows</span><span class="sxs-lookup"><span data-stu-id="1e46a-136">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
