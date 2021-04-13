---
title: Group (Framework della barra multifunzione di Windows)
description: Il gruppo organizza i comandi e i controlli correlati all'interno di una scheda.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400173"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="b388d-103">Group (Framework della barra multifunzione di Windows)</span><span class="sxs-lookup"><span data-stu-id="b388d-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="b388d-104">Il gruppo organizza i comandi e i controlli correlati all'interno di una [scheda](windowsribbon-controls-tab.md).</span><span class="sxs-lookup"><span data-stu-id="b388d-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="b388d-105">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b388d-105">Details</span></span>](#details)
-   [<span data-ttu-id="b388d-106">Proprietà gruppo</span><span class="sxs-lookup"><span data-stu-id="b388d-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="b388d-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b388d-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="b388d-108">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b388d-108">Details</span></span>

<span data-ttu-id="b388d-109">Lo screenshot seguente illustra il controllo gruppo della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="b388d-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![screenshot con callout che mostra un gruppo.](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="b388d-111">Proprietà gruppo</span><span class="sxs-lookup"><span data-stu-id="b388d-111">Group Properties</span></span>

<span data-ttu-id="b388d-112">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo gruppo.</span><span class="sxs-lookup"><span data-stu-id="b388d-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="b388d-113">In genere, una proprietà del gruppo viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="b388d-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="b388d-114">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="b388d-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="b388d-115">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="b388d-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="b388d-116">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="b388d-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="b388d-117">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="b388d-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="b388d-118">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo gruppo.</span><span class="sxs-lookup"><span data-stu-id="b388d-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b388d-119">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="b388d-119">Property Key</span></span></th>
<th><span data-ttu-id="b388d-120">Note</span><span class="sxs-lookup"><span data-stu-id="b388d-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b388d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="b388d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="b388d-122">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b388d-123">Per il Framework è necessario che il valore di <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> per un controllo gruppo inizi con la lettera maiuscola Z. Se il valore fornito dall'applicazione nel metodo di callback <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler:: UpdateProperty</strong></a> non inizia con la lettera Z, questo valore viene ignorato e viene invece generato un valore dal Framework.</span><span class="sxs-lookup"><span data-stu-id="b388d-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="b388d-124">Il valore del Framework è la lettera Z seguita da un valore numerico a partire da 1 e che aumenta in modo sequenziale, come richiesto, per i controlli gruppo successivi (Z1, Z2,..., ZX).</span><span class="sxs-lookup"><span data-stu-id="b388d-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b388d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="b388d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="b388d-126">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b388d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="b388d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="b388d-128">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b388d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="b388d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="b388d-130">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b388d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="b388d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="b388d-132">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b388d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="b388d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="b388d-134">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b388d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="b388d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="b388d-136">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b388d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="b388d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="b388d-138">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="b388d-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b388d-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b388d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b388d-140">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="b388d-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="b388d-141">**Group - elemento**</span><span class="sxs-lookup"><span data-stu-id="b388d-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

