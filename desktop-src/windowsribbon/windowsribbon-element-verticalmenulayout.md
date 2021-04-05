---
title: Elemento VerticalMenuLayout
description: Rappresenta un layout verticale per gli elementi in una raccolta.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Barra multifunzione Windows elemento VerticalMenuLayout
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724343"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="48a1e-104">Elemento VerticalMenuLayout</span><span class="sxs-lookup"><span data-stu-id="48a1e-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="48a1e-105">Rappresenta un layout verticale per gli elementi in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="48a1e-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="48a1e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="48a1e-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="48a1e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="48a1e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48a1e-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="48a1e-108">Attribute</span></span></th>
<th><span data-ttu-id="48a1e-109">Type</span><span class="sxs-lookup"><span data-stu-id="48a1e-109">Type</span></span></th>
<th><span data-ttu-id="48a1e-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="48a1e-110">Required</span></span></th>
<th><span data-ttu-id="48a1e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a1e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48a1e-112"><strong>Gripper</strong></span><span class="sxs-lookup"><span data-stu-id="48a1e-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="48a1e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="48a1e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="48a1e-114">No</span><span class="sxs-lookup"><span data-stu-id="48a1e-114">No</span></span><br/></td>
<td><span data-ttu-id="48a1e-115">Un handle di ridimensionamento collegato all'elenco a discesa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="48a1e-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="48a1e-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="48a1e-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="48a1e-117">
<dt><span></span><span></span><strong></strong> Nessuno</span><span class="sxs-lookup"><span data-stu-id="48a1e-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="48a1e-118"><dt><span></span><span></span><strong></strong> Verticale</span><span class="sxs-lookup"><span data-stu-id="48a1e-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="48a1e-119">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="48a1e-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a1e-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="48a1e-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="48a1e-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="48a1e-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="48a1e-122">No</span><span class="sxs-lookup"><span data-stu-id="48a1e-122">No</span></span><br/></td>
<td><span data-ttu-id="48a1e-123"><strong>Windows 8 e versioni successive</strong></span><span class="sxs-lookup"><span data-stu-id="48a1e-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="48a1e-124">Consente di evidenziare tutti gli elementi dell'elenco fino a, incluso, l'elemento MouseOver corrente (anziché solo l'elemento MouseOver).</span><span class="sxs-lookup"><span data-stu-id="48a1e-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="48a1e-125">Usato in genere per più funzionalità di <strong>annullamento</strong> e <strong>ripristino</strong> .</span><span class="sxs-lookup"><span data-stu-id="48a1e-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="48a1e-126">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="48a1e-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="48a1e-127"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="48a1e-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="48a1e-128">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="48a1e-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a1e-129"><strong>prime righe</strong></span><span class="sxs-lookup"><span data-stu-id="48a1e-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="48a1e-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="48a1e-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="48a1e-131">No</span><span class="sxs-lookup"><span data-stu-id="48a1e-131">No</span></span><br/></td>
<td><span data-ttu-id="48a1e-132">Specifica il numero di righe di elementi che devono essere visibili senza scorrimento.</span><span class="sxs-lookup"><span data-stu-id="48a1e-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="48a1e-133">
<dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="48a1e-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="48a1e-134">Qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="48a1e-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="48a1e-135">Il valore predefinito è <strong>-1</strong> , che specifica di visualizzare il maggior numero possibile di righe di elementi.</span><span class="sxs-lookup"><span data-stu-id="48a1e-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="48a1e-136">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="48a1e-136">Child elements</span></span>

<span data-ttu-id="48a1e-137">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="48a1e-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="48a1e-138">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="48a1e-138">Parent elements</span></span>



| <span data-ttu-id="48a1e-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="48a1e-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48a1e-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="48a1e-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="48a1e-141">**Inribbongallery. MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="48a1e-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="48a1e-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="48a1e-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="48a1e-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="48a1e-143">Remarks</span></span>

<span data-ttu-id="48a1e-144">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="48a1e-144">Required.</span></span>

<span data-ttu-id="48a1e-145">L'elemento **VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deve essere presente una volta per ogni elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**inribbongallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="48a1e-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="48a1e-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="48a1e-146">Examples</span></span>

<span data-ttu-id="48a1e-147">Nell'esempio seguente viene illustrato il markup di base per un elemento **VerticalMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="48a1e-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="48a1e-148">In questa sezione del codice vengono illustrate le dichiarazioni di controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="48a1e-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="48a1e-149">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="48a1e-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="48a1e-150">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a1e-150">Minimum supported system</span></span><br/> | <span data-ttu-id="48a1e-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48a1e-151">Windows 7</span></span> |
| <span data-ttu-id="48a1e-152">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="48a1e-152">Can be empty</span></span>                        | <span data-ttu-id="48a1e-153">Sì</span><span class="sxs-lookup"><span data-stu-id="48a1e-153">Yes</span></span>       |



 

 





