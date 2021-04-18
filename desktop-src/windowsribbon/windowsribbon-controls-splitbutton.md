---
title: Pulsante di menu combinato
description: Il pulsante di suddivisione è un controllo composito con il quale l'utente può selezionare un valore predefinito associato a un pulsante primario oppure selezionare da un elenco di valori che si escludono a vicenda, visualizzati in un elenco a discesa associato a un pulsante secondario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300592"
---
# <a name="split-button"></a><span data-ttu-id="8d81f-103">Pulsante di menu combinato</span><span class="sxs-lookup"><span data-stu-id="8d81f-103">Split Button</span></span>

<span data-ttu-id="8d81f-104">Il pulsante di suddivisione è un controllo composito con il quale l'utente può selezionare un valore predefinito associato a un pulsante primario oppure selezionare da un elenco di valori che si escludono a vicenda, visualizzati in un elenco a discesa associato a un pulsante secondario.</span><span class="sxs-lookup"><span data-stu-id="8d81f-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="8d81f-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8d81f-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8d81f-106">Proprietà pulsante di divisione</span><span class="sxs-lookup"><span data-stu-id="8d81f-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="8d81f-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d81f-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="8d81f-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8d81f-108">Introduction</span></span>

<span data-ttu-id="8d81f-109">Questo controllo è utile per esporre elementi strettamente correlati nei casi in cui è disponibile un valore predefinito ovvio e in cui i singoli elementi possono essere rappresentati da un'immagine, un testo o entrambi.</span><span class="sxs-lookup"><span data-stu-id="8d81f-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="8d81f-110">Lo screenshot seguente illustra il pulsante di suddivisione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8d81f-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![Screenshot di un controllo SplitButton in una barra multifunzione di esempio.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="8d81f-112">Proprietà pulsante di divisione</span><span class="sxs-lookup"><span data-stu-id="8d81f-112">Split Button Properties</span></span>

<span data-ttu-id="8d81f-113">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo pulsante di divisione.</span><span class="sxs-lookup"><span data-stu-id="8d81f-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="8d81f-114">In genere, la proprietà di un pulsante di suddivisione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="8d81f-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="8d81f-115">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="8d81f-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="8d81f-116">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="8d81f-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="8d81f-117">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="8d81f-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="8d81f-118">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="8d81f-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="8d81f-119">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo pulsante di divisione.</span><span class="sxs-lookup"><span data-stu-id="8d81f-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d81f-120">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="8d81f-120">Property Key</span></span></th>
<th><span data-ttu-id="8d81f-121">Note</span><span class="sxs-lookup"><span data-stu-id="8d81f-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d81f-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="8d81f-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="8d81f-123">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8d81f-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="8d81f-124">Se tutti gli elementi figlio sono disabilitati, il Framework imposta <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> su false (0).</span><span class="sxs-lookup"><span data-stu-id="8d81f-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="8d81f-125">In caso contrario, se sono abilitati uno o più elementi figlio, UI_PKEY_Enabled viene impostato su true (-1).</span><span class="sxs-lookup"><span data-stu-id="8d81f-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="8d81f-126">Quando uno o più elementi figlio sono abilitati o disabilitati, la proprietà <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> per il controllo pulsante di suddivisione deve essere invalidata.</span><span class="sxs-lookup"><span data-stu-id="8d81f-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="8d81f-127">In questo modo il Framework esegue una query sul valore della proprietà aggiornata e aggiorna lo stato del controllo pulsante di suddivisione nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8d81f-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d81f-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="8d81f-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="8d81f-129">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8d81f-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d81f-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="8d81f-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="8d81f-131">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8d81f-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d81f-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="8d81f-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="8d81f-133">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="8d81f-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8d81f-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d81f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d81f-135">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="8d81f-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="8d81f-136">**Elemento di markup SplitButton**</span><span class="sxs-lookup"><span data-stu-id="8d81f-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>