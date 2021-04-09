---
title: Elemento Button (Framework della barra multifunzione di Windows)
description: Rappresenta un controllo Button.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Barra multifunzione Windows elemento pulsante
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117815"
---
# <a name="button-element"></a><span data-ttu-id="ffe23-104">Elemento Button</span><span class="sxs-lookup"><span data-stu-id="ffe23-104">Button element</span></span>

<span data-ttu-id="ffe23-105">Rappresenta un controllo [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe23-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ffe23-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ffe23-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="ffe23-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="ffe23-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffe23-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="ffe23-108">Attribute</span></span></th>
<th><span data-ttu-id="ffe23-109">Type</span><span class="sxs-lookup"><span data-stu-id="ffe23-109">Type</span></span></th>
<th><span data-ttu-id="ffe23-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ffe23-110">Required</span></span></th>
<th><span data-ttu-id="ffe23-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffe23-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffe23-112"><strong>ApplicationDefaults. checkin</strong></span><span class="sxs-lookup"><span data-stu-id="ffe23-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="ffe23-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffe23-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="ffe23-114">No</span><span class="sxs-lookup"><span data-stu-id="ffe23-114">No</span></span><br/></td>
<td><span data-ttu-id="ffe23-115">Questo attributo è valido solo quando l'elemento <strong>Button</strong> è figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolBar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ffe23-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="ffe23-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffe23-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ffe23-117">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="ffe23-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ffe23-118">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ffe23-118">Default.</span></span> <br/> </dd> <span data-ttu-id="ffe23-119"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="ffe23-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffe23-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="ffe23-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="ffe23-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ffe23-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="ffe23-122">No</span><span class="sxs-lookup"><span data-stu-id="ffe23-122">No</span></span><br/></td>
<td><span data-ttu-id="ffe23-123">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ffe23-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="ffe23-124">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="ffe23-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ffe23-125">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="ffe23-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="ffe23-126">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="ffe23-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="ffe23-127">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ffe23-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffe23-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ffe23-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ffe23-129">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="ffe23-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ffe23-130">No</span><span class="sxs-lookup"><span data-stu-id="ffe23-130">No</span></span><br/></td>
<td><span data-ttu-id="ffe23-131">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ffe23-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ffe23-132">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="ffe23-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ffe23-133">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="ffe23-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ffe23-134">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="ffe23-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ffe23-135">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ffe23-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ffe23-136">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ffe23-136">Child elements</span></span>

<span data-ttu-id="ffe23-137">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="ffe23-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ffe23-138">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ffe23-138">Parent elements</span></span>



| <span data-ttu-id="ffe23-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffe23-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffe23-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="ffe23-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="ffe23-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="ffe23-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="ffe23-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="ffe23-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="ffe23-143">**Group**</span><span class="sxs-lookup"><span data-stu-id="ffe23-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="ffe23-144">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="ffe23-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="ffe23-145">**QuickAccessToolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="ffe23-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="ffe23-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="ffe23-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="ffe23-147">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="ffe23-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="ffe23-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="ffe23-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="ffe23-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffe23-149">Remarks</span></span>

<span data-ttu-id="ffe23-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ffe23-150">Optional.</span></span>

<span data-ttu-id="ffe23-151">Può verificarsi al massimo una volta per ogni elemento [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe23-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="ffe23-152">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolBar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe23-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="ffe23-153">Il **pulsante** supporta le [modalità di applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna a sinistra del menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ffe23-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="ffe23-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffe23-154">Examples</span></span>

<span data-ttu-id="ffe23-155">Nell'esempio seguente viene illustrato il markup di base per il **pulsante**.</span><span class="sxs-lookup"><span data-stu-id="ffe23-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="ffe23-156">In questa sezione del codice vengono illustrate le dichiarazioni di comando dei **pulsanti** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **Button** .</span><span class="sxs-lookup"><span data-stu-id="ffe23-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="ffe23-157">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **Button** .</span><span class="sxs-lookup"><span data-stu-id="ffe23-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="ffe23-158">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ffe23-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ffe23-159">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffe23-159">Minimum supported system</span></span><br/> | <span data-ttu-id="ffe23-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffe23-160">Windows 7</span></span> |
| <span data-ttu-id="ffe23-161">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="ffe23-161">Can be empty</span></span>                        | <span data-ttu-id="ffe23-162">Sì</span><span class="sxs-lookup"><span data-stu-id="ffe23-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="ffe23-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffe23-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe23-164">Button (controllo)</span><span class="sxs-lookup"><span data-stu-id="ffe23-164">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="ffe23-165">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="ffe23-165">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

