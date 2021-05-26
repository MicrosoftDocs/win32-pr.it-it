---
title: Barre di scorrimento flat
description: Microsoft Internet Explorer 4.0 ha introdotto una nuova tecnologia visiva denominata barre di scorrimento flat.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423891"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="92278-103">Barre di scorrimento flat</span><span class="sxs-lookup"><span data-stu-id="92278-103">Flat Scroll Bars</span></span>

<span data-ttu-id="92278-104">Microsoft Internet Explorer 4.0 ha introdotto una nuova tecnologia visiva denominata barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="92278-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="92278-105">Dal punto di vista funzionale, le barre di scorrimento flat si comportano esattamente come le barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="92278-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="92278-106">La differenza è che è possibile personalizzarne l'aspetto in misura maggiore rispetto alle barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="92278-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="92278-107">La figura seguente mostra una finestra che contiene una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="92278-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![Screenshot di una finestra che contiene una barra di scorrimento semplice](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="92278-109">Le barre di scorrimento flat sono supportate Comctl32.dll versioni da 4.71 a 5.82.</span><span class="sxs-lookup"><span data-stu-id="92278-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="92278-110">Comctl32.dll versioni 6.00 e successive non supportano barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="92278-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="92278-111">Uso di barre di scorrimento flat</span><span class="sxs-lookup"><span data-stu-id="92278-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="92278-112">Questa sezione descrive come implementare barre di scorrimento flat nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92278-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="92278-113">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="92278-113">Before You Begin</span></span>

<span data-ttu-id="92278-114">Per usare le funzioni della barra di scorrimento flat, è necessario includere Commctrl.h nei file di origine e collegarsi a Comctl32.lib.</span><span class="sxs-lookup"><span data-stu-id="92278-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="92278-115">Aggiunta di barre di scorrimento flat a una finestra</span><span class="sxs-lookup"><span data-stu-id="92278-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="92278-116">Per aggiungere barre di scorrimento flat a una finestra, chiamare [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando l'handle alla finestra.</span><span class="sxs-lookup"><span data-stu-id="92278-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="92278-117">Anziché usare le funzioni standard della barra di scorrimento per modificare le barre di scorrimento, è necessario usare la funzione XXX FlatSB \_ equivalente.</span><span class="sxs-lookup"><span data-stu-id="92278-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="92278-118">Sono disponibili funzioni della barra di scorrimento flat per l'impostazione e il recupero delle informazioni di scorrimento, dell'intervallo e della posizione.</span><span class="sxs-lookup"><span data-stu-id="92278-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="92278-119">Se le barre di scorrimento flat non sono state inizializzate per la finestra, l'API della barra di scorrimento flat rimanda alle funzioni standard corrispondenti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="92278-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="92278-120">In questo modo è possibile attivare e disattivare le barre di scorrimento flat senza dover scrivere codice condizionale.</span><span class="sxs-lookup"><span data-stu-id="92278-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="92278-121">Poiché un'applicazione può aver impostato metriche personalizzate per le barre di scorrimento flat, non vengono aggiornate automaticamente quando le metriche di sistema cambiano.</span><span class="sxs-lookup"><span data-stu-id="92278-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="92278-122">Quando le metriche della barra di scorrimento del sistema cambiano, viene trasmesso un messaggio [**WM \_ SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) con *wParam* impostato su [**SPI \_ SETNONCLIENTMETRICS.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)</span><span class="sxs-lookup"><span data-stu-id="92278-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="92278-123">Per aggiornare le barre di scorrimento flat alle nuove metriche di sistema, le applicazioni devono gestire questo messaggio e modificare in modo esplicito le proprietà dipendenti dalla metrica della barra di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="92278-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="92278-124">Per aggiornare le proprietà della barra di scorrimento, [**usare FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="92278-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="92278-125">Il frammento di codice seguente modifica le proprietà dipendenti dalla metrica di una barra di scorrimento semplice nei valori di sistema correnti.</span><span class="sxs-lookup"><span data-stu-id="92278-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


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



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="92278-126">Miglioramento delle barre di scorrimento flat</span><span class="sxs-lookup"><span data-stu-id="92278-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="92278-127">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente di modificare le barre di scorrimento flat per personalizzare l'aspetto della finestra.</span><span class="sxs-lookup"><span data-stu-id="92278-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="92278-128">Per le barre di scorrimento verticali, è possibile modificare la larghezza della barra e l'altezza delle frecce di direzione.</span><span class="sxs-lookup"><span data-stu-id="92278-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="92278-129">Per le barre di scorrimento orizzontali, è possibile modificare l'altezza della barra e la larghezza delle frecce di direzione.</span><span class="sxs-lookup"><span data-stu-id="92278-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="92278-130">È anche possibile modificare il colore di sfondo delle barre di scorrimento orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="92278-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="92278-131">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente anche di personalizzare la modalità di visualizzazione delle barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="92278-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="92278-132">Modificando le proprietà WSB PROP VSTYLE e \_ \_ WSB \_ PROP HSTYLE, è possibile impostare il tipo di barra di scorrimento \_ da usare.</span><span class="sxs-lookup"><span data-stu-id="92278-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="92278-133">Sono disponibili tre stili.</span><span class="sxs-lookup"><span data-stu-id="92278-133">Three styles are available.</span></span>



|   <span data-ttu-id="92278-134">Stile</span><span class="sxs-lookup"><span data-stu-id="92278-134">Style</span></span>                 |   <span data-ttu-id="92278-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92278-135">Description</span></span>                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92278-136">MODALITÀ \_ FSB \_ ENCARTA</span><span class="sxs-lookup"><span data-stu-id="92278-136">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="92278-137">Viene visualizzata una barra di scorrimento semplice standard.</span><span class="sxs-lookup"><span data-stu-id="92278-137">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="92278-138">Quando il mouse si sposta su un pulsante di direzione o sul cursore, tale parte della barra di scorrimento verrà visualizzata in 3D.</span><span class="sxs-lookup"><span data-stu-id="92278-138">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="92278-139">FSB \_ FLAT \_ MODE</span><span class="sxs-lookup"><span data-stu-id="92278-139">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="92278-140">Viene visualizzata una barra di scorrimento semplice standard.</span><span class="sxs-lookup"><span data-stu-id="92278-140">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="92278-141">Quando il mouse si sposta su un pulsante di direzione o sul cursore, tale parte della barra di scorrimento verrà visualizzata con colori invertiti.</span><span class="sxs-lookup"><span data-stu-id="92278-141">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="92278-142">MODALITÀ REGOLARE \_ \_ FSB</span><span class="sxs-lookup"><span data-stu-id="92278-142">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="92278-143">Viene visualizzata una barra di scorrimento normale e nonflat.</span><span class="sxs-lookup"><span data-stu-id="92278-143">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="92278-144">Non verrà applicato alcun effetto visivo speciale.</span><span class="sxs-lookup"><span data-stu-id="92278-144">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="92278-145">Rimozione di barre di scorrimento flat</span><span class="sxs-lookup"><span data-stu-id="92278-145">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="92278-146">Per rimuovere le barre di scorrimento flat dalla finestra, chiamare la [**funzione UninitializeFlatSB,**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) passando l'handle alla finestra.</span><span class="sxs-lookup"><span data-stu-id="92278-146">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="92278-147">Questa funzione rimuove le barre di scorrimento flat dalla finestra solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92278-147">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="92278-148">Non è necessario chiamare questa funzione quando la finestra viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="92278-148">You do not need to call this function when your window is destroyed.</span></span>

 

 