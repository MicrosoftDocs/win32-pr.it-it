---
title: Come creare un controllo List-View controllo
description: Questo argomento illustra come creare un controllo visualizzazione elenco. Per creare un controllo di visualizzazione elenco, usare la funzione CreateWindow o CreateWindowEx e specificare la classe finestra WC \_ LISTVIEW.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826611"
---
# <a name="how-to-create-a-list-view-control"></a>Come creare un controllo List-View controllo

Questo argomento illustra come creare un controllo visualizzazione elenco. Per creare un controllo visualizzazione elenco, usare la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la [**classe finestra \_ LISTVIEW WC.**](common-control-window-classes.md)

È anche possibile creare un controllo visualizzazione elenco come parte di un modello di finestra di dialogo. È necessario specificare [**WC \_ LISTVIEW**](common-control-window-classes.md) come nome della classe. Per usare un controllo visualizzazione elenco come parte di un modello di finestra di dialogo, è necessario chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) prima di creare un'istanza della finestra di dialogo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Registrare prima di tutto la classe window chiamando la [**funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e specificando il bit [**ICC \_ LISTVIEW \_ CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) nella struttura **INITCOMMONCONTROLSEX** che lo accompagna. In questo modo si garantisce che la DLL dei controlli comuni sia caricata. Usare quindi la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la [**classe finestra WC \_ LISTVIEW.**](common-control-window-classes.md)

> [!Note]  
> Per impostazione predefinita, un controllo visualizzazione elenco usa il tipo di carattere del titolo dell'icona. È tuttavia possibile usare un [**messaggio WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) per specificare il tipo di carattere da usare per il testo. È consigliabile inviare questo messaggio prima di inserire gli elementi. Il controllo usa le dimensioni del tipo di carattere specificato dal messaggio **WM \_ SETFONT** per determinare la spaziatura e il layout. È anche possibile personalizzare il tipo di carattere per ogni elemento. Per altre informazioni, vedere [Disegno personalizzato.](custom-draw.md)

 

L'esempio di codice C++ seguente crea un controllo visualizzazione elenco nella visualizzazione report.


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




In genere, le applicazioni di visualizzazione elenco consentono all'utente di passare da una visualizzazione a un'altra.

L'esempio di codice C++ seguente modifica lo stile della finestra della visualizzazione elenco, che a sua volta modifica la visualizzazione.


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

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View seguenti](list-view-controls-overview.md)
</dt> <dt>

[Uso dei List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 