---
title: Barra di scorrimento (riferimento all'elemento dell'interfaccia utente MSAA)
description: Le barre di scorrimento consentono a un utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata. Il nome della classe della finestra per una barra di scorrimento è \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047305"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="16f39-104">Barra di scorrimento (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="16f39-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="16f39-105">Questo argomento descrive gli oggetti **barra di scorrimento** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="16f39-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="16f39-106">La creazione di oggetti **barra di scorrimento** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="16f39-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="16f39-107">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="16f39-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="16f39-108">Le barre di scorrimento consentono a un utente di scegliere la direzione e la distanza per scorrere le informazioni in una finestra o in una casella di riepilogo correlata.</span><span class="sxs-lookup"><span data-stu-id="16f39-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="16f39-109">Il nome della classe della finestra per una barra di scorrimento è "SCROLLBAR".</span><span class="sxs-lookup"><span data-stu-id="16f39-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="16f39-110">Il contenuto delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varia a seconda che la barra di scorrimento sia verticale o orizzontale e su quale delle parti seguenti della barra di scorrimento venga eseguita una query da parte del client:</span><span class="sxs-lookup"><span data-stu-id="16f39-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="16f39-111">Barra di scorrimento stessa</span><span class="sxs-lookup"><span data-stu-id="16f39-111">The scroll bar itself</span></span>
-   <span data-ttu-id="16f39-112">Pulsante freccia in alto o a destra</span><span class="sxs-lookup"><span data-stu-id="16f39-112">The top or right arrow button</span></span>
-   <span data-ttu-id="16f39-113">Pulsante freccia in basso o a sinistra</span><span class="sxs-lookup"><span data-stu-id="16f39-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="16f39-114">Casella di scorrimento (Thumb)</span><span class="sxs-lookup"><span data-stu-id="16f39-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="16f39-115">Area in alto o a destra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-115">The page up or page right region</span></span>
-   <span data-ttu-id="16f39-116">La pagina verso il basso o l'area a sinistra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="16f39-117">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="16f39-117">IAccessible Methods</span></span>

<span data-ttu-id="16f39-118">Una barra di scorrimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="16f39-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="16f39-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): l'oggetto barra di scorrimento e il cursore di scorrimento non supportano il metodo **accDoDefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="16f39-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="16f39-120">Per le altre parti della barra di scorrimento in una barra di scorrimento verticale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) con *wParam* impostato sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="16f39-121">Pulsante/area</span><span class="sxs-lookup"><span data-stu-id="16f39-121">Button/Region</span></span>       | <span data-ttu-id="16f39-122">Vaule</span><span class="sxs-lookup"><span data-stu-id="16f39-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="16f39-123">Pulsante freccia in alto</span><span class="sxs-lookup"><span data-stu-id="16f39-123">Top arrow button</span></span>    | <span data-ttu-id="16f39-124">\_lineup SB</span><span class="sxs-lookup"><span data-stu-id="16f39-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="16f39-125">Pulsante freccia in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-125">Bottom arrow button</span></span> | <span data-ttu-id="16f39-126">\_LINEDOWN SB</span><span class="sxs-lookup"><span data-stu-id="16f39-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="16f39-127">Area di paging</span><span class="sxs-lookup"><span data-stu-id="16f39-127">Page up region</span></span>      | <span data-ttu-id="16f39-128">\_PAGEUP SB</span><span class="sxs-lookup"><span data-stu-id="16f39-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="16f39-129">Area in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-129">Page down region</span></span>    | <span data-ttu-id="16f39-130">\_PGGIÙ SB</span><span class="sxs-lookup"><span data-stu-id="16f39-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="16f39-131">Per le altre parti della barra di scorrimento in una barra di scorrimento orizzontale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) con *wParam* impostato sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="16f39-132">Pulsante/area</span><span class="sxs-lookup"><span data-stu-id="16f39-132">Button/Region</span></span>      | <span data-ttu-id="16f39-133">Valore</span><span class="sxs-lookup"><span data-stu-id="16f39-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="16f39-134">Pulsante freccia sinistra</span><span class="sxs-lookup"><span data-stu-id="16f39-134">Left arrow button</span></span>  | <span data-ttu-id="16f39-135">\_LINELEFT SB</span><span class="sxs-lookup"><span data-stu-id="16f39-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="16f39-136">Pulsante freccia destra</span><span class="sxs-lookup"><span data-stu-id="16f39-136">Right arrow button</span></span> | <span data-ttu-id="16f39-137">\_LINERIGHT SB</span><span class="sxs-lookup"><span data-stu-id="16f39-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="16f39-138">Area a sinistra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-138">Page left region</span></span>   | <span data-ttu-id="16f39-139">\_PAGELEFT SB</span><span class="sxs-lookup"><span data-stu-id="16f39-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="16f39-140">Area a destra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-140">Page right region</span></span>  | <span data-ttu-id="16f39-141">\_PAGERIGHT SB</span><span class="sxs-lookup"><span data-stu-id="16f39-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="16f39-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="16f39-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="16f39-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="16f39-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="16f39-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="16f39-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="16f39-145">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="16f39-145">IAccessible Properties</span></span>

<span data-ttu-id="16f39-146">Una barra di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="16f39-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="16f39-147">[**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la proprietà **childCount** per l'oggetto barra di scorrimento è cinque.</span><span class="sxs-lookup"><span data-stu-id="16f39-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="16f39-148">Per le altre parti della barra di scorrimento, la proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="16f39-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="16f39-149">[**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): l'oggetto barra di scorrimento e il cursore di scorrimento non supportano la proprietà **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="16f39-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="16f39-150">La proprietà **DefaultAction** per i pulsanti freccia e le aree ombreggiate su entrambi i lati del cursore di scorrimento è "premere".</span><span class="sxs-lookup"><span data-stu-id="16f39-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="16f39-151">[**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription): la proprietà **Description** dipende dalla parte della barra di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="16f39-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="16f39-152">Le parti di una barra di scorrimento verticale hanno le descrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="16f39-153">Parte</span><span class="sxs-lookup"><span data-stu-id="16f39-153">Part</span></span>                | <span data-ttu-id="16f39-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16f39-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="16f39-155">Barra di scorrimento stessa</span><span class="sxs-lookup"><span data-stu-id="16f39-155">Scroll bar itself</span></span>   | <span data-ttu-id="16f39-156">"Usato per modificare l'area di visualizzazione verticale"</span><span class="sxs-lookup"><span data-stu-id="16f39-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="16f39-157">Pulsante freccia in alto</span><span class="sxs-lookup"><span data-stu-id="16f39-157">Top arrow button</span></span>    | <span data-ttu-id="16f39-158">"Sposta la posizione verticale verso l'alto di una riga"</span><span class="sxs-lookup"><span data-stu-id="16f39-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="16f39-159">Pulsante freccia in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-159">Bottom arrow button</span></span> | <span data-ttu-id="16f39-160">"Sposta la posizione verticale verso il basso di una riga"</span><span class="sxs-lookup"><span data-stu-id="16f39-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="16f39-161">Cursore di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-161">Scroll thumb</span></span>        | <span data-ttu-id="16f39-162">"Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente".</span><span class="sxs-lookup"><span data-stu-id="16f39-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="16f39-163">Area di paging</span><span class="sxs-lookup"><span data-stu-id="16f39-163">Page up region</span></span>      | <span data-ttu-id="16f39-164">"Sposta la posizione verticale verso l'alto di un paio di righe"</span><span class="sxs-lookup"><span data-stu-id="16f39-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="16f39-165">Area in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-165">Page down region</span></span>    | <span data-ttu-id="16f39-166">"Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente".</span><span class="sxs-lookup"><span data-stu-id="16f39-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="16f39-167">Le parti di una barra di scorrimento orizzontale hanno le descrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="16f39-168">Parte</span><span class="sxs-lookup"><span data-stu-id="16f39-168">Part</span></span>               | <span data-ttu-id="16f39-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16f39-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="16f39-170">Barra di scorrimento stessa</span><span class="sxs-lookup"><span data-stu-id="16f39-170">Scroll bar itself</span></span>  | <span data-ttu-id="16f39-171">"Usato per modificare l'area di visualizzazione orizzontale"</span><span class="sxs-lookup"><span data-stu-id="16f39-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="16f39-172">Pulsante freccia sinistra</span><span class="sxs-lookup"><span data-stu-id="16f39-172">Left arrow button</span></span>  | <span data-ttu-id="16f39-173">"Sposta la posizione orizzontale a sinistra di una colonna"</span><span class="sxs-lookup"><span data-stu-id="16f39-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="16f39-174">Pulsante freccia destra</span><span class="sxs-lookup"><span data-stu-id="16f39-174">Right arrow button</span></span> | <span data-ttu-id="16f39-175">' Sposta la posizione orizzontale a destra di una colonna "</span><span class="sxs-lookup"><span data-stu-id="16f39-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="16f39-176">Cursore di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-176">Scroll thumb</span></span>       | <span data-ttu-id="16f39-177">"Indica la posizione orizzontale corrente e può essere trascinata per modificarla direttamente".</span><span class="sxs-lookup"><span data-stu-id="16f39-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="16f39-178">Area a sinistra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-178">Page left region</span></span>   | <span data-ttu-id="16f39-179">"Sposta la posizione orizzontale a sinistra di un paio di colonne"</span><span class="sxs-lookup"><span data-stu-id="16f39-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="16f39-180">Area a destra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-180">Page right region</span></span>  | <span data-ttu-id="16f39-181">"Indica la posizione verticale corrente e può essere trascinata per modificarla direttamente".</span><span class="sxs-lookup"><span data-stu-id="16f39-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="16f39-182">**ottenere \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="16f39-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="16f39-183">**ottenere \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="16f39-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="16f39-184">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la proprietà **Name** dipende dalla parte della barra di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="16f39-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="16f39-185">I nomi delle parti di una barra di scorrimento verticale sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="16f39-186">Parte</span><span class="sxs-lookup"><span data-stu-id="16f39-186">Part</span></span>                | <span data-ttu-id="16f39-187">Nome</span><span class="sxs-lookup"><span data-stu-id="16f39-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="16f39-188">Finestra della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-188">Scroll bar window</span></span>   | <span data-ttu-id="16f39-189">Verticale</span><span class="sxs-lookup"><span data-stu-id="16f39-189">"Vertical"</span></span>  |
    | <span data-ttu-id="16f39-190">Pulsante freccia in alto</span><span class="sxs-lookup"><span data-stu-id="16f39-190">Top arrow button</span></span>    | <span data-ttu-id="16f39-191">"Riga su"</span><span class="sxs-lookup"><span data-stu-id="16f39-191">"Line up"</span></span>   |
    | <span data-ttu-id="16f39-192">Pulsante freccia in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-192">Bottom arrow button</span></span> | <span data-ttu-id="16f39-193">"Linea in basso"</span><span class="sxs-lookup"><span data-stu-id="16f39-193">"Line down"</span></span> |
    | <span data-ttu-id="16f39-194">Cursore di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-194">Scroll thumb</span></span>        | <span data-ttu-id="16f39-195">Posizione</span><span class="sxs-lookup"><span data-stu-id="16f39-195">"Position"</span></span>  |
    | <span data-ttu-id="16f39-196">Area di paging</span><span class="sxs-lookup"><span data-stu-id="16f39-196">Page up region</span></span>      | <span data-ttu-id="16f39-197">"PGSU"</span><span class="sxs-lookup"><span data-stu-id="16f39-197">"Page up"</span></span>   |
    | <span data-ttu-id="16f39-198">Area in basso</span><span class="sxs-lookup"><span data-stu-id="16f39-198">Page down region</span></span>    | <span data-ttu-id="16f39-199">"PGGIÙ"</span><span class="sxs-lookup"><span data-stu-id="16f39-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="16f39-200">I nomi delle parti di una barra di scorrimento orizzontale sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="16f39-201">Parte</span><span class="sxs-lookup"><span data-stu-id="16f39-201">Part</span></span>               | <span data-ttu-id="16f39-202">Nome</span><span class="sxs-lookup"><span data-stu-id="16f39-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="16f39-203">Finestra della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-203">Scroll bar window</span></span>  | <span data-ttu-id="16f39-204">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="16f39-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="16f39-205">Pulsante freccia sinistra</span><span class="sxs-lookup"><span data-stu-id="16f39-205">Left arrow button</span></span>  | <span data-ttu-id="16f39-206">"Colonna a sinistra"</span><span class="sxs-lookup"><span data-stu-id="16f39-206">"Column left"</span></span>  |
    | <span data-ttu-id="16f39-207">Pulsante freccia destra</span><span class="sxs-lookup"><span data-stu-id="16f39-207">Right arrow button</span></span> | <span data-ttu-id="16f39-208">"Colonna a destra"</span><span class="sxs-lookup"><span data-stu-id="16f39-208">"Column right"</span></span> |
    | <span data-ttu-id="16f39-209">Cursore di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-209">Scroll thumb</span></span>       | <span data-ttu-id="16f39-210">Posizione</span><span class="sxs-lookup"><span data-stu-id="16f39-210">"Position"</span></span>     |
    | <span data-ttu-id="16f39-211">Area a destra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-211">Page right region</span></span>  | <span data-ttu-id="16f39-212">"Pagina a destra"</span><span class="sxs-lookup"><span data-stu-id="16f39-212">"Page right"</span></span>   |
    | <span data-ttu-id="16f39-213">Area a sinistra della pagina</span><span class="sxs-lookup"><span data-stu-id="16f39-213">Page left region</span></span>   | <span data-ttu-id="16f39-214">"Pagina a sinistra"</span><span class="sxs-lookup"><span data-stu-id="16f39-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="16f39-215">[**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la proprietà **Parent** dei pulsanti di direzione, il cursore di scorrimento e l'area ombreggiata su entrambi i lati del cursore sono la finestra della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="16f39-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="16f39-216">La proprietà **Parent** della finestra della barra di scorrimento è una finestra ( \_ finestra del sistema \_ di ruoli) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe Window.</span><span class="sxs-lookup"><span data-stu-id="16f39-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="16f39-217">[**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** dipende dalla parte della barra di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="16f39-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="16f39-218">Le parti di una barra di scorrimento hanno i ruoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="16f39-219">Parte</span><span class="sxs-lookup"><span data-stu-id="16f39-219">Part</span></span>                                                  | <span data-ttu-id="16f39-220">Ruolo</span><span class="sxs-lookup"><span data-stu-id="16f39-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="16f39-221">Barra di scorrimento stessa</span><span class="sxs-lookup"><span data-stu-id="16f39-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="16f39-222">**\_barra di \_ scorrimento sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="16f39-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="16f39-223">Pulsanti freccia in alto, in basso, a sinistra e a destra</span><span class="sxs-lookup"><span data-stu-id="16f39-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="16f39-224">**\_pulsante sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="16f39-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="16f39-225">Cursore di scorrimento</span><span class="sxs-lookup"><span data-stu-id="16f39-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="16f39-226">**\_indicatore del sistema di ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="16f39-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="16f39-227">PGSU, PGGIÙ, pagina a sinistra e pagina a destra</span><span class="sxs-lookup"><span data-stu-id="16f39-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="16f39-228">**\_pulsante sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="16f39-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="16f39-229">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la proprietà **state** di ogni componente della barra di scorrimento include una combinazione dei [valori](object-state-constants.md)seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f39-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="16f39-230">State</span><span class="sxs-lookup"><span data-stu-id="16f39-230">State</span></span>                                                                                 | <span data-ttu-id="16f39-231">Valore</span><span class="sxs-lookup"><span data-stu-id="16f39-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="16f39-232">**sistema di stato \_ \_ invisibile**</span><span class="sxs-lookup"><span data-stu-id="16f39-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="16f39-233">Per la barra di scorrimento, indica che la barra di scorrimento verticale o orizzontale specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="16f39-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="16f39-234">Per le aree PGSU o PGGIÙ, questo indica che il cursore è posizionato in modo tale che l'area non esiste.</span><span class="sxs-lookup"><span data-stu-id="16f39-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="16f39-235">**\_Offscreen sistema di stato \_**</span><span class="sxs-lookup"><span data-stu-id="16f39-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="16f39-236">Per la barra di scorrimento, indica che la finestra è dimensionata in modo tale che la barra di scorrimento verticale o orizzontale specificata non sia attualmente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="16f39-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="16f39-237">**sistema di stato \_ \_ premuto**</span><span class="sxs-lookup"><span data-stu-id="16f39-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="16f39-238">Viene premuto il pulsante freccia o l'area della pagina.</span><span class="sxs-lookup"><span data-stu-id="16f39-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="16f39-239">**sistema di stato non \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="16f39-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="16f39-240">Il componente è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="16f39-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="16f39-241">[**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la proprietà **value** per la finestra della barra di scorrimento indica la posizione della barra di scorrimento e è una stringa che contiene un numero intero compreso tra "0" e "100".</span><span class="sxs-lookup"><span data-stu-id="16f39-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="16f39-242">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16f39-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f39-243">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="16f39-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 