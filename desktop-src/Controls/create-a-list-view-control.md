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
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="28cbc-104">Come creare un controllo List-View</span><span class="sxs-lookup"><span data-stu-id="28cbc-104">How to Create a List-View Control</span></span>

<span data-ttu-id="28cbc-105">In questo argomento viene illustrato come creare un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="28cbc-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="28cbc-106">Per creare un controllo di visualizzazione elenco, usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la classe della finestra [**\_ ListView di WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="28cbc-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="28cbc-107">È anche possibile creare un controllo di visualizzazione elenco come parte di un modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="28cbc-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="28cbc-108">È necessario specificare [**il \_ controllo ListView di WC**](common-control-window-classes.md) come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="28cbc-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="28cbc-109">Per utilizzare un controllo visualizzazione elenco come parte di un modello di finestra di dialogo, è necessario chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) prima di creare un'istanza della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="28cbc-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="28cbc-110">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="28cbc-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="28cbc-111">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="28cbc-111">Technologies</span></span>

-   [<span data-ttu-id="28cbc-112">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="28cbc-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="28cbc-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="28cbc-113">Prerequisites</span></span>

-   <span data-ttu-id="28cbc-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="28cbc-114">C/C++</span></span>
-   <span data-ttu-id="28cbc-115">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="28cbc-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="28cbc-116">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="28cbc-116">Instructions</span></span>


<span data-ttu-id="28cbc-117">Prima di tutto, registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e specificando il bit delle [**\_ \_ classi ListView di ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) nella struttura **InitCommonControlsEx** associata.</span><span class="sxs-lookup"><span data-stu-id="28cbc-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="28cbc-118">In questo modo si garantisce che la DLL dei controlli comuni venga caricata.</span><span class="sxs-lookup"><span data-stu-id="28cbc-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="28cbc-119">Usare quindi la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la classe della finestra di [**\_ controllo WC ListView**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="28cbc-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="28cbc-120">Per impostazione predefinita, un controllo di visualizzazione elenco Usa il tipo di carattere del titolo dell'icona.</span><span class="sxs-lookup"><span data-stu-id="28cbc-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="28cbc-121">Tuttavia, è possibile usare un messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) per specificare il tipo di carattere da usare per il testo.</span><span class="sxs-lookup"><span data-stu-id="28cbc-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="28cbc-122">È necessario inviare questo messaggio prima di inserire elementi.</span><span class="sxs-lookup"><span data-stu-id="28cbc-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="28cbc-123">Il controllo Usa le dimensioni del tipo di carattere specificato dal messaggio di **tipo \_ carattere di WM** per determinare la spaziatura e il layout.</span><span class="sxs-lookup"><span data-stu-id="28cbc-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="28cbc-124">È anche possibile personalizzare il tipo di carattere per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="28cbc-124">You can also customize the font for each item.</span></span> <span data-ttu-id="28cbc-125">Per ulteriori informazioni, vedere [Custom disegnato](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="28cbc-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="28cbc-126">Nell'esempio di codice C++ riportato di seguito viene creato un controllo visualizzazione elenco in visualizzazione report.</span><span class="sxs-lookup"><span data-stu-id="28cbc-126">The following C++ code example creates a list-view control in report view.</span></span>


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




<span data-ttu-id="28cbc-127">In genere, le applicazioni di visualizzazione elenco consentono all'utente di passare da una visualizzazione all'altra.</span><span class="sxs-lookup"><span data-stu-id="28cbc-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="28cbc-128">Nell'esempio di codice C++ riportato di seguito viene modificato lo stile della finestra della visualizzazione elenco, che a sua volta modifica la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="28cbc-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="28cbc-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28cbc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28cbc-130">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="28cbc-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="28cbc-131">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="28cbc-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="28cbc-132">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="28cbc-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 