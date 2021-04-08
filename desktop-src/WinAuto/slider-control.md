---
title: Controllo Slider (riferimento all'elemento MSAA UI)
description: Un controllo dispositivo di scorrimento, detto anche controllo TrackBar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento. I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045286"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="6c854-104">Controllo Slider (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="6c854-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="6c854-105">In questo argomento vengono descritti gli oggetti **controllo dispositivo di scorrimento** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="6c854-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="6c854-106">La procedura per la creazione di oggetti **controllo dispositivo di scorrimento** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="6c854-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="6c854-107">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="6c854-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="6c854-108">Un controllo dispositivo di scorrimento, detto anche controllo TrackBar, consente a un utente di selezionare da un intervallo di valori spostando un dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6c854-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="6c854-109">I controlli del volume disponibili nel sistema operativo Windows sono dispositivi di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6c854-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="6c854-110">Il nome della classe della finestra per un controllo dispositivo di scorrimento è la \_ classe TrackBar, definita come "msctls \_ TrackBar" in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="6c854-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="6c854-111">Il contenuto delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varia a seconda che il dispositivo di scorrimento sia verticale o orizzontale e che il client esegue una query sulle parti seguenti del controllo dispositivo di scorrimento:</span><span class="sxs-lookup"><span data-stu-id="6c854-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="6c854-112">Finestra del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-112">Slider window</span></span>
-   <span data-ttu-id="6c854-113">Cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-113">Slider thumb</span></span>
-   <span data-ttu-id="6c854-114">Area ombreggiata sopra (o</span><span class="sxs-lookup"><span data-stu-id="6c854-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="6c854-115">Area ombreggiata sotto (o a destra di) il cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="6c854-116">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="6c854-116">IAccessible Methods</span></span>

<span data-ttu-id="6c854-117">Un controllo dispositivo di scorrimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="6c854-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="6c854-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="6c854-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="6c854-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="6c854-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="6c854-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="6c854-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="6c854-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="6c854-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="6c854-122">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="6c854-122">IAccessible Properties</span></span>

<span data-ttu-id="6c854-123">Un controllo dispositivo di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c854-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="6c854-124">**ottenere \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="6c854-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="6c854-125">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="6c854-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="6c854-126">**ottenere \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="6c854-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="6c854-127">**ottenere \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="6c854-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="6c854-128">**ottenere \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="6c854-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="6c854-129">[**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la proprietà **KeyboardShortcut** è la chiave di accesso della finestra del dispositivo di scorrimento, che è un carattere sottolineato nel testo dell'etichetta per il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6c854-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="6c854-130">La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".</span><span class="sxs-lookup"><span data-stu-id="6c854-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="6c854-131">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la proprietà **Name** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="6c854-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="6c854-132">Le parti di un dispositivo di scorrimento verticale hanno i nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c854-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="6c854-133">Parte dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-133">Slider part</span></span>                    | <span data-ttu-id="6c854-134">Nome</span><span class="sxs-lookup"><span data-stu-id="6c854-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="6c854-135">Finestra del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-135">Slider window</span></span>                  | <span data-ttu-id="6c854-136">Controllo testo statico utilizzato come etichetta</span><span class="sxs-lookup"><span data-stu-id="6c854-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="6c854-137">Cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-137">Slider thumb</span></span>                   | <span data-ttu-id="6c854-138">Posizione</span><span class="sxs-lookup"><span data-stu-id="6c854-138">"Position"</span></span>                          |
    | <span data-ttu-id="6c854-139">Area ombreggiata sopra il cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="6c854-140">"PGSU"</span><span class="sxs-lookup"><span data-stu-id="6c854-140">"Page up"</span></span>                           |
    | <span data-ttu-id="6c854-141">Area ombreggiata sotto il cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="6c854-142">"PGGIÙ"</span><span class="sxs-lookup"><span data-stu-id="6c854-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="6c854-143">Le parti di un dispositivo di scorrimento orizzontale hanno i nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c854-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="6c854-144">Parte dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-144">Slider part</span></span>                              | <span data-ttu-id="6c854-145">Nome</span><span class="sxs-lookup"><span data-stu-id="6c854-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="6c854-146">Finestra del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-146">Slider window</span></span>                            | <span data-ttu-id="6c854-147">Controllo testo statico utilizzato come etichetta</span><span class="sxs-lookup"><span data-stu-id="6c854-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="6c854-148">Cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-148">Slider thumb</span></span>                             | <span data-ttu-id="6c854-149">Posizione</span><span class="sxs-lookup"><span data-stu-id="6c854-149">"Position"</span></span>                          |
    | <span data-ttu-id="6c854-150">Area ombreggiata a sinistra del cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="6c854-151">"Pagina a sinistra"</span><span class="sxs-lookup"><span data-stu-id="6c854-151">"Page left"</span></span>                         |
    | <span data-ttu-id="6c854-152">Area ombreggiata a destra del cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="6c854-153">"Pagina a destra"</span><span class="sxs-lookup"><span data-stu-id="6c854-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="6c854-154">[**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la proprietà **Parent** dei pulsanti di direzione, il cursore di scorrimento e l'area ombreggiata su entrambi i lati del controllo Thumb è la finestra del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6c854-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="6c854-155">La proprietà **Parent** della finestra del dispositivo di scorrimento è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe Window.</span><span class="sxs-lookup"><span data-stu-id="6c854-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="6c854-156">[**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** dipende dalla parte del dispositivo di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="6c854-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="6c854-157">Parte dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-157">Slider part</span></span>                                     | [<span data-ttu-id="6c854-158">Ruolo</span><span class="sxs-lookup"><span data-stu-id="6c854-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="6c854-159">Finestra del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-159">Slider window</span></span>                                   | [<span data-ttu-id="6c854-160">**\_dispositivo di \_ scorrimento sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="6c854-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="6c854-161">Cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-161">Slider thumb</span></span>                                    | [<span data-ttu-id="6c854-162">**\_indicatore del sistema di ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="6c854-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="6c854-163">Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="6c854-164">**\_pulsante sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="6c854-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="6c854-165">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate):[i valori](object-state-constants.md) per la proprietà **state** dipendono dalla parte del dispositivo di scorrimento su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="6c854-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="6c854-166">Parte dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-166">Slider Part</span></span>                                     | <span data-ttu-id="6c854-167">Possibili valori di stato</span><span class="sxs-lookup"><span data-stu-id="6c854-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6c854-168">Finestra del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-168">Slider window</span></span>                                   | <span data-ttu-id="6c854-169">[**Stato \_ di sistema stato \_ invisibile**](object-state-constants.md) al sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema</span><span class="sxs-lookup"><span data-stu-id="6c854-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="6c854-170">Cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-170">Slider thumb</span></span>                                    | <span data-ttu-id="6c854-171">Zero (0), che indica che l'oggetto è visibile oppure che lo stato del sistema di stato [**\_ \_ invisibile**](object-state-constants.md) al sistema dello stato non è \| [**\_ \_ disponibile**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="6c854-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="6c854-172">Aree ombreggiate su entrambi i lati del cursore del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6c854-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="6c854-173">Zero (0), che indica che l'oggetto è visibile oppure che lo stato del sistema di stato [**\_ \_ invisibile**](object-state-constants.md) al sistema dello stato non è \| [**\_ \_ disponibile**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="6c854-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="6c854-174">[**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la proprietà **value** per la finestra del dispositivo di scorrimento indica la posizione del cursore e è una stringa che contiene un numero intero compreso tra "0" e "100".</span><span class="sxs-lookup"><span data-stu-id="6c854-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c854-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c854-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c854-176">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="6c854-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="6c854-177">**Barra di scorrimento**</span><span class="sxs-lookup"><span data-stu-id="6c854-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




