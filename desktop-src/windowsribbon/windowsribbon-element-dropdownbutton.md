---
title: Elemento DropDownButton
description: Rappresenta un controllo pulsante di Drop-Down standard.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Barra multifunzione Windows elemento DropDownButton
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729223"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="35596-104">Elemento DropDownButton</span><span class="sxs-lookup"><span data-stu-id="35596-104">DropDownButton element</span></span>

<span data-ttu-id="35596-105">Rappresenta un controllo [pulsante a discesa](windowsribbon-controls-dropdownbutton.md) standard.</span><span class="sxs-lookup"><span data-stu-id="35596-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="35596-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="35596-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="35596-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="35596-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35596-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="35596-108">Attribute</span></span></th>
<th><span data-ttu-id="35596-109">Type</span><span class="sxs-lookup"><span data-stu-id="35596-109">Type</span></span></th>
<th><span data-ttu-id="35596-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="35596-110">Required</span></span></th>
<th><span data-ttu-id="35596-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35596-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35596-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="35596-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="35596-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="35596-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="35596-114">No</span><span class="sxs-lookup"><span data-stu-id="35596-114">No</span></span><br/></td>
<td><span data-ttu-id="35596-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="35596-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="35596-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="35596-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="35596-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="35596-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="35596-118">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="35596-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="35596-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="35596-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35596-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="35596-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="35596-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="35596-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="35596-122">No</span><span class="sxs-lookup"><span data-stu-id="35596-122">No</span></span><br/></td>
<td><span data-ttu-id="35596-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="35596-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="35596-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="35596-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="35596-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="35596-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="35596-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="35596-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="35596-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="35596-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="35596-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="35596-128">Child elements</span></span>



| <span data-ttu-id="35596-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="35596-129">Element</span></span>                                                                             | <span data-ttu-id="35596-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35596-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="35596-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="35596-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="35596-132">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-133">**Casella**</span><span class="sxs-lookup"><span data-stu-id="35596-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="35596-134">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="35596-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="35596-136">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="35596-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="35596-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="35596-138">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="35596-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="35596-140">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="35596-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="35596-142">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="35596-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="35596-144">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="35596-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="35596-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="35596-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="35596-146">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="35596-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="35596-148">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35596-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="35596-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="35596-150">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="35596-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="35596-151">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="35596-151">Parent elements</span></span>



| <span data-ttu-id="35596-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="35596-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="35596-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="35596-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="35596-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="35596-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="35596-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="35596-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="35596-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="35596-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="35596-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="35596-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="35596-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="35596-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="35596-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="35596-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="35596-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="35596-160">Remarks</span></span>

<span data-ttu-id="35596-161">Facoltativo o obbligatorio, a seconda dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="35596-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="35596-162">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="35596-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="35596-163">**DropDownButton** supporta le [modalità di applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35596-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="35596-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di **DropDownButton** quando **DropDownButton** è un discendente di [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="35596-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35596-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="35596-165">Examples</span></span>

<span data-ttu-id="35596-166">Nell'esempio seguente viene illustrato il markup di base per **DropDownButton**.</span><span class="sxs-lookup"><span data-stu-id="35596-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="35596-167">In questa sezione del codice vengono illustrate le dichiarazioni di comando **DropDownButton** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="35596-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="35596-168">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="35596-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="35596-169">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="35596-169">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="35596-170">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35596-170">Minimum supported system</span></span><br/> | <span data-ttu-id="35596-171">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35596-171">Windows 7</span></span> |
| <span data-ttu-id="35596-172">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="35596-172">Can be empty</span></span>                        | <span data-ttu-id="35596-173">No</span><span class="sxs-lookup"><span data-stu-id="35596-173">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="35596-174">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="35596-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35596-175">Controllo pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="35596-175">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="35596-176">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="35596-176">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

