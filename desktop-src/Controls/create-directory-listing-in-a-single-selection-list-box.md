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
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Come creare un elenco di directory in una casella di riepilogo a selezione singola

In questo argomento viene illustrato come utilizzare una casella di riepilogo a selezione singola per visualizzare e accedere al contenuto di una directory. La casella di riepilogo a selezione singola è il tipo predefinito della casella di riepilogo. Un utente può selezionare un solo elemento alla volta da una casella di riepilogo a selezione singola.

L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un file nell'elenco ed eliminarlo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


L'applicazione Directory Listing deve eseguire le seguenti attività correlate alla casella di riepilogo:

-   Inizializzare la casella di riepilogo.
-   Recupera la selezione dell'utente dalla casella di riepilogo.
-   Rimuovere il nome file dalla casella di riepilogo dopo che il file selezionato è stato eliminato.

Nell'esempio di codice C++ riportato di seguito, la routine della finestra di dialogo Inizializza la casella di riepilogo a selezione singola ( \_ file IDC) utilizzando la funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per riempire la casella di riepilogo con i nomi di tutti i file nella directory corrente. Quando l'utente seleziona un file e sceglie il pulsante **Elimina** , la funzione [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) Recupera il nome del file selezionato. Il codice elimina il file usando la funzione [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e aggiorna la casella di riepilogo directory inviando il [**messaggio \_ DELETESTRING lb**](lb-deletestring.md) .



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso di caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 