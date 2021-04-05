---
title: CheckBox (elemento)
description: Rappresenta un controllo casella di controllo.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Barra multifunzione Windows elemento CheckBox
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104117335"
---
# <a name="checkbox-element"></a><span data-ttu-id="d2b8d-104">CheckBox (elemento)</span><span class="sxs-lookup"><span data-stu-id="d2b8d-104">CheckBox element</span></span>

<span data-ttu-id="d2b8d-105">Rappresenta un controllo [casella di controllo](windowsribbon-controls-checkbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d2b8d-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="d2b8d-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d2b8d-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="d2b8d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d2b8d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2b8d-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="d2b8d-108">Attribute</span></span></th>
<th><span data-ttu-id="d2b8d-109">Type</span><span class="sxs-lookup"><span data-stu-id="d2b8d-109">Type</span></span></th>
<th><span data-ttu-id="d2b8d-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d2b8d-110">Required</span></span></th>
<th><span data-ttu-id="d2b8d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2b8d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2b8d-112"><strong>ApplicationDefaults. checkin</strong></span><span class="sxs-lookup"><span data-stu-id="d2b8d-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="d2b8d-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="d2b8d-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="d2b8d-114">No</span><span class="sxs-lookup"><span data-stu-id="d2b8d-114">No</span></span><br/></td>
<td><span data-ttu-id="d2b8d-115">Questo attributo è valido solo quando l'elemento <strong>CheckBox</strong> è figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolBar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="d2b8d-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2b8d-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2b8d-117">La <strong>casella</strong> di controllo non supporta uno stato terziario o indeterminato.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="d2b8d-118">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="d2b8d-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="d2b8d-119">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-119">Default.</span></span> <br/> </dd> <span data-ttu-id="d2b8d-120"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="d2b8d-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2b8d-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d2b8d-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d2b8d-122">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="d2b8d-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d2b8d-123">No</span><span class="sxs-lookup"><span data-stu-id="d2b8d-123">No</span></span><br/></td>
<td><span data-ttu-id="d2b8d-124">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d2b8d-125">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="d2b8d-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d2b8d-126">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d2b8d-127">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d2b8d-128">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d2b8d-129">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d2b8d-129">Child elements</span></span>

<span data-ttu-id="d2b8d-130">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d2b8d-131">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d2b8d-131">Parent elements</span></span>



| <span data-ttu-id="d2b8d-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="d2b8d-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2b8d-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="d2b8d-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="d2b8d-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="d2b8d-136">**Group**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="d2b8d-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="d2b8d-138">**QuickAccessToolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="d2b8d-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="d2b8d-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="d2b8d-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2b8d-141">Remarks</span></span>

<span data-ttu-id="d2b8d-142">Facoltativo o obbligatorio, a seconda dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="d2b8d-143">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolBar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="d2b8d-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d2b8d-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2b8d-144">Examples</span></span>

<span data-ttu-id="d2b8d-145">Nell'esempio seguente viene illustrato il markup di base per l'elemento **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="d2b8d-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="d2b8d-146">Questa sezione di codice mostra le dichiarazioni del comando **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="d2b8d-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="d2b8d-147">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="d2b8d-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="d2b8d-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d2b8d-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d2b8d-149">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2b8d-149">Minimum supported system</span></span><br/> | <span data-ttu-id="d2b8d-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2b8d-150">Windows 7</span></span> |
| <span data-ttu-id="d2b8d-151">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="d2b8d-151">Can be empty</span></span>                        | <span data-ttu-id="d2b8d-152">Sì</span><span class="sxs-lookup"><span data-stu-id="d2b8d-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="d2b8d-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2b8d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b8d-154">Controllo Check Box</span><span class="sxs-lookup"><span data-stu-id="d2b8d-154">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





