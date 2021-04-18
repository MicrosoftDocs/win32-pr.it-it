---
title: ComboBox (elemento)
description: Rappresenta un controllo casella combinata.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Barra multifunzione Windows elemento ComboBox
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299365"
---
# <a name="combobox-element"></a><span data-ttu-id="c9a12-104">ComboBox (elemento)</span><span class="sxs-lookup"><span data-stu-id="c9a12-104">ComboBox element</span></span>

<span data-ttu-id="c9a12-105">Rappresenta un controllo [casella combinata](windowsribbon-controls-combobox.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a12-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="c9a12-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c9a12-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="c9a12-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="c9a12-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a12-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="c9a12-108">Attribute</span></span></th>
<th><span data-ttu-id="c9a12-109">Type</span><span class="sxs-lookup"><span data-stu-id="c9a12-109">Type</span></span></th>
<th><span data-ttu-id="c9a12-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c9a12-110">Required</span></span></th>
<th><span data-ttu-id="c9a12-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a12-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9a12-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c9a12-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c9a12-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="c9a12-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c9a12-114">No</span><span class="sxs-lookup"><span data-stu-id="c9a12-114">No</span></span><br/></td>
<td><span data-ttu-id="c9a12-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c9a12-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c9a12-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="c9a12-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c9a12-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c9a12-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c9a12-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9a12-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c9a12-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c9a12-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9a12-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="c9a12-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="c9a12-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9a12-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="c9a12-122">No</span><span class="sxs-lookup"><span data-stu-id="c9a12-122">No</span></span><br/></td>
<td><span data-ttu-id="c9a12-123">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="c9a12-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="c9a12-124">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="c9a12-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="c9a12-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c9a12-125">Default.</span></span> <br/> </dd> <span data-ttu-id="c9a12-126"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="c9a12-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9a12-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="c9a12-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="c9a12-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9a12-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="c9a12-129">No</span><span class="sxs-lookup"><span data-stu-id="c9a12-129">No</span></span><br/></td>
<td><span data-ttu-id="c9a12-130">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="c9a12-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="c9a12-131">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="c9a12-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="c9a12-132">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c9a12-132">Default.</span></span> <br/> </dd> <span data-ttu-id="c9a12-133"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="c9a12-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9a12-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="c9a12-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="c9a12-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="c9a12-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="c9a12-136">No</span><span class="sxs-lookup"><span data-stu-id="c9a12-136">No</span></span><br/></td>
<td><span data-ttu-id="c9a12-137"><dt><span></span><span></span><strong></strong> NoResize</span><span class="sxs-lookup"><span data-stu-id="c9a12-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="c9a12-138">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c9a12-138">Default.</span></span> <br/> </dd> <span data-ttu-id="c9a12-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="c9a12-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c9a12-140">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c9a12-140">Child elements</span></span>

<span data-ttu-id="c9a12-141">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="c9a12-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c9a12-142">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c9a12-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a12-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9a12-143">Element</span></span></th>
<th><span data-ttu-id="c9a12-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a12-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9a12-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9a12-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c9a12-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9a12-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c9a12-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9a12-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c9a12-151">Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c9a12-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9a12-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9a12-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="c9a12-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9a12-153">Remarks</span></span>

<span data-ttu-id="c9a12-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9a12-154">Optional.</span></span>

<span data-ttu-id="c9a12-155">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a12-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="c9a12-156">Poiché **ComboBox** è esclusivamente una raccolta di elementi, non supporta gli elementi di comando.</span><span class="sxs-lookup"><span data-stu-id="c9a12-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="c9a12-157">È anche l'unico controllo raccolta che non supporta uno spazio dei comandi (una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi).</span><span class="sxs-lookup"><span data-stu-id="c9a12-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="c9a12-158">Per ulteriori informazioni, vedere [utilizzo delle raccolte](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="c9a12-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="c9a12-159">Lo screenshot seguente illustra un controllo [casella combinata](windowsribbon-controls-combobox.md) della barra multifunzione di Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="c9a12-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot di un controllo ComboBox sulla barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="c9a12-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9a12-161">Examples</span></span>

<span data-ttu-id="c9a12-162">Gli esempi seguenti illustrano il markup di base per **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="c9a12-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="c9a12-163">In questa sezione del codice vengono illustrate le dichiarazioni di comando **ComboBox** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="c9a12-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="c9a12-164">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="c9a12-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="c9a12-165">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c9a12-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="c9a12-166">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a12-166">Minimum supported system</span></span><br/> | <span data-ttu-id="c9a12-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9a12-167">Windows 7</span></span> |
| <span data-ttu-id="c9a12-168">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="c9a12-168">Can be empty</span></span>                        | <span data-ttu-id="c9a12-169">Sì</span><span class="sxs-lookup"><span data-stu-id="c9a12-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="c9a12-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a12-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a12-171">Controllo Combo Box</span><span class="sxs-lookup"><span data-stu-id="c9a12-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="c9a12-172">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="c9a12-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





