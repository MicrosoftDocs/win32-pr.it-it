---
title: Testo statico (riferimento all'elemento dell'interfaccia utente MSAA)
description: I controlli di testo statici rappresentano un modo pratico per visualizzare il testo nelle finestre di dialogo e altre finestre. I controlli di testo statici spesso vengono usati come etichette per altri controlli.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856858"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="81959-104">Testo statico (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="81959-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="81959-105">I controlli di testo statici rappresentano un modo pratico per visualizzare il testo nelle finestre di dialogo e altre finestre.</span><span class="sxs-lookup"><span data-stu-id="81959-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="81959-106">I controlli di testo statici spesso vengono usati come etichette per altri controlli.</span><span class="sxs-lookup"><span data-stu-id="81959-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="81959-107">Il nome della classe della finestra per un controllo testo statico è "STATIC".</span><span class="sxs-lookup"><span data-stu-id="81959-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="81959-108">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="81959-108">IAccessible Methods</span></span>

<span data-ttu-id="81959-109">I controlli di testo statici supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="81959-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="81959-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="81959-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="81959-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="81959-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="81959-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="81959-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="81959-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="81959-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="81959-114">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="81959-114">IAccessible Properties</span></span>

<span data-ttu-id="81959-115">I controlli di testo statici supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="81959-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="81959-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81959-116">Property</span></span>                                                                             | <span data-ttu-id="81959-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="81959-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81959-118">**ottenere \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="81959-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="81959-119">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="81959-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="81959-120">La proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="81959-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="81959-121">**ottenere \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="81959-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="81959-122">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="81959-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="81959-123">**ottenere \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="81959-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="81959-124">**ottenere \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="81959-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="81959-125">**ottenere \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="81959-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="81959-126">La proprietà **KeyboardShortcut** è la chiave di accesso, ovvero il carattere sottolineato nel testo che attiva il controllo associato al testo statico.</span><span class="sxs-lookup"><span data-stu-id="81959-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="81959-127">La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".</span><span class="sxs-lookup"><span data-stu-id="81959-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="81959-128">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="81959-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="81959-129">La proprietà **Name** corrisponde al testo nel controllo testo statico.</span><span class="sxs-lookup"><span data-stu-id="81959-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="81959-130">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="81959-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="81959-131">La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="81959-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="81959-132">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="81959-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="81959-133">La proprietà **Role** è [**\_ \_ STATICTEXT del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="81959-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="81959-134">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="81959-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="81959-135">La proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: sistema di stato di sola [**\_ \_ lettura stato sistema di stato**](object-state-constants.md) \| [**\_ \_ invisibile**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="81959-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="81959-136">Note</span><span class="sxs-lookup"><span data-stu-id="81959-136">Notes</span></span>

-   <span data-ttu-id="81959-137">Il metodo [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) restituisce disp \_ E \_ MEMBERNOTFOUND quando viene chiamato con [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto testo statico.</span><span class="sxs-lookup"><span data-stu-id="81959-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="81959-138">I controlli statici con lo \_ stile dell'icona SS restituiscono dati non validi nella proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="81959-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81959-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81959-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81959-140">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="81959-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





