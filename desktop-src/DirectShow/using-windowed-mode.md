---
description: Uso della modalità finestra
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Uso della modalità finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314380"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="319d7-103">Uso della modalità finestra</span><span class="sxs-lookup"><span data-stu-id="319d7-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="319d7-104">Il [filtro renderer video](video-renderer-filter.md) legacy usa sempre la modalità con finestra.</span><span class="sxs-lookup"><span data-stu-id="319d7-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="319d7-105">Per impostazione predefinita, i filtri VMR-7 e VMR-9 utilizzano la modalità finestra, ma supportano anche la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="319d7-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="319d7-106">In modalità finestra, il renderer video crea la propria finestra in cui dipinge i fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="319d7-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="319d7-107">Se non diversamente specificato, questa finestra è una finestra di primo livello con i bordi e la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="319d7-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="319d7-108">Nella maggior parte dei casi, tuttavia, la finestra video verrà collegata a una finestra dell'applicazione, in modo che il video sia integrato nell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="319d7-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="319d7-109">La procedura da adottare è la seguente:</span><span class="sxs-lookup"><span data-stu-id="319d7-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="319d7-110">Eseguire una query per **IVideoWindow**.</span><span class="sxs-lookup"><span data-stu-id="319d7-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="319d7-111">Impostare la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="319d7-111">Set the parent window.</span></span>
3.  <span data-ttu-id="319d7-112">Imposta nuovi stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="319d7-112">Set new window styles.</span></span>
4.  <span data-ttu-id="319d7-113">Posizionare la finestra del video all'interno della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="319d7-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="319d7-114">Invia una notifica alla finestra video dei \_ messaggi di spostamento WM.</span><span class="sxs-lookup"><span data-stu-id="319d7-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="319d7-115">**Query per IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="319d7-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="319d7-116">Prima di avviare la riproduzione, eseguire una query su Filter Graph Manager per l'interfaccia **IVideoWindow** :</span><span class="sxs-lookup"><span data-stu-id="319d7-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="319d7-117">**Impostare la finestra padre**</span><span class="sxs-lookup"><span data-stu-id="319d7-117">**Set the Parent Window**</span></span>

<span data-ttu-id="319d7-118">Per impostare la finestra padre, chiamare il metodo [**IVideoWindow::p UT \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un handle per la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="319d7-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="319d7-119">Questo metodo accetta una variabile di tipo [**OAHWND**](oahwnd.md), quindi esegue il cast dell'handle a questo tipo:</span><span class="sxs-lookup"><span data-stu-id="319d7-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="319d7-120">**Imposta nuovi stili della finestra**</span><span class="sxs-lookup"><span data-stu-id="319d7-120">**Set New Window Styles**</span></span>

<span data-ttu-id="319d7-121">Modificare lo stile della finestra video chiamando il metodo [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :</span><span class="sxs-lookup"><span data-stu-id="319d7-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="319d7-122">Il \_ flag WS Child imposta la finestra come finestra figlio e il \_ flag WS CLIPSIBLINGS impedisce che la finestra venga disegnata all'interno dell'area client di un'altra finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="319d7-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="319d7-123">**Posizionare la finestra del video**</span><span class="sxs-lookup"><span data-stu-id="319d7-123">**Position the Video Window**</span></span>

<span data-ttu-id="319d7-124">Per impostare la posizione del video rispetto all'area client della finestra dell'applicazione, chiamare il metodo [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="319d7-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="319d7-125">Questo metodo accetta un rettangolo che specifica il bordo sinistro, il bordo superiore, lo spessore e l'altezza della finestra del video.</span><span class="sxs-lookup"><span data-stu-id="319d7-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="319d7-126">Il codice seguente, ad esempio, estende la finestra video per adattarsi all'intera area client della finestra padre:</span><span class="sxs-lookup"><span data-stu-id="319d7-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="319d7-127">Per ottenere la dimensione nativa del video, chiamare il metodo [**IBasicVideo:: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) sul gestore del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="319d7-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="319d7-128">Queste informazioni possono essere usate per ridimensionare il video e mantengono le proporzioni corrette.</span><span class="sxs-lookup"><span data-stu-id="319d7-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="319d7-129">**Rispondere ai \_ messaggi di spostamento WM**</span><span class="sxs-lookup"><span data-stu-id="319d7-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="319d7-130">Per ottenere prestazioni ottimali, è consigliabile inviare una notifica al renderer video ogni volta che la finestra si sposta mentre il grafico è sospeso.</span><span class="sxs-lookup"><span data-stu-id="319d7-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="319d7-131">Chiamare il metodo [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) per inviare il \_ messaggio di spostamento WM:</span><span class="sxs-lookup"><span data-stu-id="319d7-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="319d7-132">Se il renderer utilizza una sovrapposizione hardware, questa notifica determina l'aggiornamento della posizione della sovrapposizione da parte del renderer.</span><span class="sxs-lookup"><span data-stu-id="319d7-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="319d7-133">(VMR-9 non usa le sovrapposizioni, pertanto non è necessario chiamare questo metodo se si usa VMR-9).</span><span class="sxs-lookup"><span data-stu-id="319d7-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="319d7-134">**Pulisci**</span><span class="sxs-lookup"><span data-stu-id="319d7-134">**Clean Up**</span></span>

<span data-ttu-id="319d7-135">Prima della chiusura dell'applicazione, arrestare il grafo e reimpostare il proprietario della finestra video su **null**.</span><span class="sxs-lookup"><span data-stu-id="319d7-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="319d7-136">In caso contrario, i messaggi della finestra potrebbero essere inviati alla finestra sbagliata, che probabilmente causa errori.</span><span class="sxs-lookup"><span data-stu-id="319d7-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="319d7-137">Inoltre, nascondere la finestra video, altrimenti è possibile che lo sfarfallio di un'immagine video venga visualizzato momentaneamente:</span><span class="sxs-lookup"><span data-stu-id="319d7-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="319d7-138">Se l'elemento padre della finestra del video è un elemento figlio della finestra principale dell'applicazione (in altre parole, se la finestra del video è figlio di un figlio), è necessario creare la finestra video usando **CoCreateInstance** e aggiungerla al grafo, anziché consentire a Filter Graph Manager di aggiungere il renderer video durante la [connessione intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="319d7-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="319d7-139">In questo modo si garantisce che la finestra video e la finestra figlio vengano ridisegnate nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="319d7-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="319d7-140">In caso contrario, la finestra figlio può essere disegnata sulla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="319d7-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="319d7-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="319d7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="319d7-142">Rendering video</span><span class="sxs-lookup"><span data-stu-id="319d7-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



