---
description: Negli esempi di codice seguenti viene illustrato come eseguire le attività seguenti associate a messaggi e code di messaggi di Windows.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Utilizzo di messaggi e code di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312486"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="2176c-103">Utilizzo di messaggi e code di messaggi</span><span class="sxs-lookup"><span data-stu-id="2176c-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="2176c-104">Negli esempi di codice seguenti viene illustrato come eseguire le attività seguenti associate a messaggi e code di messaggi di Windows.</span><span class="sxs-lookup"><span data-stu-id="2176c-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="2176c-105">Creazione di un ciclo di messaggi</span><span class="sxs-lookup"><span data-stu-id="2176c-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="2176c-106">Esame di una coda di messaggi</span><span class="sxs-lookup"><span data-stu-id="2176c-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="2176c-107">Invio di un messaggio</span><span class="sxs-lookup"><span data-stu-id="2176c-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="2176c-108">Invio di un messaggio</span><span class="sxs-lookup"><span data-stu-id="2176c-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="2176c-109">Creazione di un ciclo di messaggi</span><span class="sxs-lookup"><span data-stu-id="2176c-109">Creating a Message Loop</span></span>

<span data-ttu-id="2176c-110">Il sistema non crea automaticamente una coda di messaggi per ogni thread.</span><span class="sxs-lookup"><span data-stu-id="2176c-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="2176c-111">Il sistema crea invece una coda di messaggi solo per i thread che eseguono operazioni che richiedono una coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="2176c-112">Se il thread crea una o più finestre, è necessario fornire un ciclo di messaggi. Questo ciclo di messaggi recupera i messaggi dalla coda di messaggi del thread e li invia alle procedure appropriate della finestra.</span><span class="sxs-lookup"><span data-stu-id="2176c-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="2176c-113">Poiché il sistema indirizza i messaggi a singole finestre in un'applicazione, è necessario che un thread crei almeno una finestra prima di avviare il ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="2176c-114">La maggior parte delle applicazioni contiene un solo thread che crea finestre.</span><span class="sxs-lookup"><span data-stu-id="2176c-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="2176c-115">Una tipica applicazione registra la classe della finestra principale, crea e Mostra la finestra principale, quindi avvia il ciclo di messaggi, tutto nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="2176c-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="2176c-116">Per creare un ciclo di messaggi, usare le funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="2176c-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="2176c-117">Se l'applicazione deve ottenere l'input di caratteri dall'utente, includere la funzione [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) nel ciclo.</span><span class="sxs-lookup"><span data-stu-id="2176c-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="2176c-118">**TranslateMessage** converte i messaggi di chiave virtuale in messaggi di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="2176c-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="2176c-119">Nell'esempio seguente viene illustrato il ciclo di messaggi nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) di una semplice applicazione basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="2176c-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="2176c-120">Nell'esempio seguente viene illustrato un ciclo di messaggi per un thread che utilizza acceleratori e viene visualizzata una finestra di dialogo non modale.</span><span class="sxs-lookup"><span data-stu-id="2176c-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="2176c-121">Quando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) o [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) restituisce **true** (che indica che il messaggio è stato elaborato), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) non vengono chiamati.</span><span class="sxs-lookup"><span data-stu-id="2176c-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="2176c-122">Il motivo è che **TranslateAccelerator** e **IsDialogMessage** eseguono tutte le operazioni necessarie per la conversione e l'invio dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="2176c-123">Esame di una coda di messaggi</span><span class="sxs-lookup"><span data-stu-id="2176c-123">Examining a Message Queue</span></span>

<span data-ttu-id="2176c-124">Occasionalmente, un'applicazione deve esaminare il contenuto della coda di messaggi di un thread dall'esterno del ciclo di messaggi del thread.</span><span class="sxs-lookup"><span data-stu-id="2176c-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="2176c-125">Se, ad esempio, la routine della finestra di un'applicazione esegue un'operazione di disegno lunga, potrebbe essere necessario che l'utente sia in grado di interrompere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2176c-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="2176c-126">A meno che l'applicazione non esamini periodicamente la coda di messaggi durante l'operazione per i messaggi del mouse e della tastiera, non risponderà all'input dell'utente finché l'operazione non viene completata.</span><span class="sxs-lookup"><span data-stu-id="2176c-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="2176c-127">Il motivo è che la funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nel ciclo di messaggi del thread non viene restituita fino al termine dell'elaborazione di un messaggio da parte della routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="2176c-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="2176c-128">È possibile utilizzare la funzione [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi durante un'operazione di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="2176c-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="2176c-129">**PeekMessage** è simile alla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) . entrambi controllano una coda di messaggi per un messaggio corrispondente ai criteri di filtro, quindi copiano il messaggio in una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) .</span><span class="sxs-lookup"><span data-stu-id="2176c-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="2176c-130">La differenza principale tra le due funzioni è che **GetMessage** non restituisce un risultato fino a quando un messaggio corrispondente ai criteri di filtro non viene inserito nella coda, mentre **PeekMessage** viene restituito immediatamente, indipendentemente dal fatto che un messaggio si trovi nella coda.</span><span class="sxs-lookup"><span data-stu-id="2176c-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="2176c-131">Nell'esempio seguente viene illustrato come utilizzare [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi per i clic del mouse e l'input da tastiera durante un'operazione di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="2176c-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="2176c-132">Altre funzioni, tra cui [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) e [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), consentono anche di esaminare il contenuto della coda di messaggi di un thread.</span><span class="sxs-lookup"><span data-stu-id="2176c-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="2176c-133">**GetQueueStatus** restituisce una matrice di flag che indica i tipi di messaggi nella coda. l'uso di questa soluzione è il modo più rapido per individuare se la coda contiene messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="2176c-134">**GetInputState** restituisce **true** se la coda contiene messaggi relativi al mouse o alla tastiera.</span><span class="sxs-lookup"><span data-stu-id="2176c-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="2176c-135">Entrambe queste funzioni possono essere utilizzate per determinare se la coda contiene messaggi che devono essere elaborati.</span><span class="sxs-lookup"><span data-stu-id="2176c-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="2176c-136">Invio di un messaggio</span><span class="sxs-lookup"><span data-stu-id="2176c-136">Posting a Message</span></span>

<span data-ttu-id="2176c-137">È possibile inviare un messaggio a una coda di messaggi tramite la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="2176c-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="2176c-138">**PostMessage** inserisce un messaggio alla fine della coda di messaggi di un thread e viene restituito immediatamente, senza attendere l'elaborazione del messaggio da parte del thread.</span><span class="sxs-lookup"><span data-stu-id="2176c-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="2176c-139">I parametri della funzione includono un handle di finestra, un identificatore di messaggio e due parametri di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2176c-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="2176c-140">Il sistema copia questi parametri in una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) , compila i membri **Time** e **PT** della struttura e inserisce la struttura nella coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="2176c-141">Il sistema utilizza l'handle di finestra passato con la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per determinare quale coda di messaggi del thread deve ricevere il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2176c-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="2176c-142">Se l'handle è in primo piano **HWND \_**, il sistema invia il messaggio alle code di messaggi del thread di tutte le finestre di primo livello.</span><span class="sxs-lookup"><span data-stu-id="2176c-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="2176c-143">È possibile utilizzare la funzione [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) per inviare un messaggio a una coda di messaggi di thread specifici.</span><span class="sxs-lookup"><span data-stu-id="2176c-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="2176c-144">**PostThreadMessage** è simile a [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), eccetto il primo parametro è un identificatore di thread anziché un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="2176c-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="2176c-145">È possibile recuperare l'identificatore del thread chiamando la funzione [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .</span><span class="sxs-lookup"><span data-stu-id="2176c-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="2176c-146">Utilizzare la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) per uscire da un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="2176c-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="2176c-147">**PostQuitMessage** invia il messaggio [**WM \_ Quit**](wm-quit.md) al thread attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2176c-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="2176c-148">Il ciclo di messaggi del thread termina e restituisce il controllo al sistema quando rileva il messaggio **WM \_ Quit** .</span><span class="sxs-lookup"><span data-stu-id="2176c-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="2176c-149">Un'applicazione in genere chiama **PostQuitMessage** in risposta al messaggio [**WM \_ Destroy**](wm-destroy.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2176c-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="2176c-150">Invio di un messaggio</span><span class="sxs-lookup"><span data-stu-id="2176c-150">Sending a Message</span></span>

<span data-ttu-id="2176c-151">La funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) viene utilizzata per inviare un messaggio direttamente a una routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="2176c-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="2176c-152">**SendMessage** chiama una routine della finestra e attende che la procedura elabori il messaggio e restituisca un risultato.</span><span class="sxs-lookup"><span data-stu-id="2176c-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="2176c-153">Un messaggio può essere inviato a qualsiasi finestra del sistema; è necessario solo un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="2176c-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="2176c-154">Il sistema utilizza l'handle per determinare quale routine della finestra deve ricevere il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2176c-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="2176c-155">Prima di elaborare un messaggio che potrebbe essere stato inviato da un altro thread, una routine della finestra deve prima chiamare la funzione [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) .</span><span class="sxs-lookup"><span data-stu-id="2176c-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="2176c-156">Se questa funzione restituisce **true**, la routine della finestra deve chiamare [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) prima di qualsiasi funzione che induce il thread a produrre il controllo, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2176c-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="2176c-157">È possibile inviare un numero di messaggi ai controlli in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2176c-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="2176c-158">Questi messaggi di controllo impostano l'aspetto, il comportamento e il contenuto dei controlli o recuperano informazioni sui controlli.</span><span class="sxs-lookup"><span data-stu-id="2176c-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="2176c-159">Ad esempio, il messaggio [**CB \_ ADDSTRING**](../controls/cb-addstring.md) può aggiungere una stringa a una casella combinata e il messaggio di controllo [**BM \_**](../controls/bm-setcheck.md) può impostare lo stato di selezione di una casella di controllo o di un pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="2176c-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="2176c-160">Utilizzare la funzione [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) per inviare un messaggio a un controllo, specificando l'identificatore del controllo e l'handle della finestra di dialogo che contiene il controllo.</span><span class="sxs-lookup"><span data-stu-id="2176c-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="2176c-161">Nell'esempio seguente, tratto da una routine della finestra di dialogo, copia una stringa dal controllo di modifica di una casella combinata nella relativa casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2176c-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="2176c-162">Nell'esempio viene usato **SendDlgItemMessage** per inviare un messaggio [**CB \_ ADDSTRING**](../controls/cb-addstring.md) alla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2176c-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
