---
title: Come creare un controllo di modifica su più righe
description: In questo argomento viene illustrato come implementare un elaboratore di testo semplice aggiungendo un controllo di modifica su più righe all'area client di una finestra.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11100d4d6f82c7a352d4ddacaa7fc05694b4d54125febc766a6d3f1c68376e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829072"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Come creare un controllo di modifica su più righe

In questo argomento viene illustrato come implementare un elaboratore di testo semplice aggiungendo un controllo di modifica su più righe all'area client di una finestra. Usando il controllo di modifica su più righe, l'utente può selezionare i comandi di modifica da un menu. Questi comandi consentono all'utente di eseguire semplici operazioni di modifica, ad esempio annullare un'azione precedente, tagliare o copiare le selezioni negli Appunti, incollare il testo dagli Appunti ed eliminare la selezione corrente.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


L'applicazione deve includere il codice per creare un'istanza di e inizializzare un controllo di modifica su più righe e quindi elaborare i comandi di modifica dell'utente.

L'esempio di codice C++ seguente implementa gran parte delle funzionalità di un elaboratore di testo semplice aggiungendo un controllo di modifica su più righe all'area client di una finestra. Il sistema esegue automaticamente operazioni di ritorno a capo automatico per il controllo di modifica e gestisce anche l'elaborazione per la barra di scorrimento verticale (creata specificando [**ES \_ AUTOVSCROLL**](edit-control-styles.md) nella chiamata alla [**funzione CreateWindow).**](/windows/desktop/api/winuser/nf-winuser-createwindowa)

I comandi di modifica dell'utente vengono inviati al processo della finestra tramite [**messaggi di notifica WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)

> [!Note]  
> Se la finestra include la Windows barra multifunzione, le dimensioni del controllo di modifica devono essere regolate in base all'altezza della barra multifunzione. Per altre informazioni, vedere Windows [Ribbon Framework.](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry)

 



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

[Informazioni di riferimento sul controllo Edit](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Uso dei controlli di modifica](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Controllo Edit](edit-controls.md)
</dt> </dl>

 

 