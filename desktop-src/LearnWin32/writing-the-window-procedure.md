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
# <a name="writing-the-window-procedure"></a><span data-ttu-id="7cb04-103">Scrittura della routine della finestra</span><span class="sxs-lookup"><span data-stu-id="7cb04-103">Writing the Window Procedure</span></span>

<span data-ttu-id="7cb04-104">La [**funzione DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chiama la routine della finestra della finestra che rappresenta la destinazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="7cb04-105">La routine della finestra ha la firma seguente.</span><span class="sxs-lookup"><span data-stu-id="7cb04-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="7cb04-106">Sono disponibili quattro parametri:</span><span class="sxs-lookup"><span data-stu-id="7cb04-106">There are four parameters:</span></span>

- <span data-ttu-id="7cb04-107">*hwnd* è un handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="7cb04-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="7cb04-108">*uMsg è* il codice del messaggio. Ad esempio, il [**messaggio WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica che la finestra è stata ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="7cb04-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="7cb04-109">*wParam* e *lParam* contengono dati aggiuntivi relativi al messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="7cb04-110">Il significato esatto dipende dal codice del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="7cb04-111">**LRESULT** è un valore intero che il programma restituisce a Windows.</span><span class="sxs-lookup"><span data-stu-id="7cb04-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="7cb04-112">Contiene la risposta del programma a un messaggio specifico.</span><span class="sxs-lookup"><span data-stu-id="7cb04-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="7cb04-113">Il significato di questo valore dipende dal codice del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="7cb04-114">**CALLBACK** è la convenzione di chiamata per la funzione.</span><span class="sxs-lookup"><span data-stu-id="7cb04-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="7cb04-115">Una routine di finestra tipica è semplicemente un'istruzione switch di grandi dimensioni che attiva il codice del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="7cb04-116">Aggiungere case per ogni messaggio che si vuole gestire.</span><span class="sxs-lookup"><span data-stu-id="7cb04-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="7cb04-117">I dati aggiuntivi per il messaggio sono contenuti nei *parametri lParam* *e wParam.*</span><span class="sxs-lookup"><span data-stu-id="7cb04-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="7cb04-118">Entrambi i parametri sono valori interi delle dimensioni di una larghezza del puntatore (32 bit o 64 bit).</span><span class="sxs-lookup"><span data-stu-id="7cb04-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="7cb04-119">Il significato di ogni oggetto dipende dal codice del messaggio (*uMsg*).</span><span class="sxs-lookup"><span data-stu-id="7cb04-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="7cb04-120">Per ogni messaggio, è necessario cercare il codice del messaggio in MSDN ed eseguire il cast dei parametri al tipo di dati corretto.</span><span class="sxs-lookup"><span data-stu-id="7cb04-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="7cb04-121">In genere i dati sono un valore numerico o un puntatore a una struttura .</span><span class="sxs-lookup"><span data-stu-id="7cb04-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="7cb04-122">Alcuni messaggi non hanno dati.</span><span class="sxs-lookup"><span data-stu-id="7cb04-122">Some messages do not have any data.</span></span>

<span data-ttu-id="7cb04-123">Ad esempio, la documentazione per il [**messaggio WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica che:</span><span class="sxs-lookup"><span data-stu-id="7cb04-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="7cb04-124">*wParam* è un flag che indica se la finestra è stata ridotta a icona, ingrandita o ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="7cb04-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="7cb04-125">*lParam* contiene la nuova larghezza e altezza della finestra come valori a 16 bit imballati in un numero a 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7cb04-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="7cb04-126">Per ottenere questi valori, è necessario eseguire uno spostamento di bit.</span><span class="sxs-lookup"><span data-stu-id="7cb04-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="7cb04-127">Fortunatamente, il file di intestazione WinDef.h include macro helper a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="7cb04-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="7cb04-128">Una tipica procedura finestra gestisce decine di messaggi, in modo che possa aumentare abbastanza a lungo.</span><span class="sxs-lookup"><span data-stu-id="7cb04-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="7cb04-129">Un modo per rendere il codice più modulare è inserire la logica per la gestione di ogni messaggio in una funzione separata.</span><span class="sxs-lookup"><span data-stu-id="7cb04-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="7cb04-130">Nella routine della finestra eseguire il cast dei *parametri wParam* *e lParam* al tipo di dati corretto e passare tali valori alla funzione.</span><span class="sxs-lookup"><span data-stu-id="7cb04-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="7cb04-131">Ad esempio, per gestire il [**messaggio WM \_ SIZE,**](/windows/desktop/winmsg/wm-size) la routine della finestra sarà simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="7cb04-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

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

<span data-ttu-id="7cb04-132">Le [**macro LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) [**e HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ottengono i valori di larghezza e altezza a 16 bit da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7cb04-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="7cb04-133">È possibile cercare questi tipi di dettagli nella documentazione MSDN per ogni codice del messaggio. La routine della finestra estrae la larghezza e l'altezza e quindi passa questi valori alla `OnSize` funzione .</span><span class="sxs-lookup"><span data-stu-id="7cb04-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="7cb04-134">Gestione dei messaggi predefinita</span><span class="sxs-lookup"><span data-stu-id="7cb04-134">Default Message Handling</span></span>

<span data-ttu-id="7cb04-135">Se non si gestisce un messaggio specifico nella routine della finestra, passare i parametri del messaggio direttamente alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)</span><span class="sxs-lookup"><span data-stu-id="7cb04-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="7cb04-136">Questa funzione esegue l'azione predefinita per il messaggio, che varia in base al tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb04-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="7cb04-137">Evitare colli di bottiglia nella procedura della finestra</span><span class="sxs-lookup"><span data-stu-id="7cb04-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="7cb04-138">Durante l'esecuzione della routine della finestra, blocca tutti gli altri messaggi per le finestre create nello stesso thread.</span><span class="sxs-lookup"><span data-stu-id="7cb04-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="7cb04-139">Pertanto, evitare una lunga elaborazione all'interno della routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="7cb04-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="7cb04-140">Si supponga, ad esempio, che il programma apra una connessione TCP e attenda a tempo indeterminato che il server risponda.</span><span class="sxs-lookup"><span data-stu-id="7cb04-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="7cb04-141">Se lo si fa all'interno della procedura della finestra, l'interfaccia utente non risponderà fino al completamento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="7cb04-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="7cb04-142">Durante questo periodo, la finestra non può elaborare l'input del mouse o della tastiera, ridisegnarsi o persino chiudersi.</span><span class="sxs-lookup"><span data-stu-id="7cb04-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="7cb04-143">È invece consigliabile spostare il lavoro in un altro thread, usando una delle funzionalità di multitasking integrate in Windows:</span><span class="sxs-lookup"><span data-stu-id="7cb04-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="7cb04-144">Creare un nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="7cb04-144">Create a new thread.</span></span>
- <span data-ttu-id="7cb04-145">Usare un pool di thread.</span><span class="sxs-lookup"><span data-stu-id="7cb04-145">Use a thread pool.</span></span>
- <span data-ttu-id="7cb04-146">Usare chiamate di I/O asincrone.</span><span class="sxs-lookup"><span data-stu-id="7cb04-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="7cb04-147">Usare chiamate di routine asincrone.</span><span class="sxs-lookup"><span data-stu-id="7cb04-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="7cb04-148">Prossima</span><span class="sxs-lookup"><span data-stu-id="7cb04-148">Next</span></span>

[<span data-ttu-id="7cb04-149">Disegno della finestra</span><span class="sxs-lookup"><span data-stu-id="7cb04-149">Painting the Window</span></span>](painting-the-window.md)
