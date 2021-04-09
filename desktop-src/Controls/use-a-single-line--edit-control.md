---
title: Come creare un controllo di modifica a riga singola
description: In questo argomento viene illustrato come creare una finestra di dialogo che contiene un controllo di modifica a riga singola.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047607"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="032cf-103">Come creare un controllo di modifica a riga singola</span><span class="sxs-lookup"><span data-stu-id="032cf-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="032cf-104">In questo argomento viene illustrato come creare una finestra di dialogo che contiene un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="032cf-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="032cf-105">Il controllo di modifica a riga singola ha lo stile di [**\_ password es**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="032cf-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="032cf-106">Per impostazione predefinita, i controlli di modifica con questo stile visualizzano un asterisco per ogni carattere digitato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="032cf-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="032cf-107">In questo esempio, tuttavia, viene utilizzato il messaggio [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) per modificare il carattere predefinito da un asterisco a un segno più (+).</span><span class="sxs-lookup"><span data-stu-id="032cf-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="032cf-108">Lo screenshot seguente mostra la finestra di dialogo dopo che l'utente ha immesso una password.</span><span class="sxs-lookup"><span data-stu-id="032cf-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![Screenshot di una finestra di dialogo contenente un controllo di modifica per l'immissione di una password](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="032cf-110">Comctl32.dll versione 6 non è ridistribuibile.</span><span class="sxs-lookup"><span data-stu-id="032cf-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="032cf-111">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="032cf-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="032cf-112">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="032cf-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="032cf-113">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="032cf-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="032cf-114">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="032cf-114">Technologies</span></span>

-   [<span data-ttu-id="032cf-115">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="032cf-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="032cf-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="032cf-116">Prerequisites</span></span>

-   <span data-ttu-id="032cf-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="032cf-117">C/C++</span></span>
-   <span data-ttu-id="032cf-118">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="032cf-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="032cf-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="032cf-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="032cf-120">Passaggio 1: creare un'istanza della finestra di dialogo password.</span><span class="sxs-lookup"><span data-stu-id="032cf-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="032cf-121">Nell'esempio di codice C++ riportato di seguito viene usata la funzione DialogBox per creare una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="032cf-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="032cf-122">Il modello della finestra di dialogo **IDD \_ password** viene passato come parametro.</span><span class="sxs-lookup"><span data-stu-id="032cf-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="032cf-123">Definisce, tra le altre cose, gli stili della finestra, i pulsanti e le dimensioni della finestra di dialogo relativa alla password.</span><span class="sxs-lookup"><span data-stu-id="032cf-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="032cf-124">Passaggio 2: inizializzare la finestra di dialogo ed elaborare l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="032cf-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="032cf-125">La procedura della finestra nell'esempio seguente inizializza la finestra di dialogo password ed elabora i messaggi di notifica e l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="032cf-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="032cf-126">Durante l'inizializzazione, la routine della finestra modifica il carattere della password predefinito in un **+** segno e imposta il pulsante predefinito su **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="032cf-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="032cf-127">Durante l'elaborazione dell'input dell'utente, la routine della finestra modifica il pulsante di push predefinito da **Annulla** a **OK** non appena l'utente immette il testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="032cf-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="032cf-128">Se l'utente preme il pulsante **OK** , la procedura della finestra usa i messaggi [**em \_ LINELENGTH**](em-linelength.md) e [**em \_ getline**](em-getline.md) per recuperare il testo.</span><span class="sxs-lookup"><span data-stu-id="032cf-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a><span data-ttu-id="032cf-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="032cf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="032cf-130">Informazioni sui controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="032cf-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="032cf-131">Modifica riferimento al controllo</span><span class="sxs-lookup"><span data-stu-id="032cf-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="032cf-132">Uso di controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="032cf-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="032cf-133">Modifica controllo</span><span class="sxs-lookup"><span data-stu-id="032cf-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 