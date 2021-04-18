---
title: Tab (Framework della barra multifunzione di Windows)
description: Una scheda contiene gruppi di controlli correlati.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340252"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="8c4e8-103">Tab (Framework della barra multifunzione di Windows)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="8c4e8-104">Una scheda contiene [gruppi](windowsribbon-controls-group.md) di controlli correlati.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="8c4e8-105">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8c4e8-105">Details</span></span>](#details)
-   [<span data-ttu-id="8c4e8-106">Proprietà della scheda</span><span class="sxs-lookup"><span data-stu-id="8c4e8-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="8c4e8-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c4e8-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="8c4e8-108">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8c4e8-108">Details</span></span>

<span data-ttu-id="8c4e8-109">Sono disponibili tre tipi di scheda nel framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="8c4e8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c4e8-110">Type</span></span>               | <span data-ttu-id="8c4e8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c4e8-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4e8-112">**Scheda Core**</span><span class="sxs-lookup"><span data-stu-id="8c4e8-112">**Core tab**</span></span>       | <span data-ttu-id="8c4e8-113">Schede principali che consentono di organizzare le funzioni predefinite dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="8c4e8-114">**Scheda contestuale**</span><span class="sxs-lookup"><span data-stu-id="8c4e8-114">**Contextual tab**</span></span> | <span data-ttu-id="8c4e8-115">Schede visualizzate durante gli stati specifici del documento o dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="8c4e8-116">Se, ad esempio, un utente seleziona un particolare tipo di oggetto, ad esempio un'immagine contenuta nell'intestazione di una tabella, è possibile che vengano visualizzate varie schede contestuali che espongono le funzionalità di tabella e immagine.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="8c4e8-117">**Scheda modale**</span><span class="sxs-lookup"><span data-stu-id="8c4e8-117">**Modal tab**</span></span>      | <span data-ttu-id="8c4e8-118">Schede principali visualizzate durante una [modalità di applicazione](ribbon-applicationmodes.md)di un documento o di un'area di lavoro specifica, ad esempio anteprima di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="8c4e8-119">Lo screenshot seguente mostra una scheda di base di Paint di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![screenshot che mostra un controllo scheda principale.](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="8c4e8-121">Proprietà della scheda</span><span class="sxs-lookup"><span data-stu-id="8c4e8-121">Tab Properties</span></span>

<span data-ttu-id="8c4e8-122">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Tab.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="8c4e8-123">In genere, una proprietà di tabulazione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="8c4e8-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="8c4e8-124">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="8c4e8-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="8c4e8-125">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="8c4e8-126">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="8c4e8-127">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="8c4e8-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="8c4e8-128">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="8c4e8-129">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="8c4e8-129">Property Key</span></span>                                                                                     | <span data-ttu-id="8c4e8-130">Note</span><span class="sxs-lookup"><span data-stu-id="8c4e8-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="8c4e8-131">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="8c4e8-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="8c4e8-132">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="8c4e8-133">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="8c4e8-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="8c4e8-134">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="8c4e8-135">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="8c4e8-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="8c4e8-136">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="8c4e8-137">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="8c4e8-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="8c4e8-138">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c4e8-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c4e8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c4e8-140">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="8c4e8-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="8c4e8-141">**Elemento markup Tab**</span><span class="sxs-lookup"><span data-stu-id="8c4e8-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
