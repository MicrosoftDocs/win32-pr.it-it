---
title: Elemento FlowMenuLayout
description: Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Barra multifunzione di Windows per l'elemento FlowMenuLayout
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442882"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="35520-104">Elemento FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="35520-104">FlowMenuLayout element</span></span>

<span data-ttu-id="35520-105">Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="35520-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="35520-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="35520-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="35520-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="35520-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35520-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="35520-108">Attribute</span></span></th>
<th><span data-ttu-id="35520-109">Type</span><span class="sxs-lookup"><span data-stu-id="35520-109">Type</span></span></th>
<th><span data-ttu-id="35520-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="35520-110">Required</span></span></th>
<th><span data-ttu-id="35520-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35520-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35520-112"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="35520-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="35520-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35520-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="35520-114">No</span><span class="sxs-lookup"><span data-stu-id="35520-114">No</span></span><br/></td>
<td><span data-ttu-id="35520-115">Specifica il numero di elementi da visualizzare in una singola riga.</span><span class="sxs-lookup"><span data-stu-id="35520-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="35520-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="35520-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="35520-117">Qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="35520-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="35520-118">Il valore predefinito è <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="35520-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35520-119"><strong>Pinza</strong></span><span class="sxs-lookup"><span data-stu-id="35520-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="35520-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="35520-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="35520-121">No</span><span class="sxs-lookup"><span data-stu-id="35520-121">No</span></span><br/></td>
<td><span data-ttu-id="35520-122">Handle di ridimensionamento associato all'elenco a discesa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="35520-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="35520-123">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="35520-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="35520-124">
<dt><span></span><span></span><strong></strong> (Nessuno)</span><span class="sxs-lookup"><span data-stu-id="35520-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="35520-125"><dt><span></span><span></span><strong></strong> (Verticale)</span><span class="sxs-lookup"><span data-stu-id="35520-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="35520-126"><dt><span></span><span></span><strong></strong> (Angolo)</span><span class="sxs-lookup"><span data-stu-id="35520-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="35520-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="35520-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35520-128"><strong>prime righe</strong></span><span class="sxs-lookup"><span data-stu-id="35520-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="35520-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35520-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="35520-130">No</span><span class="sxs-lookup"><span data-stu-id="35520-130">No</span></span><br/></td>
<td><span data-ttu-id="35520-131">Specifica il numero di righe dell'elemento da visualizzare senza scorrere.</span><span class="sxs-lookup"><span data-stu-id="35520-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="35520-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="35520-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="35520-133">Qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="35520-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="35520-134">Il valore predefinito <strong>è -1</strong> che specifica di visualizzare il maggior numero possibile di righe di elementi.</span><span class="sxs-lookup"><span data-stu-id="35520-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="35520-135">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="35520-135">Child elements</span></span>

<span data-ttu-id="35520-136">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="35520-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="35520-137">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="35520-137">Parent elements</span></span>



| <span data-ttu-id="35520-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="35520-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35520-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="35520-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="35520-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="35520-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="35520-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="35520-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="35520-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="35520-142">Remarks</span></span>

<span data-ttu-id="35520-143">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="35520-143">Required.</span></span>

<span data-ttu-id="35520-144">L'elemento [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o **FlowMenuLayout** deve verificarsi una volta per ogni elemento [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)</span><span class="sxs-lookup"><span data-stu-id="35520-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="35520-145">Gli elementi vengono disposti in base alle proprietà di interruzione di riga intrinseche agli *attributi di* riga *e* colonna.</span><span class="sxs-lookup"><span data-stu-id="35520-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="35520-146">Quando il contenuto supera la lunghezza di una singola riga, il menu interrompe le righe, esegue il wrapping delle righe e allinea il contenuto in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="35520-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="35520-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="35520-147">Examples</span></span>

<span data-ttu-id="35520-148">Nell'esempio seguente viene illustrato il markup di base per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="35520-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="35520-149">Questa sezione di codice illustra la dichiarazione del controllo [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) con una **specifica FlowMenuLayout.**</span><span class="sxs-lookup"><span data-stu-id="35520-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="35520-150">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="35520-150">Element information</span></span>

* <span data-ttu-id="35520-151">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="35520-151">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="35520-152">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="35520-152">**Can be empty**: Yes</span></span>


 

 





