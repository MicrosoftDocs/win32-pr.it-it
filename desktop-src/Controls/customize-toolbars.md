---
title: Come personalizzare le barre degli strumenti
description: La maggior parte delle applicazioni basate su Windows utilizza i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104046460"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="f3962-103">Come personalizzare le barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="f3962-103">How to Customize Toolbars</span></span>

<span data-ttu-id="f3962-104">La maggior parte delle applicazioni basate su Windows utilizza i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma.</span><span class="sxs-lookup"><span data-stu-id="f3962-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="f3962-105">Tuttavia, le barre degli strumenti statiche presentano alcune carenze, ad esempio uno spazio troppo piccolo per visualizzare efficacemente tutti gli strumenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="f3962-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="f3962-106">La soluzione a questo problema consiste nel rendere le barre degli strumenti dell'applicazione personalizzabili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f3962-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="f3962-107">Quindi, gli utenti possono scegliere di visualizzare solo gli strumenti necessari e possono organizzarli in modo da adattarli ai propri Workstyle personali.</span><span class="sxs-lookup"><span data-stu-id="f3962-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="f3962-108">Non è possibile personalizzare le barre degli strumenti nelle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f3962-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="f3962-109">Per abilitare la personalizzazione, includere il flag di stile controlli comuni [**\_ regolabili CCS**](common-control-styles.md) quando si crea il controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="f3962-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="f3962-110">Esistono due approcci di base per la personalizzazione:</span><span class="sxs-lookup"><span data-stu-id="f3962-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="f3962-111">Finestra di dialogo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-111">The customization dialog box.</span></span> <span data-ttu-id="f3962-112">Questa finestra di dialogo fornita dal sistema rappresenta l'approccio più semplice.</span><span class="sxs-lookup"><span data-stu-id="f3962-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="f3962-113">Fornisce agli utenti un'interfaccia utente grafica che consente di aggiungere, eliminare o spostare icone.</span><span class="sxs-lookup"><span data-stu-id="f3962-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="f3962-114">Trascinamento e rilascio di strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-114">Dragging and dropping tools.</span></span> <span data-ttu-id="f3962-115">L'implementazione della funzionalità di trascinamento della selezione consente agli utenti di spostare gli strumenti in un'altra posizione sulla barra degli strumenti o di eliminarli trascinandoli dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="f3962-116">Fornisce agli utenti un modo rapido e semplice per organizzare la barra degli strumenti, ma non consente l'aggiunta di strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="f3962-117">È possibile implementare entrambi gli approcci, a seconda delle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="f3962-118">Nessuno di questi due approcci alla personalizzazione fornisce un meccanismo incorporato, ad esempio un pulsante Annulla o Annulla, per ripristinare lo stato precedente della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="f3962-119">Per archiviare lo stato di prepersonalizzazione della barra degli strumenti, è necessario usare in modo esplicito l'API del controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="f3962-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="f3962-120">Se necessario, è possibile utilizzare le informazioni archiviate in un secondo momento per ripristinare lo stato originale della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f3962-121">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f3962-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f3962-122">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f3962-122">Technologies</span></span>

-   [<span data-ttu-id="f3962-123">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="f3962-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f3962-124">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f3962-124">Prerequisites</span></span>

-   <span data-ttu-id="f3962-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="f3962-125">C/C++</span></span>
-   <span data-ttu-id="f3962-126">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="f3962-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f3962-127">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f3962-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="f3962-128">Finestra di dialogo personalizzazione</span><span class="sxs-lookup"><span data-stu-id="f3962-128">Customization Dialog Box</span></span>

<span data-ttu-id="f3962-129">La finestra di dialogo personalizzazione viene fornita dal controllo Toolbar per offrire agli utenti un modo semplice per aggiungere, spostare o eliminare strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="f3962-130">Gli utenti possono avviarlo facendo doppio clic sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="f3962-131">Le applicazioni possono avviare la finestra di dialogo di personalizzazione a livello di programmazione inviando la barra degli strumenti a un messaggio di personalizzazione [**TB \_**](tb-customize.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="f3962-132">Nella figura seguente viene illustrato un esempio della finestra di dialogo di personalizzazione della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![Screenshot di una finestra con una barra degli strumenti a tre elementi e una finestra di dialogo con elenchi dei pulsanti disponibili e correnti della barra degli strumenti](images/tb-customdlg.png)

<span data-ttu-id="f3962-134">Gli strumenti nella casella di riepilogo a destra sono quelli attualmente presenti sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="f3962-135">Inizialmente, questo elenco conterrà gli strumenti specificati quando si crea la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="f3962-136">Nella casella di riepilogo a sinistra sono contenuti gli strumenti che è possibile aggiungere alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="f3962-137">L'applicazione è responsabile del popolamento dell'elenco (ad eccezione del separatore, visualizzato automaticamente).</span><span class="sxs-lookup"><span data-stu-id="f3962-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="f3962-138">Il controllo Toolbar informa l'applicazione che sta avviando una finestra di dialogo di personalizzazione inviando la finestra padre a un codice di notifica [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguito da un codice di notifica [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="f3962-139">Nella maggior parte dei casi, non è necessario che l'applicazione risponda a questi codici di notifica.</span><span class="sxs-lookup"><span data-stu-id="f3962-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="f3962-140">Tuttavia, se non si desidera che la finestra di dialogo Personalizza barra degli strumenti visualizzi un pulsante?, gestire TBN \_ INITCUSTOMIZE restituendo TBNRF \_ HIDEHELP.</span><span class="sxs-lookup"><span data-stu-id="f3962-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="f3962-141">Il controllo Toolbar raccoglie quindi le informazioni necessarie per inizializzare la finestra di dialogo inviando tre serie di codici di notifica, nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="f3962-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="f3962-142">Un codice di notifica [ \_ QUERYINSERT TBN](tbn-queryinsert.md) per ciascun pulsante della barra degli strumenti per determinare dove possono essere inseriti i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f3962-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="f3962-143">Restituisce **false** per impedire l'inserimento di un pulsante a sinistra del pulsante specificato nel messaggio di notifica.</span><span class="sxs-lookup"><span data-stu-id="f3962-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="f3962-144">Se si restituisce **false** a tutti i \_ codici di notifica TBN QUERYINSERT, la finestra di dialogo non verrà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="f3962-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="f3962-145">Un codice di notifica [TBN \_ QUERYDELETE](tbn-querydelete.md) per ogni strumento attualmente sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="f3962-146">Restituisce **true** se è possibile eliminare uno strumento oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f3962-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="f3962-147">Una serie di codici di notifica [ \_ GETBUTTONINFO di TBN](tbn-getbuttoninfo.md) per popolare l'elenco dei pulsanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="f3962-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="f3962-148">Per aggiungere un pulsante all'elenco, compilare la struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che viene passata con il codice di notifica e restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="f3962-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="f3962-149">Quando non sono disponibili altri strumenti da aggiungere, restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="f3962-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="f3962-150">Si noti che è possibile restituire informazioni per i pulsanti già presenti sulla barra degli strumenti. questi pulsanti non verranno aggiunti all'elenco.</span><span class="sxs-lookup"><span data-stu-id="f3962-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="f3962-151">Viene quindi visualizzata la finestra di dialogo e l'utente può iniziare a personalizzare la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="f3962-152">Quando la finestra di dialogo è aperta, l'applicazione può ricevere diversi codici di notifica, a seconda delle azioni dell'utente:</span><span class="sxs-lookup"><span data-stu-id="f3962-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="f3962-153">[TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="f3962-154">L'utente ha modificato il percorso di uno strumento sulla barra degli strumenti o ha aggiunto uno strumento.</span><span class="sxs-lookup"><span data-stu-id="f3962-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="f3962-155">Restituisce **false** per impedire che lo strumento venga inserito in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="f3962-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="f3962-156">[TBN \_ DELETINGBUTTON](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="f3962-157">L'utente sta per rimuovere uno strumento dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="f3962-158">[TBN \_ CUSTHELP](tbn-custhelp.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="f3962-159">L'utente ha fatto clic sul pulsante della guida.</span><span class="sxs-lookup"><span data-stu-id="f3962-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="f3962-160">[TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="f3962-161">L'utente ha aggiunto, spostato o eliminato uno strumento.</span><span class="sxs-lookup"><span data-stu-id="f3962-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="f3962-162">[TBN \_ Reimpostazione](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="f3962-163">L'utente ha fatto clic sul pulsante Reimposta.</span><span class="sxs-lookup"><span data-stu-id="f3962-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="f3962-164">Dopo che la finestra di dialogo viene distrutta, l'applicazione riceverà un codice di notifica [ \_ ENDADJUST TBN](tbn-endadjust.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="f3962-165">Nell'esempio di codice seguente viene illustrato un modo per implementare la personalizzazione della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="f3962-166">Trascinamento e rilascio di strumenti</span><span class="sxs-lookup"><span data-stu-id="f3962-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="f3962-167">Gli utenti possono anche ridisporre i pulsanti di una barra degli strumenti premendo il tasto MAIUSC e trascinando il pulsante in un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="f3962-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="f3962-168">Il processo di trascinamento della selezione viene gestito automaticamente dal controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="f3962-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="f3962-169">Viene visualizzata un'immagine fantasma del pulsante mentre viene trascinata e la barra degli strumenti viene riordinata dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="f3962-170">Gli utenti non possono aggiungere pulsanti in questo modo, ma possono eliminare un pulsante rilasciandolo dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="f3962-171">Sebbene il controllo Toolbar normalmente esegue questa operazione automaticamente, invia anche l'applicazione due codici di notifica: [TBN \_ QUERYDELETE](tbn-querydelete.md) e [TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="f3962-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="f3962-172">Per controllare il processo di trascinamento della selezione, gestire questi codici di notifica come segue:</span><span class="sxs-lookup"><span data-stu-id="f3962-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="f3962-173">Il codice di notifica [ \_ QUERYDELETE di TBN](tbn-querydelete.md) viene inviato non appena l'utente tenta di spostare il pulsante, prima che il pulsante fantasma venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f3962-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="f3962-174">Restituisce **false** per impedire lo spostamento del pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="f3962-175">Se si restituisce **true**, l'utente potrà spostare lo strumento o eliminarlo lasciandolo fuori dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="f3962-176">Se è possibile spostare uno strumento, è possibile eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="f3962-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="f3962-177">Tuttavia, se l'utente elimina uno strumento, il controllo Toolbar invierà all'applicazione un codice di notifica [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) . a questo punto è possibile scegliere di reinserire il pulsante nella posizione originale, annullando quindi l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="f3962-178">Il codice di notifica [ \_ QUERYINSERT di TBN](tbn-queryinsert.md) viene inviato quando l'utente tenta di rilasciare il pulsante sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="f3962-179">Per evitare che il pulsante spostato da un pulsante a sinistra del pulsante specificato nella notifica restituisca **false**.</span><span class="sxs-lookup"><span data-stu-id="f3962-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="f3962-180">Questo codice di notifica non viene inviato se l'utente rilascia lo strumento dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="f3962-181">Se l'utente tenta di trascinare un pulsante senza premere anche il tasto MAIUSC, il controllo Toolbar non gestirà l'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="f3962-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="f3962-182">Tuttavia, invierà all'applicazione un codice di notifica [ \_ BEGINDRAG TBN](tbn-begindrag.md) per indicare l'inizio di un'operazione di trascinamento e un codice di notifica [TBN \_ ENDDRAG](tbn-enddrag.md) per indicare la fine.</span><span class="sxs-lookup"><span data-stu-id="f3962-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="f3962-183">Se si vuole abilitare questa forma di trascinamento della selezione, l'applicazione deve gestire questi codici di notifica, fornire l'interfaccia utente necessaria e modificare la barra degli strumenti per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="f3962-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="f3962-184">Salvataggio e ripristino delle barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="f3962-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="f3962-185">Nel processo di personalizzazione di una barra degli strumenti, è possibile che l'applicazione debba salvare le informazioni in modo da ripristinare lo stato originale della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="f3962-186">Per avviare il salvataggio o il ripristino dello stato di una barra degli strumenti, inviare il controllo Toolbar a [**TB \_ SAVERESTORE**](tb-saverestore.md) messaggio con *lParam* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="f3962-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="f3962-187">Il valore *lParam* di questo messaggio specifica se si richiede un'operazione di salvataggio o di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f3962-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="f3962-188">Una volta inviato il messaggio, esistono due modi per gestire l'operazione di salvataggio/ripristino:</span><span class="sxs-lookup"><span data-stu-id="f3962-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="f3962-189">Con i controlli comuni [versione 4,72](common-control-versions.md) e precedenti, è necessario implementare un gestore [ \_ GETBUTTONINFO TBN](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="f3962-190">Il controllo Toolbar invia questo codice di notifica per richiedere informazioni su ogni pulsante mentre viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="f3962-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="f3962-191">La versione 5,80 include un'opzione Salva/Ripristina.</span><span class="sxs-lookup"><span data-stu-id="f3962-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="f3962-192">All'inizio del processo, quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà un codice di notifica [TBN \_ Save](tbn-save.md) o [TBN \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="f3962-193">Per utilizzare questa opzione, è necessario implementare i gestori delle notifiche per fornire le informazioni sulla bitmap e sullo stato necessarie per salvare o ripristinare lo stato della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="f3962-194">Gli Stati della barra degli strumenti vengono salvati in un flusso di dati costituito da blocchi di dati definiti dalla shell in alternanza con blocchi di dati definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="f3962-195">Un blocco di dati di ogni tipo viene archiviato per ciascun pulsante, insieme a un blocco facoltativo di dati globali che le applicazioni possono inserire all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="f3962-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="f3962-196">Durante il processo di salvataggio, il gestore di [ \_ salvataggio TBN](tbn-save.md) aggiunge i blocchi definiti dall'applicazione al flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="f3962-197">Durante il processo di ripristino, il gestore di [ \_ ripristino TBN](tbn-restore.md) legge ogni blocco e fornisce alla shell le informazioni necessarie per ricostruire la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="f3962-198">Come gestire una notifica di \_ salvataggio TBN</span><span class="sxs-lookup"><span data-stu-id="f3962-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="f3962-199">Il primo codice di notifica di [ \_ salvataggio TBN](tbn-save.md) viene inviato all'inizio del processo di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="f3962-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="f3962-200">Prima di salvare i pulsanti, i membri della struttura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) vengono impostati come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f3962-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="f3962-201">Membro</span><span class="sxs-lookup"><span data-stu-id="f3962-201">Member</span></span>       | <span data-ttu-id="f3962-202">Impostazione</span><span class="sxs-lookup"><span data-stu-id="f3962-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3962-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="f3962-203">**iItem**</span></span>    | <span data-ttu-id="f3962-204">–1</span><span class="sxs-lookup"><span data-stu-id="f3962-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f3962-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="f3962-205">**cbData**</span></span>   | <span data-ttu-id="f3962-206">Quantità di memoria necessaria per i dati definiti dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="f3962-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f3962-207">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="f3962-207">**cButtons**</span></span> | <span data-ttu-id="f3962-208">Numero di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f3962-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f3962-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="f3962-209">**pData**</span></span>    | <span data-ttu-id="f3962-210">Quantità calcolata di memoria necessaria per i dati definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="f3962-211">Si includono in genere alcuni dati globali, oltre ai dati per ogni pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="f3962-212">Aggiungere tale valore a **cbData** e allocare memoria sufficiente a **pData** per contenerlo.</span><span class="sxs-lookup"><span data-stu-id="f3962-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="f3962-213">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="f3962-213">**pCurrent**</span></span> | <span data-ttu-id="f3962-214">Primo byte non usato nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="f3962-215">Se non sono necessarie informazioni sulla barra degli strumenti globali, impostare **pCurrent**  =  **pData** in modo che punti all'inizio del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="f3962-216">Se sono necessarie informazioni sulla barra degli strumenti globali, archiviarle in **pData**, quindi impostare **pCurrent** sull'inizio della parte inutilizzata del flusso di dati prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="f3962-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="f3962-217">Se si desidera aggiungere informazioni sulla barra degli strumenti globali, posizionarlo all'inizio del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="f3962-218">Avanzare **pCurrent** alla fine dei dati globali in modo che punti all'inizio della parte inutilizzata del flusso di dati e restituisca.</span><span class="sxs-lookup"><span data-stu-id="f3962-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="f3962-219">Una volta restituito, la shell inizia a salvare le informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="f3962-220">Aggiunge i dati definiti dalla Shell per il primo pulsante in **pCurrent** , quindi sposta **pCurrent** all'inizio della parte inutilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3962-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="f3962-221">Dopo aver salvato ciascun pulsante, viene inviato un codice di notifica di [ \_ salvataggio TBN](tbn-save.md) e viene restituito [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) con questi membri impostati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f3962-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="f3962-222">Membro</span><span class="sxs-lookup"><span data-stu-id="f3962-222">Member</span></span>                       | <span data-ttu-id="f3962-223">Impostazione</span><span class="sxs-lookup"><span data-stu-id="f3962-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3962-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="f3962-224">**iItem**</span></span>                    | <span data-ttu-id="f3962-225">Indice in base zero del numero del pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="f3962-226">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="f3962-226">**pCurrent**</span></span>                 | <span data-ttu-id="f3962-227">Puntatore al primo byte non usato nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="f3962-228">Se si desidera archiviare informazioni aggiuntive sul pulsante, archiviarle nella posizione a cui punta **pCurrent** e aggiornare **pCurrent** in modo da puntare alla prima parte non utilizzata del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f3962-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="f3962-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="f3962-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="f3962-230">Struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che descrive il pulsante salvato.</span><span class="sxs-lookup"><span data-stu-id="f3962-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="f3962-231">Quando si riceve il codice di notifica, è necessario estrarre tutte le informazioni specifiche del pulsante necessarie da [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span><span class="sxs-lookup"><span data-stu-id="f3962-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="f3962-232">Tenere presente che quando si aggiunge un pulsante, è possibile usare il membro **dwData** di **TBBUTTON** per conservare i dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3962-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="f3962-233">Caricare i dati nel flusso di dati in **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f3962-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="f3962-234">Avanzare **pCurrent** alla fine dei dati, puntando nuovamente all'inizio della parte inutilizzata del flusso e restituire.</span><span class="sxs-lookup"><span data-stu-id="f3962-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="f3962-235">La shell passa quindi al pulsante Avanti, aggiunge le informazioni a **pData**, sposta **PCurrent**, carica [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e invia un altro codice di notifica di [ \_ salvataggio TBN](tbn-save.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="f3962-236">Questo processo continua fino a quando non vengono salvati tutti i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f3962-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="f3962-237">Ripristino delle barre degli strumenti salvate</span><span class="sxs-lookup"><span data-stu-id="f3962-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="f3962-238">Il processo di ripristino Annulla fondamentalmente il processo di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="f3962-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="f3962-239">All'inizio, l'applicazione riceverà un codice di notifica del [ \_ ripristino TBN](tbn-restore.md) con il membro **iItem** della struttura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) impostato su-1.</span><span class="sxs-lookup"><span data-stu-id="f3962-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="f3962-240">Il membro **cbData** è impostato sulla dimensione di **pData** e **cButtons** è impostato sul numero di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f3962-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="f3962-241">Il gestore delle notifiche deve estrarre le informazioni globali inserite all'inizio di **pData** durante il salvataggio e avanzare **pCurrent** all'inizio del primo blocco di dati definiti dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="f3962-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="f3962-242">Impostare **cBytesPerRecord** sulla dimensione dei blocchi di dati usati per salvare i dati dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f3962-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="f3962-243">Impostare **cButtons** sul numero di pulsanti e restituire.</span><span class="sxs-lookup"><span data-stu-id="f3962-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="f3962-244">Il [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) successivo è per il primo pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="f3962-245">Il membro **pCurrent** punta all'inizio del primo blocco di dati dei pulsanti e **iItem** è impostato sull'indice del pulsante.</span><span class="sxs-lookup"><span data-stu-id="f3962-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="f3962-246">Estrarre i dati e avanzare **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f3962-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="f3962-247">Caricare i dati in [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e restituire.</span><span class="sxs-lookup"><span data-stu-id="f3962-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="f3962-248">Per omettere un pulsante dalla barra degli strumenti ripristinata, impostare il membro **idCommand** di **TBBUTTON** su zero.</span><span class="sxs-lookup"><span data-stu-id="f3962-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="f3962-249">La shell ripete il processo per i pulsanti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="f3962-250">Oltre ai messaggi [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) e **NMTBRESTORE** , è inoltre possibile utilizzare messaggi quali [TBN \_ Reset](tbn-reset.md) per salvare e ripristinare una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f3962-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="f3962-251">Nell'esempio di codice seguente viene salvata una barra degli strumenti prima che venga personalizzata e viene ripristinata se l'applicazione riceve un messaggio di [ \_ reimpostazione TBN](tbn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="f3962-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="f3962-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3962-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3962-253">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="f3962-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="f3962-254">**Valori di indice dell'immagine del pulsante standard della barra degli strumenti**</span><span class="sxs-lookup"><span data-stu-id="f3962-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="f3962-255">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f3962-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




