---
description: Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231672"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="70a04-103">elemento functionDeclarations</span><span class="sxs-lookup"><span data-stu-id="70a04-103">functionDeclarations element</span></span>

<span data-ttu-id="70a04-104">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="70a04-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="70a04-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="70a04-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="70a04-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="70a04-106">Attributes</span></span>

<span data-ttu-id="70a04-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="70a04-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="70a04-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="70a04-108">Child elements</span></span>



| <span data-ttu-id="70a04-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="70a04-109">Element</span></span>                                   | <span data-ttu-id="70a04-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a04-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a04-111">**async**</span><span class="sxs-lookup"><span data-stu-id="70a04-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="70a04-112">Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="70a04-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="70a04-113">**eventi**</span><span class="sxs-lookup"><span data-stu-id="70a04-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="70a04-114">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="70a04-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="70a04-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="70a04-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="70a04-116">Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="70a04-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="70a04-117">**operazione**</span><span class="sxs-lookup"><span data-stu-id="70a04-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="70a04-118">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="70a04-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="70a04-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="70a04-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="70a04-120">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="70a04-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="70a04-121">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="70a04-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="70a04-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="70a04-122">Parent elements</span></span>



| <span data-ttu-id="70a04-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="70a04-123">Element</span></span>                         | <span data-ttu-id="70a04-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a04-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="70a04-125">**file**</span><span class="sxs-lookup"><span data-stu-id="70a04-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="70a04-126">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="70a04-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="70a04-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="70a04-127">Remarks</span></span>

<span data-ttu-id="70a04-128">Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto.</span><span class="sxs-lookup"><span data-stu-id="70a04-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="70a04-129">Queste dichiarazioni sono in un formato appropriato per l'utilizzo da un compilatore C++ e vengono in genere utilizzate nei file con estensione cpp.</span><span class="sxs-lookup"><span data-stu-id="70a04-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="70a04-130">Esempio:</span><span class="sxs-lookup"><span data-stu-id="70a04-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="70a04-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="70a04-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="70a04-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a04-132">Minimum supported system</span></span><br/> | <span data-ttu-id="70a04-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70a04-133">Windows Vista</span></span> |
| <span data-ttu-id="70a04-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="70a04-134">Can be empty</span></span>                        | <span data-ttu-id="70a04-135">Sì</span><span class="sxs-lookup"><span data-stu-id="70a04-135">Yes</span></span>           |



 

 




