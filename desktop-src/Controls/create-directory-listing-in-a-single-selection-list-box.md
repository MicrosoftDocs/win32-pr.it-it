---
title: Creare un elenco di directory in un controllo ListBox
description: Questo argomento illustra come usare una casella di riepilogo a selezione singola per visualizzare e accedere al contenuto di una directory.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926dc09e1e8cee85d230b0715684e084350c97c64b6f6cafb8228cc82cc61dc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920471"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Come creare un elenco di directory in un controllo ListBox a selezione singola

Questo argomento illustra come usare una casella di riepilogo a selezione singola per visualizzare e accedere al contenuto di una directory. La casella di riepilogo a selezione singola è il tipo di casella di riepilogo predefinito. Un utente può selezionare un solo elemento alla volta da una casella di riepilogo a selezione singola.

L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un file dall'elenco ed eliminarlo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


L'applicazione elenco directory deve eseguire le attività correlate alla casella di riepilogo seguenti:

-   Inizializzare la casella di riepilogo.
-   Recuperare la selezione dell'utente dalla casella di riepilogo.
-   Rimuovere il nome del file dalla casella di riepilogo dopo l'eliminazione del file selezionato.

Nell'esempio di codice C++ seguente la procedura della finestra di dialogo inizializza la casella di riepilogo a selezione singola (IDC FILELIST) usando la funzione \_ [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per riempire la casella di riepilogo con i nomi di tutti i file nella directory corrente. Quando l'utente seleziona un file e sceglie il pulsante **Elimina,** la [**funzione DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera il nome del file selezionato. Il codice elimina il file usando la [**funzione DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e aggiorna la casella di riepilogo della directory inviando il messaggio [**\_ LB DELETESTRING.**](lb-deletestring.md)



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

[Informazioni di riferimento sul controllo Casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso delle caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 