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
# <a name="how-to-create-a-multiple-selection-list-box"></a>Come creare una casella di riepilogo Multiple-Selection

In questo argomento viene illustrato come visualizzare e accedere al contenuto di una directory in una casella di riepilogo a selezione multipla. In una casella di riepilogo a selezione multipla, l'utente può selezionare più di un elemento alla volta.

L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un gruppo di file dall'elenco ed eliminarli.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


L'applicazione elenco directory deve eseguire le seguenti attività correlate alla casella di riepilogo:

-   Inizializzare la casella di riepilogo.
-   Recuperare le selezioni dell'utente dalla casella di riepilogo.
-   Rimuovere i nomi file dalla casella di riepilogo dopo l'eliminazione dei file selezionati.

Nell'esempio di codice C++ riportato di seguito, la routine della finestra di dialogo Inizializza la casella di riepilogo a selezione multipla ( \_ file IDC) utilizzando la funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per riempire la casella di riepilogo con i nomi di tutti i file nella directory corrente.

Quando l'utente seleziona un gruppo di file e sceglie il pulsante **Elimina** , la routine della finestra di dialogo Invia il messaggio [**\_ GETSELCOUNT lb**](lb-getselcount.md) per recuperare il numero di file selezionati e il messaggio [**lb \_ GETSELITEMS**](lb-getselitems.md) per recuperare una matrice di elementi selezionati della casella di riepilogo. Dopo l'eliminazione di un file, la routine della finestra di dialogo rimuove l'elemento corrispondente dalla casella di riepilogo inviando il messaggio [**\_ DELETESTRING lb**](lb-deletestring.md) .



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso di caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 




