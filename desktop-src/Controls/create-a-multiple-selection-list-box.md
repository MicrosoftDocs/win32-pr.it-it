---
title: Come creare una casella Multiple-Selection dati
description: In questo argomento viene illustrato come visualizzare e accedere al contenuto di una directory in una casella di riepilogo a selezione multipla.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f375ca2df82f851401baec79683a54ff28cf14e7a004d08cb0885e60fb036d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920861"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Come creare una casella Multiple-Selection dati

In questo argomento viene illustrato come visualizzare e accedere al contenuto di una directory in una casella di riepilogo a selezione multipla. In una casella di riepilogo a selezione multipla l'utente può selezionare più di un elemento alla volta.

L'esempio di codice C++ in questo argomento consente a un utente di visualizzare un elenco di file nella directory corrente, selezionare un gruppo di file dall'elenco ed eliminarli.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


L'applicazione elenco directory deve eseguire le attività correlate alla casella di riepilogo seguenti:

-   Inizializzare la casella di riepilogo.
-   Recuperare le selezioni dell'utente dalla casella di riepilogo.
-   Rimuovere i nomi dei file dalla casella di riepilogo dopo l'eliminazione dei file selezionati.

Nell'esempio di codice C++ seguente la routine della finestra di dialogo inizializza la casella di riepilogo a selezione multipla (IDC FILELIST) usando la funzione \_ [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) per compilare la casella di riepilogo con i nomi di tutti i file nella directory corrente.

Quando l'utente seleziona un gruppo di  file e sceglie il pulsante Elimina, la procedura della finestra di dialogo invia il messaggio [**\_ LB GETSELCOUNT,**](lb-getselcount.md) per recuperare il numero di file selezionati e il messaggio [**LB \_ GETSELITEMS,**](lb-getselitems.md) per recuperare una matrice di elementi della casella di riepilogo selezionati. Dopo l'eliminazione di un file, la routine della finestra di dialogo rimuove l'elemento corrispondente dalla casella di riepilogo inviando il [**messaggio \_ LB DELETESTRING.**](lb-deletestring.md)



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

[Informazioni di riferimento sul controllo Casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso delle caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 




