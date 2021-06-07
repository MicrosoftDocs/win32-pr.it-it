---
title: Elemento CheckBox
description: Rappresenta un controllo Casella di controllo.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Elemento CheckBox nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443042"
---
# <a name="checkbox-element"></a><span data-ttu-id="60ec5-104">Elemento CheckBox</span><span class="sxs-lookup"><span data-stu-id="60ec5-104">CheckBox element</span></span>

<span data-ttu-id="60ec5-105">Rappresenta un [controllo Casella di](windowsribbon-controls-checkbox.md) controllo.</span><span class="sxs-lookup"><span data-stu-id="60ec5-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="60ec5-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="60ec5-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="60ec5-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="60ec5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60ec5-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="60ec5-108">Attribute</span></span></th>
<th><span data-ttu-id="60ec5-109">Type</span><span class="sxs-lookup"><span data-stu-id="60ec5-109">Type</span></span></th>
<th><span data-ttu-id="60ec5-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60ec5-110">Required</span></span></th>
<th><span data-ttu-id="60ec5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ec5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60ec5-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="60ec5-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="60ec5-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="60ec5-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="60ec5-114">No</span><span class="sxs-lookup"><span data-stu-id="60ec5-114">No</span></span><br/></td>
<td><span data-ttu-id="60ec5-115">Questo attributo è valido solo quando <strong>l'elemento CheckBox</strong> è figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60ec5-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="60ec5-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="60ec5-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="60ec5-117"><strong>CheckBox</strong> non supporta uno stato terziario o indeterminato.</span><span class="sxs-lookup"><span data-stu-id="60ec5-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="60ec5-118">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="60ec5-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="60ec5-119">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="60ec5-119">Default.</span></span> <br/> </dd> <span data-ttu-id="60ec5-120"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="60ec5-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60ec5-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="60ec5-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="60ec5-122">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="60ec5-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="60ec5-123">No</span><span class="sxs-lookup"><span data-stu-id="60ec5-123">No</span></span><br/></td>
<td><span data-ttu-id="60ec5-124">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60ec5-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="60ec5-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="60ec5-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="60ec5-126">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="60ec5-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="60ec5-127">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="60ec5-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="60ec5-128">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="60ec5-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="60ec5-129">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="60ec5-129">Child elements</span></span>

<span data-ttu-id="60ec5-130">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="60ec5-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="60ec5-131">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="60ec5-131">Parent elements</span></span>



| <span data-ttu-id="60ec5-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="60ec5-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60ec5-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="60ec5-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="60ec5-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="60ec5-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="60ec5-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="60ec5-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="60ec5-136">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="60ec5-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="60ec5-137">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="60ec5-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="60ec5-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="60ec5-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="60ec5-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="60ec5-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="60ec5-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="60ec5-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="60ec5-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="60ec5-141">Remarks</span></span>

<span data-ttu-id="60ec5-142">Facoltativo o obbligatorio, a seconda dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="60ec5-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="60ec5-143">Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="60ec5-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="60ec5-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="60ec5-144">Examples</span></span>

<span data-ttu-id="60ec5-145">L'esempio seguente illustra il markup di base per **l'elemento CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="60ec5-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="60ec5-146">Questa sezione di codice illustra le **dichiarazioni del comando CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="60ec5-146">This section of code shows the **CheckBox** Command declarations.</span></span>


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



<span data-ttu-id="60ec5-147">Questa sezione di codice illustra le **dichiarazioni del controllo CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="60ec5-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="60ec5-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="60ec5-148">Element information</span></span>

* <span data-ttu-id="60ec5-149">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="60ec5-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="60ec5-150">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="60ec5-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="60ec5-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60ec5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ec5-152">Controllo Check Box</span><span class="sxs-lookup"><span data-stu-id="60ec5-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





