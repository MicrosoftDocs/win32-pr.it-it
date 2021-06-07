---
title: Elemento Ribbon
description: Rappresenta il controllo barra multifunzione nella visualizzazione barra multifunzione.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Barra multifunzione dell'elemento Barra multifunzione
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445002"
---
# <a name="ribbon-element"></a><span data-ttu-id="a9fcc-104">Elemento Ribbon</span><span class="sxs-lookup"><span data-stu-id="a9fcc-104">Ribbon element</span></span>

<span data-ttu-id="a9fcc-105">Rappresenta il controllo barra multifunzione nella visualizzazione barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="a9fcc-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a9fcc-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="a9fcc-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a9fcc-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9fcc-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="a9fcc-108">Attribute</span></span></th>
<th><span data-ttu-id="a9fcc-109">Type</span><span class="sxs-lookup"><span data-stu-id="a9fcc-109">Type</span></span></th>
<th><span data-ttu-id="a9fcc-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a9fcc-110">Required</span></span></th>
<th><span data-ttu-id="a9fcc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9fcc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9fcc-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="a9fcc-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="a9fcc-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9fcc-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="a9fcc-114">No</span><span class="sxs-lookup"><span data-stu-id="a9fcc-114">No</span></span><br/></td>
<td><span data-ttu-id="a9fcc-115"><dt><span></span><span></span><strong></strong> (Piccola)</span><span class="sxs-lookup"><span data-stu-id="a9fcc-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="a9fcc-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-116">Default.</span></span> <br/> </dd> <span data-ttu-id="a9fcc-117"><dt><span></span><span></span><strong></strong> (Media)</span><span class="sxs-lookup"><span data-stu-id="a9fcc-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a9fcc-118"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="a9fcc-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9fcc-119"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="a9fcc-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="a9fcc-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9fcc-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="a9fcc-121">No</span><span class="sxs-lookup"><span data-stu-id="a9fcc-121">No</span></span><br/></td>
<td><span data-ttu-id="a9fcc-122">Usato per annotare l'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="a9fcc-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="a9fcc-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a9fcc-124">Qualsiasi sequenza di zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="a9fcc-125">La lunghezza massima è illimitata.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a9fcc-126">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a9fcc-126">Child elements</span></span>



| <span data-ttu-id="a9fcc-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9fcc-127">Element</span></span>                                                                                         | <span data-ttu-id="a9fcc-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9fcc-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a9fcc-129">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="a9fcc-130">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a9fcc-131">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="a9fcc-132">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a9fcc-133">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="a9fcc-134">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a9fcc-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="a9fcc-136">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a9fcc-137">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="a9fcc-138">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a9fcc-139">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="a9fcc-140">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a9fcc-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a9fcc-141">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a9fcc-141">Parent elements</span></span>



| <span data-ttu-id="a9fcc-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9fcc-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="a9fcc-143">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="a9fcc-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a9fcc-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9fcc-144">Remarks</span></span>

<span data-ttu-id="a9fcc-145">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-145">Required.</span></span>

<span data-ttu-id="a9fcc-146">Deve verificarsi esattamente una volta per [**ogni elemento Application.Views.**](windowsribbon-element-application-views.md)</span><span class="sxs-lookup"><span data-stu-id="a9fcc-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a9fcc-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9fcc-147">Examples</span></span>

<span data-ttu-id="a9fcc-148">L'esempio seguente illustra il markup di base per una **visualizzazione barra** multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a9fcc-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="a9fcc-149">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a9fcc-149">Element information</span></span>




* <span data-ttu-id="a9fcc-150">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9fcc-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="a9fcc-151">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="a9fcc-151">**Can be empty**: No</span></span>



 

 





