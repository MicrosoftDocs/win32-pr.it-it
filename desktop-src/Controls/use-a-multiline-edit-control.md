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
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="2ee22-103">Come creare un controllo di modifica su più righe</span><span class="sxs-lookup"><span data-stu-id="2ee22-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="2ee22-104">In questo argomento viene illustrato come implementare un semplice elaboratore di testo aggiungendo un controllo di modifica su più righe all'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="2ee22-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="2ee22-105">Utilizzando il controllo di modifica su più righe, l'utente può selezionare Modifica comandi da un menu.</span><span class="sxs-lookup"><span data-stu-id="2ee22-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="2ee22-106">Questi comandi consentono all'utente di eseguire semplici operazioni di modifica, ad esempio annullare un'azione precedente, tagliare o copiare selezioni negli Appunti, incollare il testo dagli Appunti ed eliminare la selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="2ee22-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2ee22-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="2ee22-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2ee22-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="2ee22-108">Technologies</span></span>

-   [<span data-ttu-id="2ee22-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="2ee22-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2ee22-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="2ee22-110">Prerequisites</span></span>

-   <span data-ttu-id="2ee22-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="2ee22-111">C/C++</span></span>
-   <span data-ttu-id="2ee22-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="2ee22-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2ee22-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="2ee22-113">Instructions</span></span>


<span data-ttu-id="2ee22-114">L'applicazione deve includere codice per creare un'istanza di e inizializzare un controllo di modifica su più righe e quindi elaborare i comandi di modifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2ee22-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="2ee22-115">Nell'esempio di codice C++ seguente viene implementata la maggior parte delle funzionalità di un elaboratore di testo semplice mediante l'aggiunta di un controllo di modifica su più righe all'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="2ee22-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="2ee22-116">Il sistema esegue automaticamente le operazioni WordWrap per il controllo di modifica e gestisce anche l'elaborazione per la barra di scorrimento verticale (creata specificando [**es \_ AUTOVSCROLL**](edit-control-styles.md) nella chiamata alla funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).</span><span class="sxs-lookup"><span data-stu-id="2ee22-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="2ee22-117">I comandi di modifica utente vengono inviati al processo della finestra tramite i messaggi di notifica del [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2ee22-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="2ee22-118">Se la finestra include la barra multifunzione di Windows, le dimensioni del controllo di modifica devono essere modificate in modo da contenere l'altezza della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2ee22-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="2ee22-119">Per altre informazioni, vedere [Framework della barra multifunzione di Windows](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span><span class="sxs-lookup"><span data-stu-id="2ee22-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



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



## <a name="related-topics"></a><span data-ttu-id="2ee22-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ee22-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ee22-121">Informazioni sui controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="2ee22-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="2ee22-122">Modifica riferimento al controllo</span><span class="sxs-lookup"><span data-stu-id="2ee22-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2ee22-123">Uso di controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="2ee22-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="2ee22-124">Modifica controllo</span><span class="sxs-lookup"><span data-stu-id="2ee22-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 