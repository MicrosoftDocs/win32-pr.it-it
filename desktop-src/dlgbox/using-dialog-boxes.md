---
title: Utilizzo delle finestre di dialogo
description: Usare le finestre di dialogo per visualizzare le informazioni e richiedere l'input dell'utente.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interfaccia utente di Windows, Windowing
- Interfaccia utente di Windows, finestre di dialogo
- finestre, finestre di dialogo
- finestre di dialogo, informazioni
- finestre di dialogo, visualizzazione
- finestre di dialogo modali
- finestre di dialogo non modali
- finestre di dialogo, modali
- finestre di dialogo, non modale
- finestre di dialogo, inizializzazione
- modelli di finestra di dialogo
- finestre di dialogo, modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047173"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="61d76-115">Utilizzo delle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="61d76-115">Using Dialog Boxes</span></span>

<span data-ttu-id="61d76-116">Usare le finestre di dialogo per visualizzare le informazioni e richiedere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="61d76-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="61d76-117">L'applicazione carica e inizializza la finestra di dialogo, elabora l'input dell'utente ed elimina la finestra di dialogo quando l'utente termina l'attività.</span><span class="sxs-lookup"><span data-stu-id="61d76-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="61d76-118">Il processo per la gestione delle finestre di dialogo varia a seconda che la finestra di dialogo sia modale o non modale.</span><span class="sxs-lookup"><span data-stu-id="61d76-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="61d76-119">Per una finestra di dialogo modale è necessario che l'utente chiuda la finestra di dialogo prima di attivare un'altra finestra nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="61d76-120">Tuttavia, l'utente può attivare Windows in applicazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="61d76-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="61d76-121">Una finestra di dialogo non modale non richiede una risposta immediata da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="61d76-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="61d76-122">È simile a una finestra principale contenente i controlli.</span><span class="sxs-lookup"><span data-stu-id="61d76-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="61d76-123">Nelle sezioni seguenti viene illustrato come utilizzare entrambi i tipi di finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="61d76-124">Visualizzazione di una finestra di messaggio</span><span class="sxs-lookup"><span data-stu-id="61d76-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="61d76-125">Creazione di una finestra di dialogo modale</span><span class="sxs-lookup"><span data-stu-id="61d76-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="61d76-126">Creazione di una finestra di dialogo non modale</span><span class="sxs-lookup"><span data-stu-id="61d76-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="61d76-127">Inizializzazione di una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="61d76-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="61d76-128">Creazione di un modello in memoria</span><span class="sxs-lookup"><span data-stu-id="61d76-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="61d76-129">Visualizzazione di una finestra di messaggio</span><span class="sxs-lookup"><span data-stu-id="61d76-129">Displaying a Message Box</span></span>

<span data-ttu-id="61d76-130">Il formato più semplice della finestra di dialogo modale è la finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="61d76-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="61d76-131">La maggior parte delle applicazioni usa le finestre di messaggio per avvisare l'utente degli errori e per richiedere indicazioni su come procedere in seguito a un errore.</span><span class="sxs-lookup"><span data-stu-id="61d76-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="61d76-132">Per creare una finestra di messaggio, è possibile utilizzare la funzione [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , specificando il messaggio e il numero e il tipo di pulsanti da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="61d76-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="61d76-133">Il sistema crea una finestra di dialogo modale che fornisce il proprio modello di finestra di dialogo e la relativa procedura.</span><span class="sxs-lookup"><span data-stu-id="61d76-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="61d76-134">Dopo che l'utente ha chiuso la finestra di messaggio **MessageBox** o **MessageBoxEx** restituisce un valore che identifica il pulsante scelto dall'utente per chiudere la finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="61d76-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="61d76-135">Nell'esempio seguente, l'applicazione visualizza una finestra di messaggio che richiede all'utente di un'azione dopo che si è verificata una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="61d76-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="61d76-136">Nella finestra di messaggio viene visualizzato il messaggio che descrive la condizione di errore e come risolverlo.</span><span class="sxs-lookup"><span data-stu-id="61d76-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="61d76-137">Lo stile **MB \_ YesNo** indica a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) di fornire due pulsanti con cui l'utente può scegliere come procedere:</span><span class="sxs-lookup"><span data-stu-id="61d76-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="61d76-138">La figura seguente mostra l'output dell'esempio di codice precedente:</span><span class="sxs-lookup"><span data-stu-id="61d76-138">The following image shows the output from the preceding code example:</span></span>

![MessageBox](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="61d76-140">Creazione di una finestra di dialogo modale</span><span class="sxs-lookup"><span data-stu-id="61d76-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="61d76-141">Per creare una finestra di dialogo modale, utilizzare la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="61d76-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="61d76-142">È necessario specificare l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="61d76-143">La funzione **DialogBox** carica il modello, Visualizza la finestra di dialogo ed elabora tutti gli input utente fino a quando l'utente non chiude la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="61d76-144">Nell'esempio seguente, l'applicazione visualizza una finestra di dialogo modale quando l'utente fa clic su **Elimina elemento** dal menu di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="61d76-145">La finestra di dialogo contiene un controllo di modifica (in cui l'utente immette il nome di un elemento) e i pulsanti **OK** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="61d76-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="61d76-146">Gli identificatori di controllo per questi controlli sono \_ rispettivamente ID itemName, IDOK e IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="61d76-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="61d76-147">La prima parte dell'esempio è costituita dalle istruzioni che creano la finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="61d76-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="61d76-148">Queste istruzioni, nella procedura della finestra principale dell'applicazione, creano la finestra di dialogo quando il sistema riceve un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con l'identificatore del \_ menu IDM DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="61d76-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="61d76-149">La seconda parte dell'esempio è la routine della finestra di dialogo, che recupera il contenuto del controllo di modifica e chiude la finestra di dialogo al momento della ricezione di un messaggio di **\_ comando WM** .</span><span class="sxs-lookup"><span data-stu-id="61d76-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="61d76-150">Nelle istruzioni seguenti viene creata la finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="61d76-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="61d76-151">Il modello della finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="61d76-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="61d76-152">In questo esempio, l'applicazione specifica la finestra principale come finestra proprietaria per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="61d76-153">Quando il sistema visualizza inizialmente la finestra di dialogo, la relativa posizione è relativa all'angolo superiore sinistro dell'area client della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="61d76-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="61d76-154">L'applicazione usa il valore restituito da [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) per determinare se procedere con l'operazione o annullarlo.</span><span class="sxs-lookup"><span data-stu-id="61d76-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="61d76-155">Le istruzioni seguenti definiscono la routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="61d76-156">In questo esempio, la procedura usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) per recuperare il testo corrente dal controllo di modifica identificato da ID \_ ItemName.</span><span class="sxs-lookup"><span data-stu-id="61d76-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="61d76-157">La procedura chiama quindi la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per impostare il valore restituito della finestra di dialogo su IDOK o IDCANCEL, a seconda del messaggio ricevuto e per iniziare il processo di chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="61d76-158">Gli identificatori IDOK e IDCANCEL corrispondono ai pulsanti **OK** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="61d76-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="61d76-159">Dopo che la stored procedure ha chiamato **EndDialog**, il sistema invia messaggi aggiuntivi alla procedura per eliminare la finestra di dialogo e restituisce nuovamente il valore restituito della finestra di dialogo alla funzione che ha creato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="61d76-160">Creazione di una finestra di dialogo non modale</span><span class="sxs-lookup"><span data-stu-id="61d76-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="61d76-161">Per creare una finestra di dialogo non modale, utilizzare la funzione [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , specificando l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="61d76-162">**CreateDialog** carica il modello, crea la finestra di dialogo e, facoltativamente, lo Visualizza.</span><span class="sxs-lookup"><span data-stu-id="61d76-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="61d76-163">L'applicazione è responsabile del recupero e dell'invio di messaggi di input utente alla routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="61d76-164">Nell'esempio seguente, l'applicazione visualizza una finestra di dialogo non modale, se non è già visualizzata, quando l'utente fa clic **su Vai a** dal menu di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="61d76-165">La finestra di dialogo contiene un controllo di modifica, una casella di controllo e pulsanti **OK** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="61d76-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="61d76-166">Il modello della finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="61d76-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="61d76-167">L'utente immette un numero di riga nel controllo di modifica e controlla la casella di controllo per specificare che il numero di riga è relativo alla riga corrente.</span><span class="sxs-lookup"><span data-stu-id="61d76-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="61d76-168">Gli identificatori di controllo sono ID \_ line, ID \_ ABSREL, IDOK e IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="61d76-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="61d76-169">Le istruzioni nella prima parte dell'esempio creano la finestra di dialogo non modale.</span><span class="sxs-lookup"><span data-stu-id="61d76-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="61d76-170">Queste istruzioni, nella procedura della finestra principale dell'applicazione, creano la finestra di dialogo quando la routine della finestra riceve un messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) con l' \_ identificatore del menu IDM goto, ma solo se la variabile globale non contiene già un handle valido.</span><span class="sxs-lookup"><span data-stu-id="61d76-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="61d76-171">La seconda parte dell'esempio è il ciclo di messaggi principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="61d76-172">Il ciclo include la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) per garantire che l'utente possa usare l'interfaccia della tastiera della finestra di dialogo in questa finestra di dialogo non modale.</span><span class="sxs-lookup"><span data-stu-id="61d76-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="61d76-173">La terza parte dell'esempio è la routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="61d76-174">La procedura consente di recuperare il contenuto del controllo di modifica e della casella di controllo quando l'utente fa clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="61d76-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="61d76-175">La procedura elimina la finestra di dialogo quando l'utente fa clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="61d76-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="61d76-176">Nelle istruzioni precedenti, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) viene chiamato solo se `hwndGoto` non contiene un handle di finestra valido.</span><span class="sxs-lookup"><span data-stu-id="61d76-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="61d76-177">In questo modo si garantisce che l'applicazione non visualizzi due finestre di dialogo nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="61d76-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="61d76-178">Per supportare questo metodo di controllo, la routine della finestra di dialogo deve impostare su **null** quando elimina la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="61d76-179">Il ciclo di messaggi di un'applicazione è costituito dalle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="61d76-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="61d76-180">Il ciclo controlla la validità dell'handle di finestra nella finestra di dialogo e chiama solo la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) se l'handle è valido.</span><span class="sxs-lookup"><span data-stu-id="61d76-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="61d76-181">**IsDialogMessage** elabora il messaggio solo se appartiene alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="61d76-182">In caso contrario, restituisce **false** e il ciclo invia il messaggio alla finestra appropriata.</span><span class="sxs-lookup"><span data-stu-id="61d76-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="61d76-183">Le istruzioni seguenti definiscono la routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="61d76-184">Nelle istruzioni precedenti, la procedura elabora i messaggi di [**\_ comando**](/windows/desktop/menurc/wm-command) [**WM \_ INITDIALOG**](wm-initdialog.md) e WM.</span><span class="sxs-lookup"><span data-stu-id="61d76-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="61d76-185">Durante l'elaborazione di **WM \_ INITDIALOG** , la routine inizializza la casella di controllo passando il valore corrente della variabile globale a [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span><span class="sxs-lookup"><span data-stu-id="61d76-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="61d76-186">La procedura restituisce **true** per indicare al sistema di impostare lo stato attivo per l'input predefinito.</span><span class="sxs-lookup"><span data-stu-id="61d76-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="61d76-187">Durante l'elaborazione del [**\_ comando WM**](/windows/desktop/menurc/wm-command) , la procedura chiude la finestra di dialogo solo se l'utente fa clic sul pulsante **Annulla** , ovvero il pulsante con l'identificatore IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="61d76-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="61d76-188">Per chiudere una finestra di dialogo non modale, è necessario che la stored procedure chiami [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="61d76-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="61d76-189">Si noti che la procedura imposta anche la variabile su **null** per assicurarsi che altre istruzioni che dipendono da questa variabile funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="61d76-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="61d76-190">Se l'utente fa clic sul pulsante **OK** , la procedura recupera lo stato corrente della casella di controllo e la assegna alla variabile **fRelative** .</span><span class="sxs-lookup"><span data-stu-id="61d76-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="61d76-191">USA quindi la variabile per recuperare il numero di riga dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="61d76-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="61d76-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) converte il testo nel controllo di modifica in un intero.</span><span class="sxs-lookup"><span data-stu-id="61d76-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="61d76-193">Il valore di **fRelative** determina se la funzione interpreta il numero come valore con segno o senza segno.</span><span class="sxs-lookup"><span data-stu-id="61d76-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="61d76-194">Se il testo del controllo di modifica non è un numero valido, **GetDlgItemInt** imposta il valore della variabile **ferritor** su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="61d76-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="61d76-195">La procedura controlla questo valore per determinare se visualizzare o meno un messaggio di errore o eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="61d76-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="61d76-196">In caso di errore, la routine della finestra di dialogo Invia un messaggio al controllo di modifica, indirizzando la selezione del testo nel controllo in modo che l'utente possa sostituirlo facilmente.</span><span class="sxs-lookup"><span data-stu-id="61d76-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="61d76-197">Se **GetDlgItemInt** non restituisce un errore, la procedura può eseguire l'attività richiesta o inviare un messaggio alla finestra proprietaria, indirizzando l'operazione in modo da eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="61d76-198">Inizializzazione di una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="61d76-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="61d76-199">È possibile inizializzare la finestra di dialogo e il relativo contenuto durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="61d76-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="61d76-200">L'attività più comune consiste nell'inizializzare i controlli in modo da riflettere le impostazioni correnti della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="61d76-201">Un'altra attività comune consiste nell'incentrare una finestra di dialogo sullo schermo o all'interno della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="61d76-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="61d76-202">Un'attività utile per alcune finestre di dialogo consiste nell'impostare lo stato attivo per l'input su un controllo specificato anziché accettare lo stato attivo per l'input predefinito.</span><span class="sxs-lookup"><span data-stu-id="61d76-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="61d76-203">Nell'esempio seguente, la routine della finestra di dialogo centra la finestra di dialogo e imposta lo stato attivo per l'input durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="61d76-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="61d76-204">Per centrare la finestra di dialogo, la procedura recupera i rettangoli della finestra di dialogo e la finestra proprietaria e calcola una nuova posizione per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="61d76-205">Per impostare lo stato attivo per l'input, la procedura controlla il parametro *wParam* per determinare l'identificatore dello stato attivo per l'input predefinito.</span><span class="sxs-lookup"><span data-stu-id="61d76-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="61d76-206">Nelle istruzioni precedenti, la procedura usa la funzione [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per recuperare l'handle della finestra proprietaria in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61d76-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="61d76-207">La funzione restituisce l'handle della finestra proprietaria alle finestre di dialogo e l'handle della finestra padre per le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="61d76-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="61d76-208">Poiché un'applicazione può creare una finestra di dialogo senza proprietario, la procedura controlla l'handle restituito e usa la funzione [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) per recuperare l'handle della finestra desktop, se necessario.</span><span class="sxs-lookup"><span data-stu-id="61d76-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="61d76-209">Dopo aver calcolato la nuova posizione, la procedura utilizza la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per spostare la finestra di dialogo, specificando il \_ valore principale di HWND per assicurarsi che la finestra di dialogo rimanga nella parte superiore della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="61d76-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="61d76-210">Prima di impostare lo stato attivo per l'input, la procedura controlla l'identificatore di controllo dello stato attivo per l'input predefinito.</span><span class="sxs-lookup"><span data-stu-id="61d76-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="61d76-211">Il sistema passa l'handle di finestra dello stato attivo per l'input predefinito nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="61d76-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="61d76-212">La funzione [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) restituisce l'identificatore per il controllo identificato dall'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="61d76-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="61d76-213">Se l'identificatore non corrisponde all'identificatore corretto, nella procedura viene utilizzata la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="61d76-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="61d76-214">Per recuperare l'handle della finestra del controllo desiderato, è necessaria la funzione [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .</span><span class="sxs-lookup"><span data-stu-id="61d76-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="61d76-215">Creazione di un modello in memoria</span><span class="sxs-lookup"><span data-stu-id="61d76-215">Creating a Template in Memory</span></span>

<span data-ttu-id="61d76-216">Le applicazioni a volte adattano o modificano il contenuto delle finestre di dialogo a seconda dello stato corrente dei dati in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="61d76-217">In questi casi, non è pratico fornire tutti i possibili modelli di finestra di dialogo come risorse nel file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d76-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="61d76-218">Tuttavia, la creazione di modelli in memoria garantisce maggiore flessibilità all'applicazione per adattarsi a qualsiasi circostanza.</span><span class="sxs-lookup"><span data-stu-id="61d76-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="61d76-219">Nell'esempio seguente, l'applicazione crea un modello in memoria per una finestra di dialogo modale che contiene un messaggio e i pulsanti **OK** e **Guida** .</span><span class="sxs-lookup"><span data-stu-id="61d76-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="61d76-220">In un modello di finestra di dialogo tutte le stringhe di caratteri, ad esempio la finestra di dialogo e i titoli dei pulsanti, devono essere stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="61d76-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="61d76-221">In questo esempio viene usata la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare queste stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="61d76-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="61d76-222">Le strutture [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) in un modello di finestra di dialogo devono essere allineate sui limiti **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="61d76-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="61d76-223">Per allineare queste strutture, in questo esempio viene utilizzata una routine helper che accetta un puntatore di input e restituisce il puntatore più vicino allineato a un limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="61d76-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 