---
description: Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: Elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998818"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="fd324-103">Elemento functionDeclarations</span><span class="sxs-lookup"><span data-stu-id="fd324-103">functionDeclarations element</span></span>

<span data-ttu-id="fd324-104">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="fd324-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="fd324-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fd324-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="fd324-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="fd324-106">Attributes</span></span>

<span data-ttu-id="fd324-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="fd324-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd324-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fd324-108">Child elements</span></span>



| <span data-ttu-id="fd324-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd324-109">Element</span></span>                                   | <span data-ttu-id="fd324-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd324-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd324-111">**async**</span><span class="sxs-lookup"><span data-stu-id="fd324-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="fd324-112">Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="fd324-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="fd324-113">**Eventi**</span><span class="sxs-lookup"><span data-stu-id="fd324-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="fd324-114">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="fd324-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="fd324-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="fd324-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="fd324-116">Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="fd324-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="fd324-117">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="fd324-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="fd324-118">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="fd324-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="fd324-119">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="fd324-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="fd324-120">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="fd324-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="fd324-121">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fd324-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="fd324-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fd324-122">Parent elements</span></span>



| <span data-ttu-id="fd324-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd324-123">Element</span></span>                         | <span data-ttu-id="fd324-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd324-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fd324-125">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="fd324-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fd324-126">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="fd324-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fd324-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd324-127">Remarks</span></span>

<span data-ttu-id="fd324-128">Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto.</span><span class="sxs-lookup"><span data-stu-id="fd324-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="fd324-129">Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte di un compilatore C++ e vengono in genere usate nei file con estensione cpp.</span><span class="sxs-lookup"><span data-stu-id="fd324-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="fd324-130">Esempio:</span><span class="sxs-lookup"><span data-stu-id="fd324-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="fd324-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fd324-131">Element information</span></span>



| <span data-ttu-id="fd324-132">Label</span><span class="sxs-lookup"><span data-stu-id="fd324-132">Label</span></span> | <span data-ttu-id="fd324-133">Valore</span><span class="sxs-lookup"><span data-stu-id="fd324-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fd324-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd324-134">Minimum supported system</span></span><br/> | <span data-ttu-id="fd324-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd324-135">Windows Vista</span></span> |
| <span data-ttu-id="fd324-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="fd324-136">Can be empty</span></span>                        | <span data-ttu-id="fd324-137">Sì</span><span class="sxs-lookup"><span data-stu-id="fd324-137">Yes</span></span>           |



 

 




