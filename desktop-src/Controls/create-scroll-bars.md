---
title: Come creare barre di scorrimento
description: Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione CreateWindowEx e specificando WS \_ HSCROLL, WS VSCROLL o entrambi \_ gli stili.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec76c49d9f97e21626546a760d0e42a44b04c70db5790e0b80c08fcdee34412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831753"
---
# <a name="how-to-create-scroll-bars"></a>Come creare barre di scorrimento

Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando WS \_ HSCROLL, WS VSCROLL o entrambi \_ gli stili.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-scroll-bar"></a>Creare una barra di scorrimento

Nell'esempio seguente viene creata una finestra con barre di scorrimento orizzontali e verticali standard.


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



Per elaborare i messaggi della barra di scorrimento per queste barre di scorrimento, è necessario includere il codice appropriato nella routine della finestra principale.

È possibile usare la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra di scorrimento specificando la classe della finestra SCROLLBAR. Verrà creata una barra di scorrimento orizzontale o verticale, a seconda che [**SBS \_ HORZ**](scroll-bar-control-styles.md) o [**SBS \_ VERT**](scroll-bar-control-styles.md) sia specificato come stile della finestra. È anche possibile specificare le dimensioni della barra di scorrimento e la relativa posizione rispetto alla finestra padre.

Nell'esempio seguente viene creata una barra di scorrimento orizzontale posizionata lungo la parte inferiore dell'area client della finestra padre.


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle barre di scorrimento](using-scroll-bars.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 