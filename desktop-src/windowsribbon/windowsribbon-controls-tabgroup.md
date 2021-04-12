---
title: Gruppo di schede
description: Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro. Il gruppo di schede contiene un set di controlli scheda relativi al contesto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338639"
---
# <a name="tab-group"></a><span data-ttu-id="6bee2-104">Gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="6bee2-104">Tab Group</span></span>

<span data-ttu-id="6bee2-105">Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6bee2-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="6bee2-106">Il gruppo di schede contiene un set di controlli [scheda](windowsribbon-controls-tab.md) relativi al contesto.</span><span class="sxs-lookup"><span data-stu-id="6bee2-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="6bee2-107">Dettagli</span><span class="sxs-lookup"><span data-stu-id="6bee2-107">Details</span></span>](#details)
-   [<span data-ttu-id="6bee2-108">Proprietà gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="6bee2-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="6bee2-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bee2-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="6bee2-110">Dettagli</span><span class="sxs-lookup"><span data-stu-id="6bee2-110">Details</span></span>

<span data-ttu-id="6bee2-111">In genere, viene visualizzato un gruppo di schede durante gli stati specifici del documento o dell'area di lavoro, ad esempio quando un utente seleziona un determinato tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="6bee2-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="6bee2-112">Per la selezione di un'immagine contenuta nell'intestazione di una tabella, ad esempio, potrebbe essere necessario visualizzare diverse schede contestuali che espongono la funzionalità di tabella e immagine.</span><span class="sxs-lookup"><span data-stu-id="6bee2-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bee2-113">Un gruppo di schede non supporta le [modalità di applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="6bee2-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="6bee2-114">Tuttavia, i singoli controlli [scheda](windowsribbon-controls-tab.md) in un gruppo di schede possono.</span><span class="sxs-lookup"><span data-stu-id="6bee2-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="6bee2-115">Lo screenshot seguente mostra una [scheda](windowsribbon-controls-tab.md) contestuale del disegno di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6bee2-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![screenshot che mostra un controllo scheda contestuale.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="6bee2-117">Proprietà gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="6bee2-117">Tab Group Properties</span></span>

<span data-ttu-id="6bee2-118">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo gruppo di schede.</span><span class="sxs-lookup"><span data-stu-id="6bee2-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="6bee2-119">In genere, una proprietà del gruppo di schede viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="6bee2-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="6bee2-120">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="6bee2-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="6bee2-121">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="6bee2-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="6bee2-122">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="6bee2-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="6bee2-123">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="6bee2-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="6bee2-124">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo gruppo di schede.</span><span class="sxs-lookup"><span data-stu-id="6bee2-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="6bee2-125">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="6bee2-125">Property Key</span></span>                                                                                     | <span data-ttu-id="6bee2-126">Note</span><span class="sxs-lookup"><span data-stu-id="6bee2-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bee2-127">Interfaccia utente \_ pkey \_ ContextAvailable</span><span class="sxs-lookup"><span data-stu-id="6bee2-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="6bee2-128">Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="6bee2-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="6bee2-129">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="6bee2-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="6bee2-130">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="6bee2-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="6bee2-131">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="6bee2-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="6bee2-132">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="6bee2-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="6bee2-133">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="6bee2-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="6bee2-134">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="6bee2-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="6bee2-135">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="6bee2-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="6bee2-136">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="6bee2-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="6bee2-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bee2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bee2-138">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="6bee2-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="6bee2-139">**Elemento di markup TabGroup**</span><span class="sxs-lookup"><span data-stu-id="6bee2-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 