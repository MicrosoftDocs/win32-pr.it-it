---
description: Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883989"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="10605-103">elemento proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="10605-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="10605-104">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="10605-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="10605-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="10605-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="10605-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="10605-106">Attributes</span></span>

<span data-ttu-id="10605-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="10605-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="10605-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="10605-108">Child elements</span></span>



| <span data-ttu-id="10605-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="10605-109">Element</span></span>                                     | <span data-ttu-id="10605-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10605-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10605-111">**async**</span><span class="sxs-lookup"><span data-stu-id="10605-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="10605-112">Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="10605-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="10605-113">**eventi**</span><span class="sxs-lookup"><span data-stu-id="10605-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="10605-114">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="10605-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="10605-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="10605-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="10605-116">Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="10605-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="10605-117">**operazione**</span><span class="sxs-lookup"><span data-stu-id="10605-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="10605-118">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="10605-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="10605-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="10605-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="10605-120">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="10605-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="10605-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="10605-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="10605-122">Specifica il nome della classe proxy sul lato client.</span><span class="sxs-lookup"><span data-stu-id="10605-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="10605-123">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="10605-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="10605-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="10605-124">Parent elements</span></span>



| <span data-ttu-id="10605-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="10605-125">Element</span></span>                         | <span data-ttu-id="10605-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10605-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="10605-127">**file**</span><span class="sxs-lookup"><span data-stu-id="10605-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="10605-128">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="10605-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="10605-129">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="10605-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="10605-130">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10605-130">Minimum supported system</span></span><br/> | <span data-ttu-id="10605-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10605-131">Windows Vista</span></span> |
| <span data-ttu-id="10605-132">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="10605-132">Can be empty</span></span>                        | <span data-ttu-id="10605-133">Sì</span><span class="sxs-lookup"><span data-stu-id="10605-133">Yes</span></span>           |



 

 




