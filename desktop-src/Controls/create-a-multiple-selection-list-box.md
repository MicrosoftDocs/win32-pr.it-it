---
title: Come creare una casella di riepilogo Multiple-Selection
description: In questo argomento viene illustrato come visualizzare e accedere al contenuto di una directory in una casella di riepilogo a selezione multipla.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047611"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="7c118-103">Come creare una casella di riepilogo Multiple-Selection</span><span class="sxs-lookup"><span data-stu-id="7c118-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="7c118-104">In questo argomento viene illustrato come visualizzare e accedere al contenuto di una directory in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="7c118-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="7c118-105">In una casella di riepilogo a selezione multipla, l'utente può selezionare più di un elemento alla volta.</span><span class="sxs-lookup"><span data-stu-id="7c118-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="7c118-106">L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un gruppo di file dall'elenco ed eliminarli.</span><span class="sxs-lookup"><span data-stu-id="7c118-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7c118-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7c118-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7c118-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7c118-108">Technologies</span></span>

-   [<span data-ttu-id="7c118-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="7c118-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7c118-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7c118-110">Prerequisites</span></span>

-   <span data-ttu-id="7c118-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7c118-111">C/C++</span></span>
-   <span data-ttu-id="7c118-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="7c118-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7c118-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7c118-113">Instructions</span></span>


<span data-ttu-id="7c118-114">L'applicazione elenco directory deve eseguire le seguenti attività correlate alla casella di riepilogo:</span><span class="sxs-lookup"><span data-stu-id="7c118-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="7c118-115">Inizializzare la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7c118-115">Initialize the list box.</span></span>
-   <span data-ttu-id="7c118-116">Recuperare le selezioni dell'utente dalla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7c118-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="7c118-117">Rimuovere i nomi file dalla casella di riepilogo dopo l'eliminazione dei file selezionati.</span><span class="sxs-lookup"><span data-stu-id="7c118-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="7c118-118">Nell'esempio di codice C++ riportato di seguito, la routine della finestra di dialogo Inizializza la casella di riepilogo a selezione multipla ( \_ file IDC) utilizzando la funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per riempire la casella di riepilogo con i nomi di tutti i file nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="7c118-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="7c118-119">Quando l'utente seleziona un gruppo di file e sceglie il pulsante **Elimina** , la routine della finestra di dialogo Invia il messaggio [**\_ GETSELCOUNT lb**](lb-getselcount.md) per recuperare il numero di file selezionati e il messaggio [**lb \_ GETSELITEMS**](lb-getselitems.md) per recuperare una matrice di elementi selezionati della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7c118-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="7c118-120">Dopo l'eliminazione di un file, la routine della finestra di dialogo rimuove l'elemento corrispondente dalla casella di riepilogo inviando il messaggio [**\_ DELETESTRING lb**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="7c118-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
        case WM_INITDIALOG: 
 
            // Initialize the list box by filling it with files from 
            // the current directory. 
            pszCurDir = achBuffer; 
            GetCurrentDirectory(MAX_PATH, pszCurDir);
            DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
            SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
 
            return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
                return FALSE; 
    } 
} 
```



## <a name="related-topics"></a><span data-ttu-id="7c118-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c118-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c118-122">Riferimento al controllo casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7c118-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7c118-123">Informazioni sulle caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7c118-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="7c118-124">Uso di caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7c118-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




