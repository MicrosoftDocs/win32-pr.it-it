---
title: Pulsante Drop-Down
description: Il pulsante Drop-Down è costituito da un pulsante che, se selezionato, Visualizza un elenco a discesa di elementi che si escludono a vicenda.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339470"
---
# <a name="drop-down-button"></a><span data-ttu-id="3a97a-103">Pulsante Drop-Down</span><span class="sxs-lookup"><span data-stu-id="3a97a-103">Drop-Down Button</span></span>

<span data-ttu-id="3a97a-104">Il pulsante Drop-Down è costituito da un pulsante che, se selezionato, Visualizza un elenco a discesa di elementi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="3a97a-104">The Drop-Down Button consists of a button that when clicked displays a drop-down list of mutually exclusive items.</span></span>

-   [<span data-ttu-id="3a97a-105">Dettagli</span><span class="sxs-lookup"><span data-stu-id="3a97a-105">Details</span></span>](#details)
-   [<span data-ttu-id="3a97a-106">Proprietà del pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="3a97a-106">Drop-Down Button Properties</span></span>](#drop-down-button-properties)
-   [<span data-ttu-id="3a97a-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a97a-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="3a97a-108">Dettagli</span><span class="sxs-lookup"><span data-stu-id="3a97a-108">Details</span></span>

<span data-ttu-id="3a97a-109">Questo controllo è utile per esporre elementi strettamente correlati nei casi in cui non sono disponibili impostazioni predefinite ovvie e in cui i singoli elementi possono essere rappresentati da un'immagine, un testo o entrambi.</span><span class="sxs-lookup"><span data-stu-id="3a97a-109">This control is useful for exposing closely related items in cases where no obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="3a97a-110">Lo screenshot seguente illustra il pulsante Drop-Down della barra multifunzione in una barra multifunzione di esempio.</span><span class="sxs-lookup"><span data-stu-id="3a97a-110">The following screen shot illustrates the Ribbon Drop-Down Button in a sample Ribbon.</span></span>

![Screenshot di un controllo DropDownButton in una barra multifunzione di esempio.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a><span data-ttu-id="3a97a-112">Proprietà del pulsante Drop-Down</span><span class="sxs-lookup"><span data-stu-id="3a97a-112">Drop-Down Button Properties</span></span>

<span data-ttu-id="3a97a-113">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo pulsante Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="3a97a-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Button control.</span></span>

<span data-ttu-id="3a97a-114">In genere, una proprietà del pulsante Drop-Down viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="3a97a-114">Typically, a Drop-Down Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="3a97a-115">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="3a97a-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="3a97a-116">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="3a97a-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="3a97a-117">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="3a97a-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="3a97a-118">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="3a97a-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="3a97a-119">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo del pulsante Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="3a97a-119">The following table lists the property keys that are associated with the Drop-Down Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a97a-120">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="3a97a-120">Property Key</span></span></th>
<th><span data-ttu-id="3a97a-121">Note</span><span class="sxs-lookup"><span data-stu-id="3a97a-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a97a-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="3a97a-123">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a97a-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="3a97a-125">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a97a-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="3a97a-126">Se tutti gli elementi figlio sono disabilitati, il Framework imposta <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> su false (0).</span><span class="sxs-lookup"><span data-stu-id="3a97a-126">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="3a97a-127">In caso contrario, se sono abilitati uno o più elementi figlio, UI_PKEY_Enabled viene impostato su true (-1).</span><span class="sxs-lookup"><span data-stu-id="3a97a-127">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="3a97a-128">La proprietà <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> per il controllo pulsante di Drop-Down deve essere invalidata dopo l'abilitazione o la disabilitazione di uno o più elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="3a97a-128">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Drop-Down Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="3a97a-129">In questo modo il Framework esegue una query sul valore della proprietà aggiornata e aggiorna lo stato del controllo Drop-Down pulsante nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="3a97a-129">This ensures that the framework queries the updated property value and refreshes the state of the Drop-Down Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a97a-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="3a97a-131">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a97a-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="3a97a-133">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a97a-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="3a97a-135">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="3a97a-137">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a97a-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="3a97a-139">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="3a97a-141">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a97a-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3a97a-142">Se il comando associato al controllo viene invalidato tramite una chiamata a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, il Framework esegue una query su questa proprietà quando <code>UI_INVALIDATIONS_VALUE</code> viene passato come valore di <em>flag</em>.</span><span class="sxs-lookup"><span data-stu-id="3a97a-142">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a97a-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="3a97a-144">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="3a97a-146">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a97a-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="3a97a-148">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a97a-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="3a97a-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="3a97a-150">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="3a97a-150">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3a97a-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a97a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a97a-152">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="3a97a-152">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="3a97a-153">**Elemento di markup DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="3a97a-153">**DropDownButton markup element**</span></span>](windowsribbon-element-dropdownbutton.md)
</dt> </dl>