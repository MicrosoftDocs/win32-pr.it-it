---
title: Ribbon (elemento)
description: Rappresenta il controllo Ribbon nella visualizzazione della barra multifunzione.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Barra multifunzione di Windows elemento barra multifunzione
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299037"
---
# <a name="ribbon-element"></a><span data-ttu-id="98c87-104">Ribbon (elemento)</span><span class="sxs-lookup"><span data-stu-id="98c87-104">Ribbon element</span></span>

<span data-ttu-id="98c87-105">Rappresenta il controllo Ribbon nella visualizzazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="98c87-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="98c87-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="98c87-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="98c87-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="98c87-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98c87-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="98c87-108">Attribute</span></span></th>
<th><span data-ttu-id="98c87-109">Type</span><span class="sxs-lookup"><span data-stu-id="98c87-109">Type</span></span></th>
<th><span data-ttu-id="98c87-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="98c87-110">Required</span></span></th>
<th><span data-ttu-id="98c87-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c87-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98c87-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="98c87-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="98c87-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="98c87-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="98c87-114">No</span><span class="sxs-lookup"><span data-stu-id="98c87-114">No</span></span><br/></td>
<td><span data-ttu-id="98c87-115"><dt><span></span><span></span><strong></strong> Piccolo</span><span class="sxs-lookup"><span data-stu-id="98c87-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="98c87-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="98c87-116">Default.</span></span> <br/> </dd> <span data-ttu-id="98c87-117"><dt><span></span><span></span><strong></strong> Media</span><span class="sxs-lookup"><span data-stu-id="98c87-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="98c87-118"><dt><span></span><span></span><strong></strong> Grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="98c87-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98c87-119"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="98c87-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="98c87-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="98c87-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="98c87-121">No</span><span class="sxs-lookup"><span data-stu-id="98c87-121">No</span></span><br/></td>
<td><span data-ttu-id="98c87-122">Utilizzato per annotare l'elemento Command.</span><span class="sxs-lookup"><span data-stu-id="98c87-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="98c87-123">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="98c87-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="98c87-124">Qualsiasi sequenza di zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="98c87-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="98c87-125">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="98c87-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="98c87-126">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="98c87-126">Child elements</span></span>



| <span data-ttu-id="98c87-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="98c87-127">Element</span></span>                                                                                         | <span data-ttu-id="98c87-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c87-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="98c87-129">**Ribbon. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="98c87-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="98c87-130">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="98c87-131">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="98c87-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="98c87-132">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="98c87-133">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="98c87-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="98c87-134">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="98c87-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="98c87-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="98c87-136">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="98c87-137">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="98c87-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="98c87-138">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="98c87-139">**Ribbon. Tabs**</span><span class="sxs-lookup"><span data-stu-id="98c87-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="98c87-140">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="98c87-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="98c87-141">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="98c87-141">Parent elements</span></span>



| <span data-ttu-id="98c87-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="98c87-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="98c87-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="98c87-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="98c87-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="98c87-144">Remarks</span></span>

<span data-ttu-id="98c87-145">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="98c87-145">Required.</span></span>

<span data-ttu-id="98c87-146">Deve essere eseguita esattamente una volta per ogni elemento [**Application. views**](windowsribbon-element-application-views.md) .</span><span class="sxs-lookup"><span data-stu-id="98c87-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="98c87-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="98c87-147">Examples</span></span>

<span data-ttu-id="98c87-148">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione della **barra multifunzione** .</span><span class="sxs-lookup"><span data-stu-id="98c87-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="98c87-149">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="98c87-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="98c87-150">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98c87-150">Minimum supported system</span></span><br/> | <span data-ttu-id="98c87-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98c87-151">Windows 7</span></span> |
| <span data-ttu-id="98c87-152">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="98c87-152">Can be empty</span></span>                        | <span data-ttu-id="98c87-153">No</span><span class="sxs-lookup"><span data-stu-id="98c87-153">No</span></span>        |



 

 





