---
title: Come creare un controllo di modifica a riga singola
description: In questo argomento viene illustrato come creare una finestra di dialogo contenente un controllo di modifica a riga singola.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597c3e611f53af56a42f837c4d85a43f97ff846e371314b130d72c568aaf860e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829117"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Come creare un controllo di modifica a riga singola

In questo argomento viene illustrato come creare una finestra di dialogo contenente un controllo di modifica a riga singola.

Il controllo di modifica a riga singola ha lo [**stile password \_ ES.**](edit-control-styles.md) Per impostazione predefinita, i controlli di modifica con questo stile visualizzano un asterisco per ogni carattere digitato dall'utente. In questo esempio, tuttavia, viene utilizzato il messaggio [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) per modificare il carattere predefinito da un asterisco a un segno più (+). Lo screenshot seguente mostra la finestra di dialogo dopo che l'utente ha immesso una password.

![Screenshot di una finestra di dialogo contenente un controllo di modifica per l'immissione di una password](images/passworddlg.png)

> [!Note]  
> Comctl32.dll versione 6 non è ridistribuibile. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Passaggio 1: Creare un'istanza della finestra di dialogo della password.

L'esempio di codice C++ seguente usa la funzione DialogBox per creare una finestra di dialogo modale. Il modello di finestra di **dialogo IDD \_ PASSWORD** viene passato come parametro. Definisce, tra le altre cose, gli stili, i pulsanti e le dimensioni della finestra di dialogo della password.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Passaggio 2: Inizializzare la finestra di dialogo ed elaborare l'input dell'utente.

La routine della finestra nell'esempio seguente inizializza la finestra di dialogo della password ed elabora i messaggi di notifica e l'input dell'utente.

Durante l'inizializzazione, la routine della finestra modifica il carattere della password predefinito in un segno e **+** imposta il pulsante di comando predefinito su **Annulla.**

Durante l'elaborazione dell'input dell'utente, la routine della finestra modifica il pulsante di comando predefinito da **CANCEL** a **OK** non appena l'utente immette testo nel controllo di modifica. Se l'utente preme il **pulsante OK,** la routine della finestra usa i messaggi [**EM \_ LINELENGTH**](em-linelength.md) ed [**EM \_ GETLINE**](em-getline.md) per recuperare il testo.



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli di modifica](about-edit-controls.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Edit](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Uso dei controlli di modifica](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Controllo Edit](edit-controls.md)
</dt> </dl>

 

 