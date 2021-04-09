---
title: Creazione di un elenco di directory in una casella di riepilogo
description: In questo argomento viene illustrato come utilizzare una casella di riepilogo a selezione singola per visualizzare e accedere al contenuto di una directory.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963566"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="86638-103">Come creare un elenco di directory in una casella di riepilogo a selezione singola</span><span class="sxs-lookup"><span data-stu-id="86638-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="86638-104">In questo argomento viene illustrato come utilizzare una casella di riepilogo a selezione singola per visualizzare e accedere al contenuto di una directory.</span><span class="sxs-lookup"><span data-stu-id="86638-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="86638-105">La casella di riepilogo a selezione singola è il tipo predefinito della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="86638-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="86638-106">Un utente può selezionare un solo elemento alla volta da una casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="86638-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="86638-107">L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un file nell'elenco ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="86638-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="86638-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="86638-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="86638-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="86638-109">Technologies</span></span>

-   [<span data-ttu-id="86638-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="86638-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="86638-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="86638-111">Prerequisites</span></span>

-   <span data-ttu-id="86638-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="86638-112">C/C++</span></span>
-   <span data-ttu-id="86638-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="86638-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="86638-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="86638-114">Instructions</span></span>


<span data-ttu-id="86638-115">L'applicazione Directory Listing deve eseguire le seguenti attività correlate alla casella di riepilogo:</span><span class="sxs-lookup"><span data-stu-id="86638-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="86638-116">Inizializzare la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="86638-116">Initialize the list box.</span></span>
-   <span data-ttu-id="86638-117">Recupera la selezione dell'utente dalla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="86638-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="86638-118">Rimuovere il nome file dalla casella di riepilogo dopo che il file selezionato è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="86638-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="86638-119">Nell'esempio di codice C++ riportato di seguito, la routine della finestra di dialogo Inizializza la casella di riepilogo a selezione singola ( \_ file IDC) utilizzando la funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per riempire la casella di riepilogo con i nomi di tutti i file nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="86638-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="86638-120">Quando l'utente seleziona un file e sceglie il pulsante **Elimina** , la funzione [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) Recupera il nome del file selezionato.</span><span class="sxs-lookup"><span data-stu-id="86638-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="86638-121">Il codice elimina il file usando la funzione [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e aggiorna la casella di riepilogo directory inviando il [**messaggio \_ DELETESTRING lb**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="86638-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
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
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
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



## <a name="related-topics"></a><span data-ttu-id="86638-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86638-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86638-123">Riferimento al controllo casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="86638-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="86638-124">Informazioni sulle caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="86638-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="86638-125">Uso di caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="86638-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 