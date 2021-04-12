---
title: Impostazione dell'immagine del cursore
description: Impostazione dell'immagine del cursore
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472894"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="71a61-103">Impostazione dell'immagine del cursore</span><span class="sxs-lookup"><span data-stu-id="71a61-103">Setting the Cursor Image</span></span>

<span data-ttu-id="71a61-104">Il *cursore* è l'immagine piccola che mostra la posizione del mouse o di un altro dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="71a61-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="71a61-105">Molte applicazioni modificano l'immagine del cursore per fornire commenti e suggerimenti all'utente.</span><span class="sxs-lookup"><span data-stu-id="71a61-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="71a61-106">Sebbene non sia obbligatorio, aggiunge un bel po' di smalto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71a61-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="71a61-107">Windows fornisce un set di immagini di cursore standard, denominate *cursori di sistema*.</span><span class="sxs-lookup"><span data-stu-id="71a61-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="71a61-108">Sono inclusi la freccia, la mano, l'i-Beam, la clessidra (che è ora un cerchio rotante) e altre.</span><span class="sxs-lookup"><span data-stu-id="71a61-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="71a61-109">In questa sezione viene descritto come utilizzare i cursori di sistema.</span><span class="sxs-lookup"><span data-stu-id="71a61-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="71a61-110">Per attività più avanzate, ad esempio la creazione di cursori personalizzati, vedere [cursori](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="71a61-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="71a61-111">È possibile associare un cursore a una classe della finestra impostando il membro **hCursor** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .</span><span class="sxs-lookup"><span data-stu-id="71a61-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="71a61-112">In caso contrario, il cursore predefinito è la freccia.</span><span class="sxs-lookup"><span data-stu-id="71a61-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="71a61-113">Quando il mouse viene spostato su una finestra, la finestra riceve un messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) (a meno che un'altra finestra non abbia acquisito il mouse).</span><span class="sxs-lookup"><span data-stu-id="71a61-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="71a61-114">A questo punto si verifica uno degli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="71a61-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="71a61-115">L'applicazione imposta il cursore e la routine della finestra restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="71a61-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="71a61-116">L'applicazione non esegue alcuna operazione e passa il [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="71a61-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="71a61-117">Per impostare il cursore, un programma esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="71a61-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="71a61-118">Chiama [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) per caricare il cursore in memoria.</span><span class="sxs-lookup"><span data-stu-id="71a61-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="71a61-119">Questa funzione restituisce un handle per il cursore.</span><span class="sxs-lookup"><span data-stu-id="71a61-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="71a61-120">Chiama il [**cursore**](/windows/desktop/api/winuser/nf-winuser-setcursor) e passa l'handle del cursore.</span><span class="sxs-lookup"><span data-stu-id="71a61-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="71a61-121">In caso contrario, se l'applicazione passa il [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la funzione **DefWindowProc** usa l'algoritmo seguente per impostare l'immagine del cursore:</span><span class="sxs-lookup"><span data-stu-id="71a61-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="71a61-122">Se la finestra dispone di un elemento padre, inviare il messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) al padre da gestire.</span><span class="sxs-lookup"><span data-stu-id="71a61-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="71a61-123">In caso contrario, se la finestra dispone di un cursore della classe, impostare il cursore sul cursore della classe.</span><span class="sxs-lookup"><span data-stu-id="71a61-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="71a61-124">Se non è presente alcun cursore della classe, impostare il cursore sul cursore a freccia.</span><span class="sxs-lookup"><span data-stu-id="71a61-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="71a61-125">La funzione [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) può caricare un cursore personalizzato da una risorsa o uno dei cursori di sistema.</span><span class="sxs-lookup"><span data-stu-id="71a61-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="71a61-126">Nell'esempio seguente viene illustrato come impostare il cursore sul cursore della mano di sistema.</span><span class="sxs-lookup"><span data-stu-id="71a61-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="71a61-127">Se si modifica il cursore, l'immagine del cursore viene reimpostata al successivo spostamento del mouse, a meno che non venga intercettato il messaggio del cursore [**WM \_**](/windows/desktop/menurc/wm-setcursor) e il cursore non venga impostato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="71a61-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="71a61-128">Nel codice seguente viene illustrato come gestire **il \_ secursore WM**.</span><span class="sxs-lookup"><span data-stu-id="71a61-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="71a61-129">Questo codice controlla prima di tutto i 16 bit inferiori di *lParam*.</span><span class="sxs-lookup"><span data-stu-id="71a61-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="71a61-130">Se è `LOWORD(lParam)` uguale a **HTCLIENT**, significa che il cursore si trova sull'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="71a61-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="71a61-131">In caso contrario, il cursore si trova sull'area non client.</span><span class="sxs-lookup"><span data-stu-id="71a61-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="71a61-132">In genere, è consigliabile impostare solo il cursore per l'area client e lasciare che Windows imposti il cursore per l'area non client.</span><span class="sxs-lookup"><span data-stu-id="71a61-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="71a61-133">Prossima</span><span class="sxs-lookup"><span data-stu-id="71a61-133">Next</span></span>

[<span data-ttu-id="71a61-134">Input utente: esempio esteso</span><span class="sxs-lookup"><span data-stu-id="71a61-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 