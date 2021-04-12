---
title: Come creare un controllo List-View
description: In questo argomento viene illustrato come creare un controllo visualizzazione elenco. Per creare un controllo di visualizzazione elenco, usare la funzione CreateWindow o CreateWindowEx e specificare la classe della \_ finestra ListView di WC.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474672"
---
# <a name="how-to-create-a-list-view-control"></a>Come creare un controllo List-View

In questo argomento viene illustrato come creare un controllo visualizzazione elenco. Per creare un controllo di visualizzazione elenco, usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la classe della finestra [**\_ ListView di WC**](common-control-window-classes.md) .

È anche possibile creare un controllo di visualizzazione elenco come parte di un modello di finestra di dialogo. È necessario specificare [**il \_ controllo ListView di WC**](common-control-window-classes.md) come nome della classe. Per utilizzare un controllo visualizzazione elenco come parte di un modello di finestra di dialogo, è necessario chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) prima di creare un'istanza della finestra di dialogo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Prima di tutto, registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e specificando il bit delle [**\_ \_ classi ListView di ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) nella struttura **InitCommonControlsEx** associata. In questo modo si garantisce che la DLL dei controlli comuni venga caricata. Usare quindi la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la classe della finestra di [**\_ controllo WC ListView**](common-control-window-classes.md) .

> [!Note]  
> Per impostazione predefinita, un controllo di visualizzazione elenco Usa il tipo di carattere del titolo dell'icona. Tuttavia, è possibile usare un messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) per specificare il tipo di carattere da usare per il testo. È necessario inviare questo messaggio prima di inserire elementi. Il controllo Usa le dimensioni del tipo di carattere specificato dal messaggio di **tipo \_ carattere di WM** per determinare la spaziatura e il layout. È anche possibile personalizzare il tipo di carattere per ogni elemento. Per ulteriori informazioni, vedere [Custom disegnato](custom-draw.md).

 

Nell'esempio di codice C++ riportato di seguito viene creato un controllo visualizzazione elenco in visualizzazione report.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




In genere, le applicazioni di visualizzazione elenco consentono all'utente di passare da una visualizzazione all'altra.

Nell'esempio di codice C++ riportato di seguito viene modificato lo stile della finestra della visualizzazione elenco, che a sua volta modifica la visualizzazione.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo visualizzazione elenco](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

 