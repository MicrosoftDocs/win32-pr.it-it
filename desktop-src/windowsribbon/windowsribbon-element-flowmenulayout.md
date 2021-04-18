---
title: Elemento FlowMenuLayout
description: Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Barra multifunzione Windows elemento FlowMenuLayout
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299231"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="a0577-104">Elemento FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="a0577-104">FlowMenuLayout element</span></span>

<span data-ttu-id="a0577-105">Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a0577-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="a0577-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a0577-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="a0577-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a0577-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0577-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="a0577-108">Attribute</span></span></th>
<th><span data-ttu-id="a0577-109">Type</span><span class="sxs-lookup"><span data-stu-id="a0577-109">Type</span></span></th>
<th><span data-ttu-id="a0577-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a0577-110">Required</span></span></th>
<th><span data-ttu-id="a0577-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0577-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0577-112"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="a0577-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="a0577-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a0577-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="a0577-114">No</span><span class="sxs-lookup"><span data-stu-id="a0577-114">No</span></span><br/></td>
<td><span data-ttu-id="a0577-115">Specifica il numero di elementi da visualizzare in una singola riga.</span><span class="sxs-lookup"><span data-stu-id="a0577-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="a0577-116">
<dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="a0577-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="a0577-117">Qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a0577-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="a0577-118">Il valore predefinito è <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0577-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0577-119"><strong>Gripper</strong></span><span class="sxs-lookup"><span data-stu-id="a0577-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="a0577-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0577-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0577-121">No</span><span class="sxs-lookup"><span data-stu-id="a0577-121">No</span></span><br/></td>
<td><span data-ttu-id="a0577-122">Un handle di ridimensionamento collegato all'elenco a discesa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a0577-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="a0577-123">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0577-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="a0577-124">
<dt><span></span><span></span><strong></strong> Nessuno</span><span class="sxs-lookup"><span data-stu-id="a0577-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a0577-125"><dt><span></span><span></span><strong></strong> Verticale</span><span class="sxs-lookup"><span data-stu-id="a0577-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a0577-126"><dt><span></span><span></span><strong></strong> Angolo</span><span class="sxs-lookup"><span data-stu-id="a0577-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="a0577-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a0577-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0577-128"><strong>prime righe</strong></span><span class="sxs-lookup"><span data-stu-id="a0577-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="a0577-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a0577-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="a0577-130">No</span><span class="sxs-lookup"><span data-stu-id="a0577-130">No</span></span><br/></td>
<td><span data-ttu-id="a0577-131">Specifica il numero di righe di elementi che devono essere visibili senza scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a0577-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="a0577-132">
<dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="a0577-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="a0577-133">Qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a0577-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="a0577-134">Il valore predefinito è <strong>-1</strong> , che specifica di visualizzare il maggior numero possibile di righe di elementi.</span><span class="sxs-lookup"><span data-stu-id="a0577-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a0577-135">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a0577-135">Child elements</span></span>

<span data-ttu-id="a0577-136">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a0577-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a0577-137">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a0577-137">Parent elements</span></span>



| <span data-ttu-id="a0577-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0577-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0577-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a0577-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="a0577-140">**Inribbongallery. MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a0577-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="a0577-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a0577-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a0577-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0577-142">Remarks</span></span>

<span data-ttu-id="a0577-143">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0577-143">Required.</span></span>

<span data-ttu-id="a0577-144">L'elemento [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o **FlowMenuLayout** deve essere presente una volta per ogni elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**inribbongallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="a0577-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="a0577-145">Gli elementi sono disposti in base alle proprietà di interruzioni di riga inerenti gli attributi di *riga* e *colonna* .</span><span class="sxs-lookup"><span data-stu-id="a0577-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="a0577-146">Quando il contenuto supera la lunghezza di una singola riga, il menu interrompe le righe, esegue il wrapping delle righe e allinea il contenuto in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a0577-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="a0577-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0577-147">Examples</span></span>

<span data-ttu-id="a0577-148">Nell'esempio seguente viene illustrato il markup di base per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="a0577-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="a0577-149">Questa sezione di codice mostra la dichiarazione di controllo [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) con una specifica **FlowMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="a0577-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="a0577-150">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a0577-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a0577-151">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0577-151">Minimum supported system</span></span><br/> | <span data-ttu-id="a0577-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0577-152">Windows 7</span></span> |
| <span data-ttu-id="a0577-153">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="a0577-153">Can be empty</span></span>                        | <span data-ttu-id="a0577-154">Sì</span><span class="sxs-lookup"><span data-stu-id="a0577-154">Yes</span></span>       |



 

 





