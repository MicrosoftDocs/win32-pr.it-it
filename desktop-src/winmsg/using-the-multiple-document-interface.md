---
description: In questa sezione viene illustrato come eseguire attività associate all'interfaccia a più documenti.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Uso dell'interfaccia a più documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317864"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="51d5f-103">Uso dell'interfaccia a più documenti</span><span class="sxs-lookup"><span data-stu-id="51d5f-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="51d5f-104">In questa sezione viene illustrato come eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="51d5f-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="51d5f-105">Registrazione delle classi figlio e della finestra cornice</span><span class="sxs-lookup"><span data-stu-id="51d5f-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="51d5f-106">Creazione di finestre cornice e figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="51d5f-107">Scrittura del ciclo di messaggi principale</span><span class="sxs-lookup"><span data-stu-id="51d5f-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="51d5f-108">Scrittura della routine della finestra cornice</span><span class="sxs-lookup"><span data-stu-id="51d5f-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="51d5f-109">Scrittura della routine della finestra figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="51d5f-110">Creazione di una finestra figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="51d5f-111">Per illustrare queste attività, in questa sezione sono inclusi esempi di MULTIPAD, un'applicazione con interfaccia a documenti multipli (MDI) tipica.</span><span class="sxs-lookup"><span data-stu-id="51d5f-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="51d5f-112">Registrazione delle classi figlio e della finestra cornice</span><span class="sxs-lookup"><span data-stu-id="51d5f-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="51d5f-113">Una tipica applicazione MDI deve registrare due classi finestra: una per la finestra cornice e una per le relative finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="51d5f-114">Se un'applicazione supporta più di un tipo di documento (ad esempio, un foglio di calcolo e un grafico), deve registrare una classe della finestra per ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="51d5f-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="51d5f-115">La struttura della classe per la finestra cornice è simile alla struttura della classe per la finestra principale in applicazioni non MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="51d5f-116">La struttura della classe per le finestre figlio MDI differisce leggermente dalla struttura per le finestre figlio in applicazioni non MDI come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="51d5f-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="51d5f-117">La struttura della classe deve avere un'icona, in quanto l'utente può ridurre a icona una finestra figlio MDI come se fosse una normale finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51d5f-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="51d5f-118">Il nome del menu deve essere **null** perché una finestra figlio MDI non può avere un proprio menu.</span><span class="sxs-lookup"><span data-stu-id="51d5f-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="51d5f-119">La struttura della classe deve riservare ulteriore spazio nella struttura della finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="51d5f-120">Con questo spazio, l'applicazione può associare dati, ad esempio un nome di file, a una particolare finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="51d5f-121">Nell'esempio seguente viene illustrato come MultiPad registra le classi della finestra cornice e figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="51d5f-122">Creazione di finestre cornice e figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="51d5f-123">Una volta registrate le classi della finestra, un'applicazione MDI può crearne le finestre.</span><span class="sxs-lookup"><span data-stu-id="51d5f-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="51d5f-124">Innanzitutto, viene creata la finestra cornice usando la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="51d5f-125">Dopo aver creato la finestra cornice, l'applicazione crea la finestra del client usando di nuovo **CreateWindow** o **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="51d5f-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="51d5f-126">L'applicazione deve specificare MDICLIENT come nome della classe della finestra client; **MdiClient** è una classe di finestra pre-registrata definita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="51d5f-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="51d5f-127">Il parametro *lpvParam* di **CreateWindow** o **CreateWindowEx** deve puntare a una struttura [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="51d5f-128">Questa struttura contiene i membri descritti nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="51d5f-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="51d5f-129">Membro</span><span class="sxs-lookup"><span data-stu-id="51d5f-129">Member</span></span>           | <span data-ttu-id="51d5f-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51d5f-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d5f-131">**hWindowMenu**</span><span class="sxs-lookup"><span data-stu-id="51d5f-131">**hWindowMenu**</span></span>  | <span data-ttu-id="51d5f-132">Handle per il menu finestra utilizzato per il controllo delle finestre figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="51d5f-133">Quando vengono create le finestre figlio, l'applicazione aggiunge i titoli al menu finestra come voci di menu.</span><span class="sxs-lookup"><span data-stu-id="51d5f-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="51d5f-134">L'utente può quindi attivare una finestra figlio facendo clic sul relativo titolo nel menu finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="51d5f-135">**idFirstChild**</span><span class="sxs-lookup"><span data-stu-id="51d5f-135">**idFirstChild**</span></span> | <span data-ttu-id="51d5f-136">Specifica l'identificatore della prima finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="51d5f-137">Alla prima finestra figlio MDI creata viene assegnato questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="51d5f-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="51d5f-138">Ulteriori finestre vengono create con identificatori di finestra incrementati.</span><span class="sxs-lookup"><span data-stu-id="51d5f-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="51d5f-139">Quando una finestra figlio viene distrutta, il sistema riassegna immediatamente gli identificatori della finestra per mantenendone l'intervallo contiguo.</span><span class="sxs-lookup"><span data-stu-id="51d5f-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="51d5f-140">Quando il titolo di una finestra figlio viene aggiunto al menu finestra, il sistema assegna un identificatore alla finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="51d5f-141">Quando l'utente fa clic sul titolo di una finestra figlio, la finestra cornice riceve un messaggio di [**\_ comando WM**](../menurc/wm-command.md) con l'identificatore nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="51d5f-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="51d5f-142">È necessario specificare un valore per il membro **idFirstChild** che non sia in conflitto con gli identificatori di voce di menu nel menu della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="51d5f-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="51d5f-143">La routine della finestra cornice di MULTIPAD crea la finestra client MDI durante l'elaborazione del messaggio [**WM \_ create**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="51d5f-144">Nell'esempio seguente viene illustrato come viene creata la finestra del client.</span><span class="sxs-lookup"><span data-stu-id="51d5f-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="51d5f-145">I titoli delle finestre figlio vengono aggiunti nella parte inferiore del menu finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="51d5f-146">Se l'applicazione aggiunge stringhe al menu della finestra usando la funzione [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , queste stringhe possono essere sovrascritte dai titoli delle finestre figlio quando il menu finestra viene ridisegnato (ogni volta che viene creata o distrutta una finestra figlio).</span><span class="sxs-lookup"><span data-stu-id="51d5f-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="51d5f-147">Un'applicazione MDI che aggiunge stringhe al menu della finestra deve usare la funzione [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) e verificare che i titoli delle finestre figlio non abbiano sovrascritto queste nuove stringhe.</span><span class="sxs-lookup"><span data-stu-id="51d5f-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="51d5f-148">Utilizzare lo stile **WS \_ CLIPCHILDREN** per creare la finestra client MDI per evitare che la finestra venga disegnata sulle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="51d5f-149">Scrittura del ciclo di messaggi principale</span><span class="sxs-lookup"><span data-stu-id="51d5f-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="51d5f-150">Il ciclo di messaggi principale di un'applicazione MDI è simile a quello di un tasto di scelta rapida per la gestione di applicazioni non MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="51d5f-151">La differenza è che il ciclo di messaggi MDI chiama la funzione [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) prima di verificare la presenza di tasti di scelta rapida definiti dall'applicazione o prima di inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="51d5f-152">Nell'esempio seguente viene illustrato il ciclo di messaggi di un'applicazione MDI tipica.</span><span class="sxs-lookup"><span data-stu-id="51d5f-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="51d5f-153">Si noti che [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) può restituire-1 se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="51d5f-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="51d5f-154">La funzione [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) converte i messaggi di [**WM \_ KeyDown**](../inputdev/wm-keydown.md) in messaggi [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) e li invia alla finestra figlio MDI attiva.</span><span class="sxs-lookup"><span data-stu-id="51d5f-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="51d5f-155">Se il messaggio non è un messaggio di accelerazione MDI, la funzione restituisce **false**, nel qual caso l'applicazione usa la funzione [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) per determinare se è stato premuto uno dei tasti di scelta rapida definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51d5f-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="51d5f-156">In caso contrario, il ciclo invia il messaggio alla procedura appropriata della finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="51d5f-157">Scrittura della routine della finestra cornice</span><span class="sxs-lookup"><span data-stu-id="51d5f-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="51d5f-158">La routine della finestra per una finestra cornice MDI è simile a quella della finestra principale di un'applicazione non MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="51d5f-159">La differenza è che una routine della finestra cornice passa tutti i messaggi che non gestisce alla funzione [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) anziché alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="51d5f-160">Inoltre, la routine della finestra cornice deve passare alcuni messaggi gestiti, inclusi quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="51d5f-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="51d5f-161">Message</span><span class="sxs-lookup"><span data-stu-id="51d5f-161">Message</span></span>                                  | <span data-ttu-id="51d5f-162">Risposta</span><span class="sxs-lookup"><span data-stu-id="51d5f-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d5f-163">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="51d5f-164">Attiva la finestra figlio MDI selezionata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="51d5f-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="51d5f-165">Questo messaggio viene inviato quando l'utente sceglie una finestra figlio MDI dal menu finestra della finestra cornice MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="51d5f-166">L'identificatore di finestra associato a questo messaggio identifica la finestra figlio MDI da attivare.</span><span class="sxs-lookup"><span data-stu-id="51d5f-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="51d5f-167">**\_MENUCHAR WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="51d5f-168">Apre il menu finestra della finestra figlio MDI attiva quando l'utente preme la combinazione di tasti ALT + – (meno).</span><span class="sxs-lookup"><span data-stu-id="51d5f-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="51d5f-169">**\_stato attivo WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="51d5f-170">Passa lo stato attivo alla finestra client MDI, che a sua volta la passa alla finestra figlio MDI attiva.</span><span class="sxs-lookup"><span data-stu-id="51d5f-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="51d5f-171">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="51d5f-172">Ridimensiona la finestra del client MDI per adattarla all'area client della nuova finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="51d5f-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="51d5f-173">Se la routine della finestra cornice ridimensiona la finestra del client MDI a una dimensione diversa, non dovrebbe passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="51d5f-174">La routine della finestra cornice in MultiPad è denominata MPFrameWndProc.</span><span class="sxs-lookup"><span data-stu-id="51d5f-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="51d5f-175">La gestione di altri messaggi da parte di MPFrameWndProc è simile a quella delle applicazioni non MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="51d5f-176">[**WM \_**](../menurc/wm-command.md) I messaggi di comando in MultiPad vengono gestiti dalla funzione CommandHandler definita localmente.</span><span class="sxs-lookup"><span data-stu-id="51d5f-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="51d5f-177">Per i messaggi di comando MULTIPAD non gestisce, CommandHandler chiama la funzione [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="51d5f-178">Se MULTIPAD non usa **DefFrameProc** per impostazione predefinita, l'utente non può attivare una finestra figlio dal menu finestra perché il messaggio **di \_ comando WM** inviato facendo clic sulla voce di menu della finestra andrebbe perso.</span><span class="sxs-lookup"><span data-stu-id="51d5f-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="51d5f-179">Scrittura della routine della finestra figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="51d5f-180">Analogamente alla routine della finestra cornice, una routine della finestra figlio MDI utilizza una funzione speciale per elaborare i messaggi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="51d5f-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="51d5f-181">Tutti i messaggi non gestiti dalla routine della finestra figlio devono essere passati alla funzione [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) anziché alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="51d5f-182">Inoltre, alcuni messaggi di gestione delle finestre devono essere passati a **DefMDIChildProc**, anche se l'applicazione gestisce il messaggio, in modo che MDI funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="51d5f-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="51d5f-183">Di seguito sono riportati i messaggi che l'applicazione deve passare a **DefMDIChildProc**.</span><span class="sxs-lookup"><span data-stu-id="51d5f-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="51d5f-184">Message</span><span class="sxs-lookup"><span data-stu-id="51d5f-184">Message</span></span>                                       | <span data-ttu-id="51d5f-185">Risposta</span><span class="sxs-lookup"><span data-stu-id="51d5f-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d5f-186">**\_CHILDACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="51d5f-187">Esegue l'elaborazione dell'attivazione quando le finestre figlio MDI vengono ridimensionate, spostate o visualizzate.</span><span class="sxs-lookup"><span data-stu-id="51d5f-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="51d5f-188">Questo messaggio deve essere passato.</span><span class="sxs-lookup"><span data-stu-id="51d5f-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="51d5f-189">**\_GETMINMAXINFO WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="51d5f-190">Calcola la dimensione di una finestra figlio MDI ingrandita, in base alle dimensioni correnti della finestra del client MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="51d5f-191">**\_MENUCHAR WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="51d5f-192">Passa il messaggio alla finestra cornice MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="51d5f-193">**\_spostamento WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="51d5f-194">Ricalcola le barre di scorrimento del client MDI, se presenti.</span><span class="sxs-lookup"><span data-stu-id="51d5f-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="51d5f-195">**\_stato attivo WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="51d5f-196">Attiva la finestra figlio, se non è la finestra figlio MDI attiva.</span><span class="sxs-lookup"><span data-stu-id="51d5f-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="51d5f-197">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="51d5f-198">Esegue operazioni necessarie per modificare le dimensioni di una finestra, in particolare per massimizzare o ripristinare una finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="51d5f-199">Il mancato passaggio di questo messaggio alla funzione [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produce risultati estremamente indesiderati.</span><span class="sxs-lookup"><span data-stu-id="51d5f-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="51d5f-200">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="51d5f-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="51d5f-201">Comandi di menu della finestra handle (noto in precedenza come sistema): **SC \_ NEXTWINDOW**, **SC \_ PREVWINDOW**, **SC \_ Move**, **SC \_ size** e **SC \_ ingrandire**.</span><span class="sxs-lookup"><span data-stu-id="51d5f-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="51d5f-202">Creazione di una finestra figlio</span><span class="sxs-lookup"><span data-stu-id="51d5f-202">Creating a Child Window</span></span>

<span data-ttu-id="51d5f-203">Per creare una finestra figlio MDI, un'applicazione può chiamare la funzione [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o inviare un messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) alla finestra client MDI.</span><span class="sxs-lookup"><span data-stu-id="51d5f-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="51d5f-204">L'applicazione può utilizzare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con lo stile **WS \_ ex \_ MDIChild** per creare finestre figlio MDI. Un'applicazione MDI a thread singolo può usare entrambi i metodi per creare una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="51d5f-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="51d5f-205">Un thread in un'applicazione MDI multithread deve usare la funzione **CreateMDIWindow** o **CreateWindowEx** per creare una finestra figlio in un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="51d5f-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="51d5f-206">Il parametro *lParam* di un messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) è un puntatore molto lungo a una struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="51d5f-207">La struttura include quattro membri della dimensione: **x** e **y**, che indicano le posizioni orizzontali e verticali della finestra e **CX** e **CY**, che indicano gli extent orizzontali e verticali della finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="51d5f-208">Uno di questi membri può essere assegnato in modo esplicito dall'applicazione oppure può essere impostato su **CW \_ usedefault (**, nel qual caso il sistema seleziona una posizione, una dimensione o entrambi, in base a un algoritmo a cascata.</span><span class="sxs-lookup"><span data-stu-id="51d5f-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="51d5f-209">In ogni caso, è necessario inizializzare tutti e quattro i membri.</span><span class="sxs-lookup"><span data-stu-id="51d5f-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="51d5f-210">MultiPad USA **\_ usedefault (CW** per tutte le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="51d5f-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="51d5f-211">L'ultimo membro della struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) è il membro dello **stile** , che può contenere bit di stile per la finestra.</span><span class="sxs-lookup"><span data-stu-id="51d5f-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="51d5f-212">Per creare una finestra figlio MDI che può avere qualsiasi combinazione di stili di finestra, specificare lo stile della finestra **\_ ALLCHILDSTYLES di MDI** .</span><span class="sxs-lookup"><span data-stu-id="51d5f-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="51d5f-213">Quando questo stile non viene specificato, una finestra figlio MDI dispone degli **stili \_ WS minimizzate**, **WS \_ ingrandite**, **WS \_ HSCROLL** e **WS \_ VSCROLL** come impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="51d5f-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="51d5f-214">MultiPad crea le finestre figlio MDI usando la relativa funzione AddFile definita localmente (che si trova nel file di origine MPFILE. C).</span><span class="sxs-lookup"><span data-stu-id="51d5f-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="51d5f-215">La funzione AddFile imposta il titolo della finestra figlio assegnando il membro **szTitle** della struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) della finestra al nome del file da modificare o a "Untitled".</span><span class="sxs-lookup"><span data-stu-id="51d5f-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="51d5f-216">Il membro **szClass** è impostato sul nome della classe della finestra figlio MDI registrata nella funzione InitializeApplication di MULTIPAD.</span><span class="sxs-lookup"><span data-stu-id="51d5f-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="51d5f-217">Il membro **hOwner** è impostato sull'handle di istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51d5f-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="51d5f-218">Nell'esempio seguente viene illustrata la funzione AddFile in MultiPad.</span><span class="sxs-lookup"><span data-stu-id="51d5f-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="51d5f-219">Il puntatore passato al parametro *lParam* del messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) viene passato alla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e viene visualizzato come primo membro nella struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passato nel messaggio [**WM \_ create**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="51d5f-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="51d5f-220">In MultiPad la finestra figlio si inizializza durante l'elaborazione dei messaggi di **WM \_** , inizializzando le variabili del documento nei dati aggiuntivi e creando la finestra figlio del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="51d5f-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
