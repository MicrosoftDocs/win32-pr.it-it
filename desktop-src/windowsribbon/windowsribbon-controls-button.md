---
title: Button (Framework della barra multifunzione di Windows)
description: Il pulsante è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118751"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="1b87c-103">Button (Framework della barra multifunzione di Windows)</span><span class="sxs-lookup"><span data-stu-id="1b87c-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="1b87c-104">Il pulsante è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b87c-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="1b87c-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="1b87c-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="1b87c-106">Proprietà pulsante</span><span class="sxs-lookup"><span data-stu-id="1b87c-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="1b87c-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b87c-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="1b87c-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="1b87c-108">Introduction</span></span>

<span data-ttu-id="1b87c-109">Lo screenshot seguente contiene tre esempi dell'elemento Button della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1b87c-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![screenshot dei controlli Button nella barra multifunzione di Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="1b87c-111">Proprietà pulsante</span><span class="sxs-lookup"><span data-stu-id="1b87c-111">Button Properties</span></span>

<span data-ttu-id="1b87c-112">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Button.</span><span class="sxs-lookup"><span data-stu-id="1b87c-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="1b87c-113">In genere, una proprietà Button viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="1b87c-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="1b87c-114">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="1b87c-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="1b87c-115">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="1b87c-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="1b87c-116">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="1b87c-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="1b87c-117">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="1b87c-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="1b87c-118">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Button.</span><span class="sxs-lookup"><span data-stu-id="1b87c-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="1b87c-119">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="1b87c-119">Property Key</span></span>                                                                                             | <span data-ttu-id="1b87c-120">Note</span><span class="sxs-lookup"><span data-stu-id="1b87c-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b87c-121">Interfaccia utente \_ pkey \_ abilitata</span><span class="sxs-lookup"><span data-stu-id="1b87c-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="1b87c-122">Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="1b87c-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="1b87c-123">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="1b87c-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="1b87c-124">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-125">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="1b87c-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="1b87c-126">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-127">Interfaccia utente \_ pkey \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="1b87c-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="1b87c-128">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-129">Interfaccia utente \_ pkey \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="1b87c-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="1b87c-130">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-131">Interfaccia utente \_ pkey \_ largeImage</span><span class="sxs-lookup"><span data-stu-id="1b87c-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="1b87c-132">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-133">Interfaccia utente \_ pkey \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="1b87c-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="1b87c-134">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-135">Interfaccia utente \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="1b87c-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="1b87c-136">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-137">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="1b87c-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="1b87c-138">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="1b87c-139">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="1b87c-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="1b87c-140">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="1b87c-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="1b87c-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b87c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b87c-142">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="1b87c-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="1b87c-143">**Elemento markup Button**</span><span class="sxs-lookup"><span data-stu-id="1b87c-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
