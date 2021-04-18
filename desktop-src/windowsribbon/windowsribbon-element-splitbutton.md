---
title: Elemento SplitButton
description: Rappresenta un controllo pulsante di suddivisione standard.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Barra multifunzione Windows elemento SplitButton
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300050"
---
# <a name="splitbutton-element"></a><span data-ttu-id="02848-104">Elemento SplitButton</span><span class="sxs-lookup"><span data-stu-id="02848-104">SplitButton element</span></span>

<span data-ttu-id="02848-105">Rappresenta un controllo [pulsante di suddivisione](windowsribbon-controls-splitbutton.md) standard.</span><span class="sxs-lookup"><span data-stu-id="02848-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="02848-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="02848-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="02848-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="02848-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02848-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="02848-108">Attribute</span></span></th>
<th><span data-ttu-id="02848-109">Type</span><span class="sxs-lookup"><span data-stu-id="02848-109">Type</span></span></th>
<th><span data-ttu-id="02848-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="02848-110">Required</span></span></th>
<th><span data-ttu-id="02848-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02848-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02848-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="02848-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="02848-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="02848-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="02848-114">No</span><span class="sxs-lookup"><span data-stu-id="02848-114">No</span></span><br/></td>
<td><span data-ttu-id="02848-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="02848-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="02848-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="02848-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="02848-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="02848-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="02848-118">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="02848-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="02848-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="02848-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02848-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="02848-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="02848-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="02848-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="02848-122">No</span><span class="sxs-lookup"><span data-stu-id="02848-122">No</span></span><br/></td>
<td><span data-ttu-id="02848-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="02848-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="02848-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="02848-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="02848-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="02848-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="02848-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="02848-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="02848-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="02848-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="02848-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02848-128">Child elements</span></span>



| <span data-ttu-id="02848-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="02848-129">Element</span></span>                                                                                   | <span data-ttu-id="02848-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02848-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="02848-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="02848-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="02848-132">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-133">**Casella**</span><span class="sxs-lookup"><span data-stu-id="02848-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="02848-134">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="02848-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="02848-136">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="02848-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="02848-138">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="02848-140">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="02848-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="02848-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="02848-142">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-143">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="02848-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="02848-144">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="02848-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="02848-145">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="02848-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="02848-146">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="02848-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="02848-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="02848-148">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="02848-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="02848-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="02848-150">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="02848-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="02848-151">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="02848-151">Parent elements</span></span>



| <span data-ttu-id="02848-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="02848-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="02848-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="02848-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="02848-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="02848-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="02848-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="02848-156">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="02848-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="02848-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="02848-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="02848-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="02848-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="02848-159">Remarks</span></span>

<span data-ttu-id="02848-160">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="02848-160">Optional.</span></span>

<span data-ttu-id="02848-161">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="02848-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="02848-162">**SplitButton** supporta le [modalità di applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02848-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="02848-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di [**DropDownButton**](windowsribbon-element-dropdownbutton.md) quando **DropDownButton** è un discendente di [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="02848-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="02848-164">[**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) deve essere presente una sola volta se le seguenti non sono presenti come elementi figlio di **SplitButton**:</span><span class="sxs-lookup"><span data-stu-id="02848-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="02848-165">**Pulsante**</span><span class="sxs-lookup"><span data-stu-id="02848-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="02848-166">**Casella**</span><span class="sxs-lookup"><span data-stu-id="02848-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="02848-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="02848-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="02848-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="02848-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="02848-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="02848-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="02848-170">**SplitButton**</span></span>
-   [<span data-ttu-id="02848-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="02848-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="02848-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="02848-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="02848-173">Questi controlli vengono considerati come elementi figlio di un singolo elemento predefinito [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="02848-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="02848-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="02848-174">Examples</span></span>

<span data-ttu-id="02848-175">Nell'esempio seguente viene illustrato il markup di base per il [pulsante di suddivisione](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="02848-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="02848-176">In questa sezione del codice vengono illustrate le dichiarazioni di comando **SplitButton** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="02848-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="02848-177">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="02848-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="02848-178">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="02848-178">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="02848-179">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02848-179">Minimum supported system</span></span><br/> | <span data-ttu-id="02848-180">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02848-180">Windows 7</span></span> |
| <span data-ttu-id="02848-181">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="02848-181">Can be empty</span></span>                        | <span data-ttu-id="02848-182">No</span><span class="sxs-lookup"><span data-stu-id="02848-182">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="02848-183">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02848-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02848-184">Controllo pulsante combinato</span><span class="sxs-lookup"><span data-stu-id="02848-184">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="02848-185">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="02848-185">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

