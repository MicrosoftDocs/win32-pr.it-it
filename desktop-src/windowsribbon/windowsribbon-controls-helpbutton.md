---
title: Pulsante della Guida
description: Il pulsante? è un controllo su cui l'utente può fare clic per visualizzare il sistema di guida dell'applicazione.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963101"
---
# <a name="help-button"></a><span data-ttu-id="33d40-103">Pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="33d40-103">Help Button</span></span>

<span data-ttu-id="33d40-104">Il pulsante? è un controllo su cui l'utente può fare clic per visualizzare il sistema di guida dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33d40-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="33d40-105">Dettagli</span><span class="sxs-lookup"><span data-stu-id="33d40-105">Details</span></span>](#details)
-   [<span data-ttu-id="33d40-106">Proprietà pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="33d40-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="33d40-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33d40-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="33d40-108">Dettagli</span><span class="sxs-lookup"><span data-stu-id="33d40-108">Details</span></span>

<span data-ttu-id="33d40-109">Lo screenshot seguente illustra il pulsante della guida della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="33d40-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![screenshot che mostra il pulsante della guida.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="33d40-111">Proprietà pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="33d40-111">Help Button Properties</span></span>

<span data-ttu-id="33d40-112">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo pulsante della guida.</span><span class="sxs-lookup"><span data-stu-id="33d40-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="33d40-113">In genere, la proprietà di un pulsante della guida viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="33d40-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="33d40-114">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="33d40-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="33d40-115">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="33d40-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="33d40-116">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="33d40-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="33d40-117">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="33d40-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="33d40-118">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo pulsante della guida.</span><span class="sxs-lookup"><span data-stu-id="33d40-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="33d40-119">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="33d40-119">Property Key</span></span>                                                                                     | <span data-ttu-id="33d40-120">Note</span><span class="sxs-lookup"><span data-stu-id="33d40-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="33d40-121">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="33d40-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="33d40-122">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="33d40-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="33d40-123">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="33d40-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="33d40-124">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="33d40-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="33d40-125">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="33d40-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="33d40-126">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="33d40-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="33d40-127">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="33d40-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="33d40-128">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="33d40-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="33d40-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33d40-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33d40-130">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="33d40-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="33d40-131">**Elemento HelpButton**</span><span class="sxs-lookup"><span data-stu-id="33d40-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 