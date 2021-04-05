---
title: Elemento Application
description: Rappresenta l'elemento di livello principale nella specifica di markup del Framework della barra multifunzione di Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Barra multifunzione Windows elemento applicazione
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734714"
---
# <a name="application-element"></a><span data-ttu-id="3bebe-104">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="3bebe-104">Application element</span></span>

<span data-ttu-id="3bebe-105">Rappresenta l'elemento di livello principale nella specifica di markup del Framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="3bebe-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="3bebe-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3bebe-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="3bebe-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="3bebe-107">Attributes</span></span>



| <span data-ttu-id="3bebe-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="3bebe-108">Attribute</span></span>            | <span data-ttu-id="3bebe-109">Type</span><span class="sxs-lookup"><span data-stu-id="3bebe-109">Type</span></span>                 | <span data-ttu-id="3bebe-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3bebe-110">Required</span></span>       | <span data-ttu-id="3bebe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bebe-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bebe-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="3bebe-112">**xmlns**</span></span><br/> | <span data-ttu-id="3bebe-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bebe-113">xs:string</span></span><br/> | <span data-ttu-id="3bebe-114">Sì</span><span class="sxs-lookup"><span data-stu-id="3bebe-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="3bebe-115">URI per l'associazione dello spazio dei nomi di markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="3bebe-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="3bebe-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3bebe-116">Child elements</span></span>



| <span data-ttu-id="3bebe-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="3bebe-117">Element</span></span>                                                                               | <span data-ttu-id="3bebe-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bebe-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="3bebe-119">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="3bebe-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="3bebe-120">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="3bebe-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="3bebe-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="3bebe-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="3bebe-122">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="3bebe-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3bebe-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3bebe-123">Parent elements</span></span>

<span data-ttu-id="3bebe-124">Non ci sono elementi padre.</span><span class="sxs-lookup"><span data-stu-id="3bebe-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bebe-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bebe-125">Remarks</span></span>

<span data-ttu-id="3bebe-126">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3bebe-126">Required.</span></span>

<span data-ttu-id="3bebe-127">Deve verificarsi esattamente una volta come contenitore per tutto il markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="3bebe-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="3bebe-128">Gli elementi figlio dell'elemento dell' **applicazione** devono essere presenti nell'ordine specificato:</span><span class="sxs-lookup"><span data-stu-id="3bebe-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="3bebe-129">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="3bebe-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="3bebe-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="3bebe-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="3bebe-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="3bebe-131">Examples</span></span>

<span data-ttu-id="3bebe-132">Nell'esempio seguente viene illustrata una dichiarazione di elemento **dell'applicazione** .</span><span class="sxs-lookup"><span data-stu-id="3bebe-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="3bebe-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3bebe-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3bebe-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bebe-134">Minimum supported system</span></span><br/> | <span data-ttu-id="3bebe-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bebe-135">Windows 7</span></span> |
| <span data-ttu-id="3bebe-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3bebe-136">Can be empty</span></span>                        | <span data-ttu-id="3bebe-137">No</span><span class="sxs-lookup"><span data-stu-id="3bebe-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="3bebe-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3bebe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bebe-139">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="3bebe-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





