---
title: Elemento ComboBox
description: Rappresenta un controllo Casella combinata.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Elemento ComboBox nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ad8866b655be587e0c3d0f123d8bc59b6b8a21
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443582"
---
# <a name="combobox-element"></a><span data-ttu-id="5c372-104">Elemento ComboBox</span><span class="sxs-lookup"><span data-stu-id="5c372-104">ComboBox element</span></span>

<span data-ttu-id="5c372-105">Rappresenta un [controllo Casella](windowsribbon-controls-combobox.md) combinata.</span><span class="sxs-lookup"><span data-stu-id="5c372-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="5c372-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5c372-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="5c372-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="5c372-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c372-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="5c372-108">Attribute</span></span></th>
<th><span data-ttu-id="5c372-109">Type</span><span class="sxs-lookup"><span data-stu-id="5c372-109">Type</span></span></th>
<th><span data-ttu-id="5c372-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5c372-110">Required</span></span></th>
<th><span data-ttu-id="5c372-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c372-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c372-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="5c372-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="5c372-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="5c372-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="5c372-114">No</span><span class="sxs-lookup"><span data-stu-id="5c372-114">No</span></span><br/></td>
<td><span data-ttu-id="5c372-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="5c372-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="5c372-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5c372-117">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="5c372-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="5c372-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="5c372-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="5c372-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5c372-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c372-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="5c372-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="5c372-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c372-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="5c372-122">No</span><span class="sxs-lookup"><span data-stu-id="5c372-122">No</span></span><br/></td>
<td><span data-ttu-id="5c372-123">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="5c372-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="5c372-124">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="5c372-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="5c372-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c372-125">Default.</span></span> <br/> </dd> <span data-ttu-id="5c372-126"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="5c372-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c372-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="5c372-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="5c372-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c372-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="5c372-129">No</span><span class="sxs-lookup"><span data-stu-id="5c372-129">No</span></span><br/></td>
<td><span data-ttu-id="5c372-130">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="5c372-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="5c372-131">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="5c372-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="5c372-132">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c372-132">Default.</span></span> <br/> </dd> <span data-ttu-id="5c372-133"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="5c372-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c372-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="5c372-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="5c372-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="5c372-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="5c372-136">No</span><span class="sxs-lookup"><span data-stu-id="5c372-136">No</span></span><br/></td>
<td><span data-ttu-id="5c372-137"><dt><span></span><span></span><strong></strong> (NoResize)</span><span class="sxs-lookup"><span data-stu-id="5c372-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="5c372-138">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c372-138">Default.</span></span> <br/> </dd> <span data-ttu-id="5c372-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="5c372-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5c372-140">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5c372-140">Child elements</span></span>

<span data-ttu-id="5c372-141">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="5c372-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5c372-142">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5c372-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c372-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c372-143">Element</span></span></th>
<th><span data-ttu-id="5c372-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c372-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c372-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5c372-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5c372-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5c372-148"><a href="windowsribbon-element-group.md"><strong>Gruppo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5c372-149"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5c372-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5c372-151">Windows 8 e più recente.</span><span class="sxs-lookup"><span data-stu-id="5c372-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c372-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c372-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="5c372-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c372-153">Remarks</span></span>

<span data-ttu-id="5c372-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c372-154">Optional.</span></span>

<span data-ttu-id="5c372-155">Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="5c372-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="5c372-156">Poiché **ComboBox è** esclusivamente una raccolta di elementi, non supporta gli elementi Command.</span><span class="sxs-lookup"><span data-stu-id="5c372-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="5c372-157">È anche l'unico controllo raccolta che non supporta uno spazio dei comandi (una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi).</span><span class="sxs-lookup"><span data-stu-id="5c372-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="5c372-158">Per altre informazioni, vedere [Uso delle raccolte.](ribbon-controls-galleries.md)</span><span class="sxs-lookup"><span data-stu-id="5c372-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="5c372-159">Lo screenshot seguente illustra un controllo Casella combinata [della](windowsribbon-controls-combobox.md) barra multifunzione di Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="5c372-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot di un controllo casella combinata nella barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="5c372-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c372-161">Examples</span></span>

<span data-ttu-id="5c372-162">Gli esempi seguenti illustrano il markup di base per **l'oggetto ComboBox.**</span><span class="sxs-lookup"><span data-stu-id="5c372-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="5c372-163">Questa sezione di codice illustra le dichiarazioni del comando **ComboBox,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per **l'elemento ComboBox.**</span><span class="sxs-lookup"><span data-stu-id="5c372-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


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



<span data-ttu-id="5c372-164">Questa sezione di codice illustra le **dichiarazioni del controllo ComboBox.**</span><span class="sxs-lookup"><span data-stu-id="5c372-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="5c372-165">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5c372-165">Element information</span></span>

* <span data-ttu-id="5c372-166">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c372-166">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="5c372-167">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="5c372-167">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="5c372-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c372-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c372-169">Controllo Combo Box</span><span class="sxs-lookup"><span data-stu-id="5c372-169">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="5c372-170">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="5c372-170">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





