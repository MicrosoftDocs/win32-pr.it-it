---
title: Elemento Button (framework della barra multifunzione di Windows)
description: Rappresenta un controllo Button.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Elemento Pulsante Barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40236b60a9fe9c72dd35d67fcf7c98bc188938af
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443572"
---
# <a name="button-element"></a><span data-ttu-id="45c8b-104">Elemento Button</span><span class="sxs-lookup"><span data-stu-id="45c8b-104">Button element</span></span>

<span data-ttu-id="45c8b-105">Rappresenta un [controllo](windowsribbon-controls-button.md) Button.</span><span class="sxs-lookup"><span data-stu-id="45c8b-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="45c8b-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="45c8b-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="45c8b-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="45c8b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45c8b-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="45c8b-108">Attribute</span></span></th>
<th><span data-ttu-id="45c8b-109">Type</span><span class="sxs-lookup"><span data-stu-id="45c8b-109">Type</span></span></th>
<th><span data-ttu-id="45c8b-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="45c8b-110">Required</span></span></th>
<th><span data-ttu-id="45c8b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45c8b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45c8b-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="45c8b-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="45c8b-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="45c8b-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="45c8b-114">No</span><span class="sxs-lookup"><span data-stu-id="45c8b-114">No</span></span><br/></td>
<td><span data-ttu-id="45c8b-115">Questo attributo è valido solo quando <strong>l'elemento Button</strong> è figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults.</strong></a></span><span class="sxs-lookup"><span data-stu-id="45c8b-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="45c8b-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="45c8b-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="45c8b-117">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="45c8b-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="45c8b-118">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="45c8b-118">Default.</span></span> <br/> </dd> <span data-ttu-id="45c8b-119"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="45c8b-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c8b-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="45c8b-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="45c8b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="45c8b-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="45c8b-122">No</span><span class="sxs-lookup"><span data-stu-id="45c8b-122">No</span></span><br/></td>
<td><span data-ttu-id="45c8b-123">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="45c8b-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="45c8b-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="45c8b-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="45c8b-125">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="45c8b-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="45c8b-126">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="45c8b-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="45c8b-127">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="45c8b-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45c8b-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="45c8b-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="45c8b-129">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="45c8b-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="45c8b-130">No</span><span class="sxs-lookup"><span data-stu-id="45c8b-130">No</span></span><br/></td>
<td><span data-ttu-id="45c8b-131">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="45c8b-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="45c8b-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="45c8b-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="45c8b-133">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="45c8b-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="45c8b-134">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="45c8b-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="45c8b-135">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="45c8b-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="45c8b-136">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="45c8b-136">Child elements</span></span>

<span data-ttu-id="45c8b-137">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="45c8b-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="45c8b-138">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="45c8b-138">Parent elements</span></span>



| <span data-ttu-id="45c8b-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="45c8b-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45c8b-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="45c8b-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="45c8b-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="45c8b-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="45c8b-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="45c8b-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="45c8b-143">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="45c8b-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="45c8b-144">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="45c8b-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="45c8b-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="45c8b-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="45c8b-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="45c8b-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="45c8b-147">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="45c8b-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="45c8b-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="45c8b-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="45c8b-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="45c8b-149">Remarks</span></span>

<span data-ttu-id="45c8b-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="45c8b-150">Optional.</span></span>

<span data-ttu-id="45c8b-151">Può verificarsi al massimo una volta per [**ogni elemento SplitButton.ButtonItem.**](windowsribbon-element-splitbutton-buttonitem.md)</span><span class="sxs-lookup"><span data-stu-id="45c8b-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="45c8b-152">Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="45c8b-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="45c8b-153">**Il** pulsante supporta [le modalità](ribbon-applicationmodes.md) dell'applicazione quando è ospitato nella colonna sinistra del menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45c8b-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="45c8b-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="45c8b-154">Examples</span></span>

<span data-ttu-id="45c8b-155">Nell'esempio seguente viene illustrato il markup di base per **l'oggetto Button.**</span><span class="sxs-lookup"><span data-stu-id="45c8b-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="45c8b-156">Questa sezione di codice illustra le **dichiarazioni button** Command, con un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per **l'elemento** Button.</span><span class="sxs-lookup"><span data-stu-id="45c8b-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


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



<span data-ttu-id="45c8b-157">Questa sezione di codice illustra le **dichiarazioni del** controllo Button.</span><span class="sxs-lookup"><span data-stu-id="45c8b-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="45c8b-158">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="45c8b-158">Element information</span></span>

* <span data-ttu-id="45c8b-159">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="45c8b-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="45c8b-160">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="45c8b-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="45c8b-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45c8b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c8b-162">Controllo Button</span><span class="sxs-lookup"><span data-stu-id="45c8b-162">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="45c8b-163">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="45c8b-163">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

