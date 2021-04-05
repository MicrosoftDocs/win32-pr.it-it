---
title: Barre di scorrimento Flat
description: In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730458"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="b705d-103">Barre di scorrimento Flat</span><span class="sxs-lookup"><span data-stu-id="b705d-103">Flat Scroll Bars</span></span>

<span data-ttu-id="b705d-104">In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici.</span><span class="sxs-lookup"><span data-stu-id="b705d-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="b705d-105">Dal punto di vista funzionale, le barre di scorrimento Flat funzionano esattamente come le barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="b705d-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="b705d-106">La differenza consiste nel fatto che è possibile personalizzare l'aspetto in modo più ampio rispetto alle barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="b705d-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="b705d-107">Nella figura seguente è illustrata una finestra che contiene una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="b705d-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![Screenshot di una finestra che contiene una barra di scorrimento semplice](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="b705d-109">Le barre di scorrimento Flat sono supportate dalle versioni Comctl32.dll da 4,71 a 5,82.</span><span class="sxs-lookup"><span data-stu-id="b705d-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="b705d-110">Comctl32.dll versioni 6,00 e successive non supportano le barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="b705d-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="b705d-111">Uso delle barre di scorrimento Flat</span><span class="sxs-lookup"><span data-stu-id="b705d-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="b705d-112">In questa sezione viene descritto come implementare le barre di scorrimento flat nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b705d-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="b705d-113">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="b705d-113">Before You Begin</span></span>

<span data-ttu-id="b705d-114">Per usare le funzioni della barra di scorrimento Flat, è necessario includere COMmctrl. h nei file di origine e il collegamento a Comctl32. lib.</span><span class="sxs-lookup"><span data-stu-id="b705d-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="b705d-115">Aggiunta di barre di scorrimento Flat a una finestra</span><span class="sxs-lookup"><span data-stu-id="b705d-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="b705d-116">Per aggiungere barre di scorrimento Flat a una finestra, chiamare [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando l'handle alla finestra.</span><span class="sxs-lookup"><span data-stu-id="b705d-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="b705d-117">Anziché utilizzare le funzioni della barra di scorrimento standard per modificare le barre di scorrimento, è necessario utilizzare la \_ funzione equivalente FlatSB xxx.</span><span class="sxs-lookup"><span data-stu-id="b705d-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="b705d-118">Sono disponibili funzioni barra di scorrimento semplice per l'impostazione e il recupero delle informazioni di scorrimento, dell'intervallo e della posizione.</span><span class="sxs-lookup"><span data-stu-id="b705d-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="b705d-119">Se le barre di scorrimento semplice non sono state inizializzate per la finestra, l'API della barra di scorrimento flat verrà rinviata alle funzioni standard corrispondenti, se usate.</span><span class="sxs-lookup"><span data-stu-id="b705d-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="b705d-120">In questo modo è possibile attivare e disattivare le barre di scorrimento piatte senza dover scrivere codice condizionale.</span><span class="sxs-lookup"><span data-stu-id="b705d-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="b705d-121">Poiché un'applicazione potrebbe avere impostato metriche personalizzate per le barre di scorrimento Flat, non vengono aggiornate automaticamente quando le metriche di sistema cambiano.</span><span class="sxs-lookup"><span data-stu-id="b705d-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="b705d-122">Quando le metriche della barra di scorrimento del sistema cambiano, viene trasmesso un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con il relativo *wParam* impostato su [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="b705d-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="b705d-123">Per aggiornare le barre di scorrimento Flat alle nuove metriche di sistema, le applicazioni devono gestire questo messaggio e modificare le proprietà dipendenti dalla metrica della barra di scorrimento flat in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="b705d-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="b705d-124">Per aggiornare le proprietà della barra di scorrimento, usare [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="b705d-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="b705d-125">Il frammento di codice seguente modifica le proprietà dipendenti dalla metrica della barra di scorrimento semplice nei valori di sistema correnti.</span><span class="sxs-lookup"><span data-stu-id="b705d-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="b705d-126">Miglioramento delle barre di scorrimento Flat</span><span class="sxs-lookup"><span data-stu-id="b705d-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="b705d-127">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente di modificare le barre di scorrimento flat per personalizzare l'aspetto della finestra.</span><span class="sxs-lookup"><span data-stu-id="b705d-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="b705d-128">Per le barre di scorrimento verticali è possibile modificare la larghezza della barra e l'altezza delle frecce di direzione.</span><span class="sxs-lookup"><span data-stu-id="b705d-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="b705d-129">Per le barre di scorrimento orizzontali, è possibile modificare l'altezza della barra e la larghezza delle frecce di direzione.</span><span class="sxs-lookup"><span data-stu-id="b705d-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="b705d-130">È anche possibile modificare il colore di sfondo delle barre di scorrimento orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="b705d-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="b705d-131">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente inoltre di personalizzare il modo in cui vengono visualizzate le barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="b705d-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="b705d-132">Modificando le \_ Proprietà WSB Prop \_ VSTYLE e WSB \_ prop \_ HSTYLE è possibile impostare il tipo di barra di scorrimento che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b705d-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="b705d-133">Sono disponibili tre stili.</span><span class="sxs-lookup"><span data-stu-id="b705d-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b705d-134">\_modalità Encarta di FSB \_</span><span class="sxs-lookup"><span data-stu-id="b705d-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="b705d-135">Viene visualizzata una barra di scorrimento flat standard.</span><span class="sxs-lookup"><span data-stu-id="b705d-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="b705d-136">Quando il mouse viene spostato su un pulsante di direzione o sul pollice, tale parte della barra di scorrimento verrà visualizzata in 3D.</span><span class="sxs-lookup"><span data-stu-id="b705d-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="b705d-137">\_modalità flat di FSB \_</span><span class="sxs-lookup"><span data-stu-id="b705d-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="b705d-138">Viene visualizzata una barra di scorrimento flat standard.</span><span class="sxs-lookup"><span data-stu-id="b705d-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="b705d-139">Quando il mouse viene spostato su un pulsante di direzione o sul pollice, tale parte della barra di scorrimento verrà visualizzata in colori invertiti.</span><span class="sxs-lookup"><span data-stu-id="b705d-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="b705d-140">\_modalità normale \_ FSB</span><span class="sxs-lookup"><span data-stu-id="b705d-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="b705d-141">Viene visualizzata una barra di scorrimento normale e non semplice.</span><span class="sxs-lookup"><span data-stu-id="b705d-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="b705d-142">Non verrà applicato alcun effetto visivo speciale.</span><span class="sxs-lookup"><span data-stu-id="b705d-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="b705d-143">Rimozione di barre di scorrimento Flat</span><span class="sxs-lookup"><span data-stu-id="b705d-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="b705d-144">Se si desidera rimuovere barre di scorrimento Flat dalla finestra, chiamare la funzione [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , passando l'handle alla finestra.</span><span class="sxs-lookup"><span data-stu-id="b705d-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="b705d-145">Questa funzione rimuove solo le barre di scorrimento semplici dalla finestra in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b705d-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="b705d-146">Quando la finestra viene distrutta, non è necessario chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b705d-146">You do not need to call this function when your window is destroyed.</span></span>

 

 