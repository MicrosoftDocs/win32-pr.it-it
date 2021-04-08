---
title: Ribbon. SizeDefinitions, proprietà
description: Rappresenta un contenitore per i modelli di layout personalizzati dei controlli della barra multifunzione.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. SizeDefinitions
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047946"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="b1b2c-104">Ribbon. SizeDefinitions, proprietà</span><span class="sxs-lookup"><span data-stu-id="b1b2c-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="b1b2c-105">Rappresenta un contenitore per i modelli di layout personalizzati dei controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="b1b2c-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="b1b2c-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b1b2c-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b1b2c-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="b1b2c-107">Attributes</span></span>

<span data-ttu-id="b1b2c-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="b1b2c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b1b2c-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b1b2c-109">Child elements</span></span>



| <span data-ttu-id="b1b2c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1b2c-110">Element</span></span>                                                                   | <span data-ttu-id="b1b2c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1b2c-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b1b2c-112">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="b1b2c-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="b1b2c-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="b1b2c-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b1b2c-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b1b2c-114">Parent elements</span></span>



| <span data-ttu-id="b1b2c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1b2c-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="b1b2c-116">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="b1b2c-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b1b2c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1b2c-117">Remarks</span></span>

<span data-ttu-id="b1b2c-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b1b2c-118">Optional.</span></span>

<span data-ttu-id="b1b2c-119">Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="b1b2c-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b1b2c-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1b2c-120">Examples</span></span>

<span data-ttu-id="b1b2c-121">Nell'esempio di codice riportato di seguito viene illustrato un modello personalizzato di base.</span><span class="sxs-lookup"><span data-stu-id="b1b2c-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="b1b2c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1b2c-122">Requirements</span></span>



| <span data-ttu-id="b1b2c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b2c-123">Requirement</span></span> | <span data-ttu-id="b1b2c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b1b2c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b1b2c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b2c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b2c-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1b2c-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b1b2c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b2c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b2c-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1b2c-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1b2c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1b2c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b2c-130">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="b1b2c-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





