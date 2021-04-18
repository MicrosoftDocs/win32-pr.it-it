---
description: Genera implementazioni per le funzioni stub per le operazioni di tipo porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313145"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="e159f-103">elemento stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="e159f-103">stubDefinitions element</span></span>

<span data-ttu-id="e159f-104">Genera implementazioni per le funzioni stub per le operazioni di tipo porta.</span><span class="sxs-lookup"><span data-stu-id="e159f-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="e159f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e159f-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="e159f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="e159f-106">Attributes</span></span>

<span data-ttu-id="e159f-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="e159f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e159f-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e159f-108">Child elements</span></span>



| <span data-ttu-id="e159f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e159f-109">Element</span></span>                                                         | <span data-ttu-id="e159f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e159f-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e159f-111">**deallocatore**</span><span class="sxs-lookup"><span data-stu-id="e159f-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="e159f-112">Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.</span><span class="sxs-lookup"><span data-stu-id="e159f-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="e159f-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="e159f-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="e159f-114">Specifica se gli argomenti dell'evento correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="e159f-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="e159f-115">**eventi**</span><span class="sxs-lookup"><span data-stu-id="e159f-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="e159f-116">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="e159f-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="e159f-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="e159f-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="e159f-118">Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="e159f-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="e159f-119">**operazione**</span><span class="sxs-lookup"><span data-stu-id="e159f-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="e159f-120">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="e159f-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="e159f-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="e159f-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="e159f-122">Specifica il tipo di deallocatore che deve essere utilizzato dalla funzione stub di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="e159f-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="e159f-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="e159f-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="e159f-124">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="e159f-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="e159f-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="e159f-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="e159f-126">Specifica il nome della classe server sul lato host.</span><span class="sxs-lookup"><span data-stu-id="e159f-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="e159f-127">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e159f-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e159f-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e159f-128">Parent elements</span></span>



| <span data-ttu-id="e159f-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="e159f-129">Element</span></span>                         | <span data-ttu-id="e159f-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e159f-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e159f-131">**file**</span><span class="sxs-lookup"><span data-stu-id="e159f-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e159f-132">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="e159f-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e159f-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e159f-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e159f-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e159f-134">Minimum supported system</span></span><br/> | <span data-ttu-id="e159f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e159f-135">Windows Vista</span></span> |
| <span data-ttu-id="e159f-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="e159f-136">Can be empty</span></span>                        | <span data-ttu-id="e159f-137">No</span><span class="sxs-lookup"><span data-stu-id="e159f-137">No</span></span>            |



 

 




