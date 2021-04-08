---
title: Uso di tasti di scelta rapida
description: In questa sezione vengono illustrate le attività associate agli acceleratori tastiera.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- input utente, tasti di scelta rapida
- acquisizione dell'input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- acceleratori
- tabelle dei tasti di scelta rapida
- risorse tabella di tasti di scelta rapida
- translate Accelerator (funzione)
- Messaggio WM_COMMAND
- WM_SYS messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046731"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="8d8c4-112">Uso di tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="8d8c4-113">In questa sezione vengono illustrate le attività associate agli acceleratori tastiera.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="8d8c4-114">Uso di una risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="8d8c4-115">Creazione della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="8d8c4-116">Caricamento della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="8d8c4-117">Chiamata della funzione di accelerazione translate</span><span class="sxs-lookup"><span data-stu-id="8d8c4-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="8d8c4-118">Elaborazione \_ dei messaggi di comando WM</span><span class="sxs-lookup"><span data-stu-id="8d8c4-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="8d8c4-119">Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="8d8c4-120">Creazione di acceleratori per gli attributi del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="8d8c4-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="8d8c4-121">Uso di una tabella di tasti di scelta rapida creata in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="8d8c4-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="8d8c4-122">Creazione di una tabella Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="8d8c4-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="8d8c4-123">Elaborazione di acceleratori</span><span class="sxs-lookup"><span data-stu-id="8d8c4-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="8d8c4-124">Eliminazione di una tabella di tasti di scelta rapida Run-Time</span><span class="sxs-lookup"><span data-stu-id="8d8c4-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="8d8c4-125">Creazione di acceleratori modificabili dall'utente</span><span class="sxs-lookup"><span data-stu-id="8d8c4-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="8d8c4-126">Uso di una risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="8d8c4-127">Il modo più comune per aggiungere il supporto acceleratore a un'applicazione consiste nell'includere una risorsa della tabella dei tasti di scelta rapida con il file eseguibile dell'applicazione e quindi caricare la risorsa in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="8d8c4-128">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="8d8c4-129">Creazione della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="8d8c4-130">Caricamento della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="8d8c4-131">Chiamata della funzione di accelerazione translate</span><span class="sxs-lookup"><span data-stu-id="8d8c4-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="8d8c4-132">Elaborazione \_ dei messaggi di comando WM</span><span class="sxs-lookup"><span data-stu-id="8d8c4-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="8d8c4-133">Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="8d8c4-134">Creazione di acceleratori per gli attributi del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="8d8c4-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="8d8c4-135">Creazione della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="8d8c4-136">Si crea una risorsa della tabella di tasti di scelta rapida [usando l'istruzione ACCELERATORS](./accelerators-resource.md) nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="8d8c4-137">È necessario assegnare un nome o un identificatore di risorsa alla tabella dei tasti di scelta rapida, preferibilmente a differenza di quanto avviene per qualsiasi altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="8d8c4-138">Il sistema usa questo identificatore per caricare la risorsa in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="8d8c4-139">Ogni acceleratore definito richiede una voce separata nella tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="8d8c4-140">In ogni voce si definisce la sequenza di tasti (codice carattere ASCII o codice chiave virtuale) che genera l'acceleratore e l'identificatore dell'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="8d8c4-141">È inoltre necessario specificare se la sequenza di tasti deve essere utilizzata in combinazione con i tasti ALT, MAIUSC o CTRL.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="8d8c4-142">Per ulteriori informazioni sulle chiavi virtuali, vedere [input da tastiera](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="8d8c4-143">Una sequenza di tasti ASCII viene specificata racchiudendo il carattere ASCII tra virgolette doppie o usando il valore intero del carattere in combinazione con il flag ASCII.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="8d8c4-144">Gli esempi seguenti illustrano come definire gli acceleratori ASCII.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="8d8c4-145">Una sequenza di tasti del codice a chiave virtuale viene specificata in modo diverso a seconda che la sequenza di tasti sia una chiave alfanumerica o una chiave non alfanumerica.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="8d8c4-146">Per una chiave alfanumerica, la lettera o il numero della chiave, racchiuso tra virgolette doppie, viene combinato con il flag **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="8d8c4-147">Per una chiave non alfanumerica, il codice della chiave virtuale per la chiave specifica viene combinato con il flag **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="8d8c4-148">Negli esempi seguenti viene illustrato come definire gli acceleratori del codice a chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="8d8c4-149">Nell'esempio seguente viene illustrata una risorsa della tabella dei tasti di scelta rapida che definisce acceleratori per le operazioni sui file.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="8d8c4-150">Il nome della risorsa è *FileAccel*.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="8d8c4-151">Se si desidera che l'utente prema ALT, MAIUSC o CTRL in una combinazione con la sequenza di tasti di scelta rapida, specificare i flag ALT, MAIUSC e CONTROL nella definizione dell'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="8d8c4-152">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="8d8c4-153">Per impostazione predefinita, quando un tasto di scelta rapida corrisponde a una voce di menu, il sistema evidenzia la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="8d8c4-154">È possibile usare il flag **noinverte** per impedire l'evidenziazione per un singolo acceleratore.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="8d8c4-155">Nell'esempio seguente viene illustrato come utilizzare il flag **noinverte** :</span><span class="sxs-lookup"><span data-stu-id="8d8c4-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="8d8c4-156">Per definire acceleratori che corrispondono alle voci di menu nell'applicazione, includere gli acceleratori nel testo delle voci di menu.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="8d8c4-157">Nell'esempio seguente viene illustrato come includere acceleratori nel testo di una voce di menu in un file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="8d8c4-158">Caricamento della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="8d8c4-159">Un'applicazione carica una risorsa della tabella dei tasti di scelta rapida chiamando la funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) e specificando l'handle dell'istanza per l'applicazione il cui file eseguibile contiene la risorsa e il nome o l'identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="8d8c4-160">**LoadAccelerators** carica la tabella dei tasti di scelta rapida specificata in memoria e restituisce l'handle alla tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="8d8c4-161">Un'applicazione può caricare una risorsa della tabella dei tasti di scelta rapida in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="8d8c4-162">In genere, un'applicazione a thread singolo carica la tabella dei tasti di scelta rapida prima di immettere il ciclo di messaggi principale.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="8d8c4-163">Un'applicazione che usa più thread in genere carica la risorsa della tabella di tasti di scelta rapida per un thread prima di immettere il ciclo di messaggi per il thread.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="8d8c4-164">Un'applicazione o un thread potrebbe inoltre utilizzare più tabelle di tasti di scelta rapida, ciascuna associata a una particolare finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="8d8c4-165">Tale applicazione caricherà la tabella dei tasti di scelta rapida per la finestra ogni volta che l'utente ha attivato la finestra.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="8d8c4-166">Per ulteriori informazioni sui thread, vedere [processi e thread](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="8d8c4-167">Chiamata della funzione di accelerazione translate</span><span class="sxs-lookup"><span data-stu-id="8d8c4-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="8d8c4-168">Per elaborare gli acceleratori, il ciclo di messaggi di un'applicazione (o di un thread) deve contenere una chiamata alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="8d8c4-169">**TranslateAccelerator** Confronta le sequenze di tasti con una tabella dei tasti di scelta rapida e, se trova una corrispondenza, traduce le sequenze di tasti in un messaggio [**WM \_**](wm-command.md) (o [**WM \_ SYSCOMMAND**](wm-syscommand.md)).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="8d8c4-170">La funzione Invia quindi il messaggio a una routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="8d8c4-171">I parametri della funzione **TranslateAccelerator** includono l'handle per la finestra che deve ricevere i messaggi di **\_ comando WM** , l'handle alla tabella dei tasti di scelta rapida utilizzata per convertire gli acceleratori e un puntatore a [**una struttura di messaggi contenente**](/windows/win32/api/winuser/ns-winuser-msg) un messaggio dalla coda.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="8d8c4-172">Nell'esempio seguente viene illustrato come chiamare **TranslateAccelerator** dall'interno di un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="8d8c4-173">Elaborazione \_ dei messaggi di comando WM</span><span class="sxs-lookup"><span data-stu-id="8d8c4-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="8d8c4-174">Quando si usa un tasto di scelta rapida, la finestra specificata nella funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) riceve un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="8d8c4-175">La parola inferiore del parametro *wParam* contiene l'identificatore del tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="8d8c4-176">La routine della finestra esamina l'identificatore per determinare l'origine del messaggio **del \_ comando WM** ed elabora il messaggio di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="8d8c4-177">In genere, se un tasto di scelta rapida corrisponde a una voce di menu nell'applicazione, all'acceleratore e alla voce di menu viene assegnato lo stesso identificatore.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="8d8c4-178">Se è necessario sapere se un messaggio [**di \_ comando WM**](wm-command.md) è stato generato da un acceleratore o da una voce di menu, è possibile esaminare la parola più ordinata del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="8d8c4-179">Se un tasto di scelta rapida ha generato il messaggio, la parola più ordinata è 1; Se una voce di menu ha generato il messaggio, la parola più ordinata è 0.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="8d8c4-180">Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d8c4-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="8d8c4-181">Il sistema elimina automaticamente le risorse della tabella dei tasti di scelta rapida caricate dalla funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , rimuovendo la risorsa dalla memoria dopo la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="8d8c4-182">Creazione di acceleratori per gli attributi del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="8d8c4-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="8d8c4-183">Nell'esempio riportato in questa sezione viene illustrato come eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d8c4-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="8d8c4-184">Creare una risorsa della tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="8d8c4-185">Caricare la tabella dei tasti di scelta rapida in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="8d8c4-186">Tradurre gli acceleratori in un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="8d8c4-187">Elabora i messaggi di [**\_ comando WM**](wm-command.md) generati dagli acceleratori.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="8d8c4-188">Queste attività vengono illustrate nel contesto di un'applicazione che include un menu di **caratteri** e gli acceleratori corrispondenti che consentono all'utente di selezionare gli attributi del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="8d8c4-189">La parte seguente di un file di definizione delle risorse definisce il menu dei **caratteri** e la tabella dei tasti di scelta rapida associata.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="8d8c4-190">Si noti che le voci di menu mostrano le sequenze di tasti di scelta rapida e che ogni acceleratore ha lo stesso identificatore della voce di menu associata.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="8d8c4-191">Le sezioni seguenti del file di origine dell'applicazione mostrano come implementare gli acceleratori.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="8d8c4-192">Uso di una tabella di tasti di scelta rapida creata in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="8d8c4-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="8d8c4-193">In questo argomento viene illustrato come utilizzare le tabelle di tasti di scelta rapida create in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="8d8c4-194">Creazione di una tabella Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="8d8c4-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="8d8c4-195">Elaborazione di acceleratori</span><span class="sxs-lookup"><span data-stu-id="8d8c4-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="8d8c4-196">Eliminazione di una tabella di tasti di scelta rapida Run-Time</span><span class="sxs-lookup"><span data-stu-id="8d8c4-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="8d8c4-197">Creazione di acceleratori modificabili dall'utente</span><span class="sxs-lookup"><span data-stu-id="8d8c4-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="8d8c4-198">Creazione di una tabella Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="8d8c4-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="8d8c4-199">Il primo passaggio per la creazione di una tabella di tasti di scelta rapida in fase di esecuzione consiste nel compilare una matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="8d8c4-200">Ogni struttura della matrice definisce un tasto di scelta rapida nella tabella.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="8d8c4-201">La definizione di un acceleratore include i relativi flag, la relativa chiave e il relativo identificatore.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="8d8c4-202">La struttura **Accel** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="8d8c4-203">Si definisce la sequenza di tasti di un acceleratore specificando un codice carattere ASCII o un codice di chiave virtuale nel membro **chiave** della struttura di [**accelerazione**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="8d8c4-204">Se si specifica un codice a chiave virtuale, è necessario prima includere il flag **FVIRTKEY** nel membro **fVirt** . in caso contrario, il sistema interpreta il codice come un codice carattere ASCII.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="8d8c4-205">È possibile includere il flag **FCONTROL**, **Falt** o **FSHIFT** , o tutti e tre, per combinare il tasto CTRL, ALT o MAIUSC con la sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="8d8c4-206">Per creare la tabella dei tasti di scelta rapida, passare un puntatore alla matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) alla funzione [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="8d8c4-207">**CreateAcceleratorTable** crea la tabella dei tasti di scelta rapida e restituisce l'handle alla tabella.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="8d8c4-208">Elaborazione di acceleratori</span><span class="sxs-lookup"><span data-stu-id="8d8c4-208">Processing Accelerators</span></span>

<span data-ttu-id="8d8c4-209">Il processo di caricamento e chiamata di acceleratori forniti da una tabella di tasti di scelta rapida creata in fase di esecuzione è identico all'elaborazione di quelli forniti da una risorsa della tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="8d8c4-210">Per altre informazioni, vedere [caricamento della risorsa della tabella dei tasti di scelta rapida tramite l'](#loading-the-accelerator-table-resource) [elaborazione \_ dei messaggi di comando WM](/windows).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="8d8c4-211">Eliminazione di una tabella di tasti di scelta rapida Run-Time</span><span class="sxs-lookup"><span data-stu-id="8d8c4-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="8d8c4-212">Il sistema elimina automaticamente le tabelle dei tasti di scelta rapida create in fase di esecuzione, rimuovendo le risorse dalla memoria dopo la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="8d8c4-213">È possibile eliminare una tabella di tasti di scelta rapida e rimuoverla dalla memoria prima passando l'handle della tabella alla funzione [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="8d8c4-214">Creazione di acceleratori modificabili dall'utente</span><span class="sxs-lookup"><span data-stu-id="8d8c4-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="8d8c4-215">Questo esempio illustra come creare una finestra di dialogo che consente all'utente di modificare il tasto di scelta rapida associato a una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="8d8c4-216">La finestra di dialogo è costituita da una casella combinata che contiene voci di menu, una casella combinata contenente i nomi delle chiavi e caselle di controllo per la selezione dei tasti CTRL, ALT e MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="8d8c4-217">Nella figura seguente viene illustrata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-217">The following illustration shows the dialog box.</span></span>

![finestra di dialogo con caselle combinate e caselle di controllo](images/useredit.gif)

<span data-ttu-id="8d8c4-219">Nell'esempio seguente viene illustrato il modo in cui la finestra di dialogo viene definita nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="8d8c4-220">La barra dei menu dell'applicazione contiene un sottomenu **carattere** i cui elementi sono associati ad acceleratori.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="8d8c4-221">I valori delle voci di menu per il modello di menu sono costanti definite come indicato di seguito nel file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="8d8c4-222">Nella finestra di dialogo viene utilizzata una matrice di strutture VKEY definite dall'applicazione, ciascuna contenente una stringa di testo della sequenza di tasti e una stringa di testo del tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="8d8c4-223">Quando viene creata, la finestra di dialogo analizza la matrice e aggiunge ogni stringa di testo della sequenza di tasti alla casella combinata **Seleziona sequenza di tasti** .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="8d8c4-224">Quando l'utente fa clic sul pulsante **OK** , la finestra di dialogo Cerca la stringa di testo della sequenza di tasti selezionata e recupera la stringa di testo dell'acceleratore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="8d8c4-225">La finestra di dialogo aggiunge la stringa di testo acceleratore al testo della voce di menu selezionata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="8d8c4-226">Nell'esempio seguente viene illustrata la matrice di strutture VKEY:</span><span class="sxs-lookup"><span data-stu-id="8d8c4-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="8d8c4-227">La procedura di inizializzazione della finestra di dialogo Compila l' **elemento SELECT** e seleziona le caselle combinate della **sequenza di tasti** .</span><span class="sxs-lookup"><span data-stu-id="8d8c4-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="8d8c4-228">Dopo che l'utente ha selezionato una voce di menu e un tasto di scelta rapida associato, nella finestra di dialogo vengono esaminati i controlli della finestra di dialogo per ottenere la selezione dell'utente, viene aggiornato il testo della voce di menu e quindi viene creata una nuova tabella dei tasti di scelta rapida che contiene il nuovo acceleratore definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="8d8c4-229">Nell'esempio seguente viene illustrata la routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="8d8c4-230">Si noti che è necessario inizializzare nella routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 