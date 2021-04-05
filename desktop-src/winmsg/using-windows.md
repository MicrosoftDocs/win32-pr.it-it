---
description: Negli esempi di questa sezione viene descritto come eseguire le attività associate all'utilizzo di Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Utilizzo di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884633"
---
# <a name="using-windows"></a><span data-ttu-id="f958b-103">Utilizzo di Windows</span><span class="sxs-lookup"><span data-stu-id="f958b-103">Using Windows</span></span>

<span data-ttu-id="f958b-104">Negli esempi di questa sezione viene descritto come eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="f958b-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="f958b-105">Creazione di una finestra principale</span><span class="sxs-lookup"><span data-stu-id="f958b-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="f958b-106">Creazione, enumerazione e ridimensionamento di finestre figlio</span><span class="sxs-lookup"><span data-stu-id="f958b-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="f958b-107">Eliminazione di una finestra</span><span class="sxs-lookup"><span data-stu-id="f958b-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="f958b-108">Uso di finestre sovrapposte</span><span class="sxs-lookup"><span data-stu-id="f958b-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="f958b-109">Creazione di una finestra principale</span><span class="sxs-lookup"><span data-stu-id="f958b-109">Creating a Main Window</span></span>

<span data-ttu-id="f958b-110">La prima finestra creata da un'applicazione è in genere la finestra principale.</span><span class="sxs-lookup"><span data-stu-id="f958b-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="f958b-111">Per creare la finestra principale, usare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra, il nome della finestra, gli stili della finestra, le dimensioni, la posizione, l'handle di menu, l'handle dell'istanza e i dati di creazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="f958b-112">Una finestra principale appartiene a una classe di finestra definita dall'applicazione, quindi è necessario registrare la classe della finestra e fornire una routine della finestra per la classe prima di creare la finestra principale.</span><span class="sxs-lookup"><span data-stu-id="f958b-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="f958b-113">La maggior parte delle applicazioni usa in genere lo stile [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) per creare la finestra principale.</span><span class="sxs-lookup"><span data-stu-id="f958b-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="f958b-114">Questo stile assegna alla finestra una barra del titolo, un menu finestra, un bordo di ridimensionamento e i pulsanti Riduci a icona e Ingrandisci.</span><span class="sxs-lookup"><span data-stu-id="f958b-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="f958b-115">La funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) restituisce un handle che identifica in modo univoco la finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="f958b-116">Nell'esempio seguente viene creata una finestra principale che appartiene a una classe di finestra definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="f958b-117">Il nome della finestra, la **finestra principale**, verrà visualizzato sulla barra del titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="f958b-118">Combinando gli [**stili \_ WS VSCROLL**](window-styles.md) e **WS \_ HSCROLL** con lo stile **WS \_ OVERLAPPEDWINDOW** , l'applicazione crea una finestra principale con barre di scorrimento orizzontali e verticali oltre ai componenti forniti dallo stile **WS \_ OVERLAPPEDWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="f958b-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="f958b-119">Le quattro occorrenze della costante **\_ usedefault (CW** impostano le dimensioni e la posizione iniziali della finestra sui valori predefiniti definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f958b-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="f958b-120">Specificando **null** anziché un handle di menu, nella finestra sarà definito il menu per la classe Window.</span><span class="sxs-lookup"><span data-stu-id="f958b-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="f958b-121">Si noti che nell'esempio precedente viene chiamata la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) dopo la creazione della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="f958b-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="f958b-122">Questa operazione viene eseguita perché il sistema non visualizza automaticamente la finestra principale dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="f958b-123">Passando il flag **SW \_ SHOWDEFAULT** a **ShowWindow**, l'applicazione consente al programma che ha avviato l'applicazione di impostare lo stato di visualizzazione iniziale della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="f958b-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="f958b-124">La funzione [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) invia alla finestra il primo messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="f958b-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="f958b-125">Creazione, enumerazione e ridimensionamento di finestre figlio</span><span class="sxs-lookup"><span data-stu-id="f958b-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="f958b-126">È possibile dividere l'area client di una finestra in aree funzionali diverse utilizzando le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="f958b-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="f958b-127">La creazione di una finestra figlio è simile alla creazione di una finestra principale: si usa la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="f958b-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="f958b-128">Per creare una finestra di una classe di finestra definita dall'applicazione, è necessario registrare la classe della finestra e fornire una routine della finestra prima di creare la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f958b-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="f958b-129">È necessario assegnare alla finestra figlio lo stile [**WS \_ child**](window-styles.md) e specificare una finestra padre per la finestra figlio al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="f958b-130">Nell'esempio seguente l'area client della finestra principale di un'applicazione viene divisa in tre aree funzionali creando tre finestre figlio di uguale dimensione.</span><span class="sxs-lookup"><span data-stu-id="f958b-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="f958b-131">Ogni finestra figlio ha la stessa altezza dell'area client della finestra principale, ma ogni finestra è la cui larghezza è pari a un terzo.</span><span class="sxs-lookup"><span data-stu-id="f958b-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="f958b-132">La finestra principale crea le finestre figlio in risposta al messaggio [**WM \_ create**](wm-create.md) , che la finestra principale riceve durante il processo di creazione di una finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="f958b-133">Poiché ogni finestra figlio ha lo stile del [**\_ bordo WS**](window-styles.md) , ognuno ha un bordo sottile.</span><span class="sxs-lookup"><span data-stu-id="f958b-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="f958b-134">Inoltre, poiché non è specificato lo stile di visualizzazione **WS \_** , ogni finestra figlio viene inizialmente nascosta.</span><span class="sxs-lookup"><span data-stu-id="f958b-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="f958b-135">Si noti inoltre che a ogni finestra figlio viene assegnato un identificatore della finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f958b-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="f958b-136">La finestra principale ridimensiona e posiziona le finestre figlio in risposta al messaggio [**di \_ dimensioni WM**](wm-size.md) , che la finestra principale riceve quando cambiano le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f958b-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="f958b-137">In risposta a **\_ dimensioni WM**, la finestra principale recupera le dimensioni dell'area client usando la funzione [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) e quindi passa le dimensioni alla funzione [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) .</span><span class="sxs-lookup"><span data-stu-id="f958b-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="f958b-138">**EnumChildWindows** passa l'handle a ogni finestra figlio, a sua volta, alla funzione di callback [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="f958b-139">Questa funzione ridimensiona e posiziona ogni finestra figlio chiamando la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) . le dimensioni e la posizione sono basate sulle dimensioni dell'area client della finestra principale e sull'identificatore della finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f958b-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="f958b-140">Successivamente, **EnumChildProc** chiama la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) per rendere visibile la finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="f958b-141">Eliminazione di una finestra</span><span class="sxs-lookup"><span data-stu-id="f958b-141">Destroying a Window</span></span>

<span data-ttu-id="f958b-142">Per eliminare una finestra, è possibile usare la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="f958b-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="f958b-143">In genere, un'applicazione invia il messaggio di [**\_ chiusura WM**](wm-close.md) prima di eliminare una finestra, offrendo alla finestra la possibilità di chiedere conferma all'utente prima che la finestra venga distrutta.</span><span class="sxs-lookup"><span data-stu-id="f958b-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="f958b-144">Una finestra che include un menu finestra riceve automaticamente il messaggio di **\_ chiusura WM** quando l'utente fa clic su **Chiudi** dal menu finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="f958b-145">Se l'utente conferma che la finestra deve essere distrutta, l'applicazione chiama **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="f958b-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="f958b-146">Il sistema invia il messaggio [**WM \_ Destroy**](wm-destroy.md) alla finestra dopo averlo rimosso dalla schermata.</span><span class="sxs-lookup"><span data-stu-id="f958b-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="f958b-147">In risposta a **WM \_ Destroy**, la finestra Salva i dati e libera tutte le risorse allocate.</span><span class="sxs-lookup"><span data-stu-id="f958b-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="f958b-148">Una finestra principale conclude l'elaborazione di **WM \_ Destroy** chiamando la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) per uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="f958b-149">Nell'esempio seguente viene illustrato come richiedere la conferma dell'utente prima di eliminare una finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="f958b-150">In risposta a [**WM \_ Close**](wm-close.md), nell'esempio viene visualizzata una finestra di dialogo che contiene i pulsanti **Sì**, **No** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="f958b-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="f958b-151">Se l'utente fa clic su **Sì**, viene chiamato [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . in caso contrario, la finestra non viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="f958b-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="f958b-152">Poiché la finestra distrutta è una finestra principale, l'esempio chiama [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in risposta a [**WM \_ Destroy**](wm-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="f958b-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="f958b-153">Uso di finestre sovrapposte</span><span class="sxs-lookup"><span data-stu-id="f958b-153">Using Layered Windows</span></span>

<span data-ttu-id="f958b-154">Per fare in modo che una finestra di dialogo venga visualizzata come finestra traslucida, creare innanzitutto la finestra di dialogo come di consueto.</span><span class="sxs-lookup"><span data-stu-id="f958b-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="f958b-155">Quindi, su [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), impostare il bit a più livelli dello stile esteso della finestra e chiamare [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) con il valore alfa desiderato.</span><span class="sxs-lookup"><span data-stu-id="f958b-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="f958b-156">Il codice potrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f958b-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="f958b-157">Si noti che il terzo parametro di [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) è un valore compreso tra 0 e 255, con 0 rendendo la finestra completamente trasparente e 255 rendendola completamente opaca.</span><span class="sxs-lookup"><span data-stu-id="f958b-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="f958b-158">Questo parametro simula la [**BlendFunction**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) più versatile della funzione [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="f958b-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="f958b-159">Per rendere questa finestra completamente opaca, rimuovere il bit **WS \_ ex \_ sovrapposto** chiamando [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e quindi chiedere di ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="f958b-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="f958b-160">La rimozione del bit si desidera per informare il sistema che può liberare memoria associata a livelli e reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="f958b-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="f958b-161">Il codice potrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f958b-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="f958b-162">Per utilizzare le finestre figlio sovrapposte, l'applicazione deve dichiarare se stessa Windows 8 nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="f958b-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
