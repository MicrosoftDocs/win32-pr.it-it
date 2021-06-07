---
title: Elemento SplitButton
description: Rappresenta un controllo pulsante di menu suddiviso standard.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Elemento SplitButton Nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf03d85dd0402548d02f107dafb209b68c13bb72
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444402"
---
# <a name="splitbutton-element"></a><span data-ttu-id="d8264-104">Elemento SplitButton</span><span class="sxs-lookup"><span data-stu-id="d8264-104">SplitButton element</span></span>

<span data-ttu-id="d8264-105">Rappresenta un controllo [pulsante di menu suddiviso](windowsribbon-controls-splitbutton.md) standard.</span><span class="sxs-lookup"><span data-stu-id="d8264-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="d8264-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d8264-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="d8264-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d8264-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8264-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="d8264-108">Attribute</span></span></th>
<th><span data-ttu-id="d8264-109">Type</span><span class="sxs-lookup"><span data-stu-id="d8264-109">Type</span></span></th>
<th><span data-ttu-id="d8264-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d8264-110">Required</span></span></th>
<th><span data-ttu-id="d8264-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8264-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8264-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="d8264-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="d8264-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8264-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d8264-114">No</span><span class="sxs-lookup"><span data-stu-id="d8264-114">No</span></span><br/></td>
<td><span data-ttu-id="d8264-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d8264-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="d8264-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="d8264-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d8264-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="d8264-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="d8264-118">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="d8264-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="d8264-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d8264-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8264-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d8264-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d8264-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="d8264-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d8264-122">No</span><span class="sxs-lookup"><span data-stu-id="d8264-122">No</span></span><br/></td>
<td><span data-ttu-id="d8264-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8264-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d8264-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="d8264-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d8264-125">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="d8264-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d8264-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d8264-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d8264-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d8264-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d8264-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d8264-128">Child elements</span></span>



| <span data-ttu-id="d8264-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8264-129">Element</span></span>                                                                                   | <span data-ttu-id="d8264-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8264-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d8264-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="d8264-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="d8264-132">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-133">**Casella**</span><span class="sxs-lookup"><span data-stu-id="d8264-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="d8264-134">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="d8264-136">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="d8264-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="d8264-138">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="d8264-140">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="d8264-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="d8264-142">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-143">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="d8264-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="d8264-144">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d8264-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="d8264-145">**SplitButton.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d8264-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="d8264-146">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d8264-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="d8264-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="d8264-148">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d8264-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="d8264-150">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="d8264-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d8264-151">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d8264-151">Parent elements</span></span>



| <span data-ttu-id="d8264-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8264-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d8264-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d8264-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="d8264-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="d8264-155">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="d8264-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="d8264-156">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="d8264-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="d8264-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="d8264-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d8264-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8264-159">Remarks</span></span>

<span data-ttu-id="d8264-160">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d8264-160">Optional.</span></span>

<span data-ttu-id="d8264-161">Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="d8264-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="d8264-162">**SplitButton** supporta le [modalità dell'applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8264-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="d8264-163">[**DropDownGallery e**](windowsribbon-element-dropdowngallery.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di [**DropDownButton**](windowsribbon-element-dropdownbutton.md) quando **DropDownButton** è un discendente di [**ApplicationMenu.**](windowsribbon-element-applicationmenu.md)</span><span class="sxs-lookup"><span data-stu-id="d8264-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="d8264-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) deve verificarsi una sola volta se gli elementi seguenti non sono presenti come elementi figlio di **SplitButton:**</span><span class="sxs-lookup"><span data-stu-id="d8264-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="d8264-165">**Pulsante**</span><span class="sxs-lookup"><span data-stu-id="d8264-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="d8264-166">**Casella**</span><span class="sxs-lookup"><span data-stu-id="d8264-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="d8264-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="d8264-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="d8264-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="d8264-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="d8264-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-170">**SplitButton**</span></span>
-   [<span data-ttu-id="d8264-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d8264-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="d8264-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="d8264-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="d8264-173">Questi controlli vengono considerati come elementi figlio di un singolo [**elemento SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) predefinito.</span><span class="sxs-lookup"><span data-stu-id="d8264-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d8264-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="d8264-174">Examples</span></span>

<span data-ttu-id="d8264-175">Nell'esempio seguente viene illustrato il markup di base per [il pulsante di menu suddiviso](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="d8264-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="d8264-176">Questa sezione di codice illustra le **dichiarazioni di Comando SplitButton,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funziona come contenitore padre per l'elemento **SplitButton.**</span><span class="sxs-lookup"><span data-stu-id="d8264-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="d8264-177">Questa sezione di codice illustra le **dichiarazioni del controllo SplitButton.**</span><span class="sxs-lookup"><span data-stu-id="d8264-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d8264-178">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d8264-178">Element information</span></span>

- <span data-ttu-id="d8264-179">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8264-179">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="d8264-180">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="d8264-180">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="d8264-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8264-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8264-182">Controllo Pulsante di menu suddiviso</span><span class="sxs-lookup"><span data-stu-id="d8264-182">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="d8264-183">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="d8264-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

