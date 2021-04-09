---
title: Come creare un controllo di modifica su più righe
description: In questo argomento viene illustrato come implementare un semplice elaboratore di testo aggiungendo un controllo di modifica su più righe all'area client di una finestra.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963574"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Come creare un controllo di modifica su più righe

In questo argomento viene illustrato come implementare un semplice elaboratore di testo aggiungendo un controllo di modifica su più righe all'area client di una finestra. Utilizzando il controllo di modifica su più righe, l'utente può selezionare Modifica comandi da un menu. Questi comandi consentono all'utente di eseguire semplici operazioni di modifica, ad esempio annullare un'azione precedente, tagliare o copiare selezioni negli Appunti, incollare il testo dagli Appunti ed eliminare la selezione corrente.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


L'applicazione deve includere codice per creare un'istanza di e inizializzare un controllo di modifica su più righe e quindi elaborare i comandi di modifica dell'utente.

Nell'esempio di codice C++ seguente viene implementata la maggior parte delle funzionalità di un elaboratore di testo semplice mediante l'aggiunta di un controllo di modifica su più righe all'area client di una finestra. Il sistema esegue automaticamente le operazioni WordWrap per il controllo di modifica e gestisce anche l'elaborazione per la barra di scorrimento verticale (creata specificando [**es \_ AUTOVSCROLL**](edit-control-styles.md) nella chiamata alla funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).

I comandi di modifica utente vengono inviati al processo della finestra tramite i messaggi di notifica del [**\_ comando WM**](/windows/desktop/menurc/wm-command) .

> [!Note]  
> Se la finestra include la barra multifunzione di Windows, le dimensioni del controllo di modifica devono essere modificate in modo da contenere l'altezza della barra multifunzione. Per altre informazioni, vedere [Framework della barra multifunzione di Windows](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
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

 

 