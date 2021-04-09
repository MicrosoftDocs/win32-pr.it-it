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
# <a name="how-to-create-a-single-line-edit-control"></a>Come creare un controllo di modifica a riga singola

In questo argomento viene illustrato come creare una finestra di dialogo che contiene un controllo di modifica a riga singola.

Il controllo di modifica a riga singola ha lo stile di [**\_ password es**](edit-control-styles.md) . Per impostazione predefinita, i controlli di modifica con questo stile visualizzano un asterisco per ogni carattere digitato dall'utente. In questo esempio, tuttavia, viene utilizzato il messaggio [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) per modificare il carattere predefinito da un asterisco a un segno più (+). Lo screenshot seguente mostra la finestra di dialogo dopo che l'utente ha immesso una password.

![Screenshot di una finestra di dialogo contenente un controllo di modifica per l'immissione di una password](images/passworddlg.png)

> [!Note]  
> Comctl32.dll versione 6 non è ridistribuibile. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Passaggio 1: creare un'istanza della finestra di dialogo password.

Nell'esempio di codice C++ riportato di seguito viene usata la funzione DialogBox per creare una finestra di dialogo modale. Il modello della finestra di dialogo **IDD \_ password** viene passato come parametro. Definisce, tra le altre cose, gli stili della finestra, i pulsanti e le dimensioni della finestra di dialogo relativa alla password.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Passaggio 2: inizializzare la finestra di dialogo ed elaborare l'input dell'utente.

La procedura della finestra nell'esempio seguente inizializza la finestra di dialogo password ed elabora i messaggi di notifica e l'input dell'utente.

Durante l'inizializzazione, la routine della finestra modifica il carattere della password predefinito in un **+** segno e imposta il pulsante predefinito su **Annulla**.

Durante l'elaborazione dell'input dell'utente, la routine della finestra modifica il pulsante di push predefinito da **Annulla** a **OK** non appena l'utente immette il testo nel controllo di modifica. Se l'utente preme il pulsante **OK** , la procedura della finestra usa i messaggi [**em \_ LINELENGTH**](em-linelength.md) e [**em \_ getline**](em-getline.md) per recuperare il testo.



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

[Modifica riferimento al controllo](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Uso di controlli di modifica](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Modifica controllo](edit-controls.md)
</dt> </dl>

 

 