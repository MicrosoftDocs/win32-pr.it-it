---
title: Casella di gruppo (riferimento all'elemento MSAA UI)
description: Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712571"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="f703f-103">Casella di gruppo (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="f703f-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="f703f-104">Questo argomento descrive gli oggetti **casella di gruppo** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="f703f-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="f703f-105">La creazione di oggetti **casella di gruppo** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="f703f-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="f703f-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="f703f-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="f703f-107">Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).</span><span class="sxs-lookup"><span data-stu-id="f703f-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="f703f-108">L'unico scopo di una casella di gruppo è organizzare i controlli correlati da uno scopo comune, indicato dall'etichetta.</span><span class="sxs-lookup"><span data-stu-id="f703f-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="f703f-109">Il nome della classe della finestra per una casella di gruppo è "BUTTON".</span><span class="sxs-lookup"><span data-stu-id="f703f-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="f703f-110">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="f703f-110">IAccessible Methods</span></span>

<span data-ttu-id="f703f-111">Una casella di gruppo supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f703f-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="f703f-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="f703f-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="f703f-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="f703f-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="f703f-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="f703f-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="f703f-115">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="f703f-115">IAccessible Properties</span></span>

<span data-ttu-id="f703f-116">Una casella di gruppo supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="f703f-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="f703f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f703f-117">Property</span></span>                                                                             | <span data-ttu-id="f703f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f703f-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f703f-119">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="f703f-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="f703f-120">La proprietà **childCount** è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="f703f-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f703f-121">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="f703f-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f703f-122">**ottenere \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="f703f-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="f703f-123">Le caselle di gruppo non dispongono di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f703f-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="f703f-124">Tuttavia, se il testo della finestra per la casella di gruppo contiene un carattere e commerciale (&), Microsoft Active Accessibility restituisce una stringa non null come proprietà **KeyboardShortcut** .</span><span class="sxs-lookup"><span data-stu-id="f703f-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f703f-125">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f703f-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="f703f-126">La proprietà **Name** viene ottenuta dal testo della finestra del controllo (o didascalia), visualizzata con la casella di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f703f-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f703f-127">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="f703f-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="f703f-128">La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="f703f-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f703f-129">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="f703f-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="f703f-130">La proprietà **Role** è [**il \_ \_ raggruppamento del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f703f-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f703f-131">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="f703f-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="f703f-132">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="f703f-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f703f-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f703f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f703f-134">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f703f-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





