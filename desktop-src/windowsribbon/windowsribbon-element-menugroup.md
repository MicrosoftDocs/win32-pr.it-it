---
title: MenuGroup - elemento
description: Rappresenta un contenitore di controlli da visualizzare in una raccolta, in un menu o in una barra degli strumenti.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Elemento MenuGroup Nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95cbda43fe2f652888a7b84539752b5d671868c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442852"
---
# <a name="menugroup-element"></a><span data-ttu-id="0a1f9-104">MenuGroup - elemento</span><span class="sxs-lookup"><span data-stu-id="0a1f9-104">MenuGroup element</span></span>

<span data-ttu-id="0a1f9-105">Rappresenta un contenitore di controlli da visualizzare in una raccolta, in un menu o in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="0a1f9-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0a1f9-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="0a1f9-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="0a1f9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a1f9-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="0a1f9-108">Attribute</span></span></th>
<th><span data-ttu-id="0a1f9-109">Type</span><span class="sxs-lookup"><span data-stu-id="0a1f9-109">Type</span></span></th>
<th><span data-ttu-id="0a1f9-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0a1f9-110">Required</span></span></th>
<th><span data-ttu-id="0a1f9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a1f9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a1f9-112"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="0a1f9-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="0a1f9-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="0a1f9-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="0a1f9-114">No</span><span class="sxs-lookup"><span data-stu-id="0a1f9-114">No</span></span><br/></td>
<td><span data-ttu-id="0a1f9-115">Specifica le dimensioni e lo stile di layout per gli elementi nell'interfaccia utente del menu.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="0a1f9-116">Una risorsa immagine può essere fornita in due dimensioni (grande e piccola) e associata all'elemento nel markup usando gli elementi della proprietà <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> e <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages.</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a1f9-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="0a1f9-117">Se viene specificata una sola immagine, il framework la ridimensiona in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="0a1f9-118">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a1f9-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="0a1f9-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span><span class="sxs-lookup"><span data-stu-id="0a1f9-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="0a1f9-120">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-120">Default.</span></span> <br/> <span data-ttu-id="0a1f9-121">Stile: immagine piccola e testo de-evidenziato.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="0a1f9-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span><span class="sxs-lookup"><span data-stu-id="0a1f9-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="0a1f9-123">Stile: immagine grande e testo in grassetto.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0a1f9-124">Se <strong>MenuGroup</strong> è un elemento figlio di <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu,</strong></a>l'attributo <em>Class</em> viene ignorato e lo stile viene <code>MajorItems</code> applicato dal framework.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a1f9-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0a1f9-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0a1f9-126">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="0a1f9-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0a1f9-127">No</span><span class="sxs-lookup"><span data-stu-id="0a1f9-127">No</span></span><br/></td>
<td><span data-ttu-id="0a1f9-128">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a1f9-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0a1f9-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="0a1f9-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0a1f9-130">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0a1f9-131">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0a1f9-132">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0a1f9-133">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a1f9-133">Child elements</span></span>



| <span data-ttu-id="0a1f9-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a1f9-134">Element</span></span>                                                                             | <span data-ttu-id="0a1f9-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a1f9-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0a1f9-136">**Button**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="0a1f9-137">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-138">**Casella**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="0a1f9-139">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="0a1f9-141">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="0a1f9-143">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="0a1f9-145">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="0a1f9-147">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-148">**Controllo FontControl**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="0a1f9-149">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="0a1f9-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="0a1f9-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="0a1f9-151">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="0a1f9-153">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0a1f9-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="0a1f9-155">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="0a1f9-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0a1f9-156">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0a1f9-156">Parent elements</span></span>



| <span data-ttu-id="0a1f9-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a1f9-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a1f9-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="0a1f9-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="0a1f9-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="0a1f9-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="0a1f9-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="0a1f9-163">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="0a1f9-164">**SplitButton.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="0a1f9-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0a1f9-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a1f9-166">Remarks</span></span>

<span data-ttu-id="0a1f9-167">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-167">Required.</span></span>

<span data-ttu-id="0a1f9-168">Deve essere presente almeno una volta per ogni elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)o [**SplitButtonGallery.MenuGroups.**](windowsribbon-element-splitbuttongallery-menugroups.md)</span><span class="sxs-lookup"><span data-stu-id="0a1f9-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="0a1f9-169">Se [**ApplicationMenu è**](windowsribbon-element-applicationmenu.md) l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="0a1f9-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="0a1f9-170">Se [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)o [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) è l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="0a1f9-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="0a1f9-171">Se [**MiniToolbar è**](windowsribbon-element-minitoolbar.md) l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="0a1f9-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="0a1f9-172">L'attributo Class non è obbligatorio [**quando ApplicationMenu**](windowsribbon-element-applicationmenu.md) è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="0a1f9-173">Il framework applica il valore MajorItems per l'attributo Class.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="0a1f9-174">Quando [**ApplicationMenu è**](windowsribbon-element-applicationmenu.md) l'elemento padre, l'attributo Class non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="0a1f9-175">Esempio</span><span class="sxs-lookup"><span data-stu-id="0a1f9-175">Examples</span></span>

<span data-ttu-id="0a1f9-176">L'esempio seguente illustra il markup di base per [**SplitButton**](windowsribbon-element-splitbutton.md) con un **elemento MenuGroup.**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="0a1f9-177">Questa sezione di codice mostra le dichiarazioni [**SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** Command con una risorsa immagine di grandi dimensioni e una piccola.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="0a1f9-178">Viene dichiarato anche un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per **l'elemento SplitButton.**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="0a1f9-179">Questa sezione di codice illustra le [**dichiarazioni dei controlli SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** con `StandardItems` e `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="0a1f9-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="0a1f9-180">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a1f9-180">Element information</span></span>

* <span data-ttu-id="0a1f9-181">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a1f9-181">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0a1f9-182">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="0a1f9-182">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="0a1f9-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a1f9-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1f9-184">Specifica delle risorse immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0a1f9-184">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="0a1f9-185">Gruppo di menu</span><span class="sxs-lookup"><span data-stu-id="0a1f9-185">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





