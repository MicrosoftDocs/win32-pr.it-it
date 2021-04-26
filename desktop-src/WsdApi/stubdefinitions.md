---
description: Genera implementazioni per funzioni stub per operazioni di tipo porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: Elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994688"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="4d9d1-103">Elemento stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="4d9d1-103">stubDefinitions element</span></span>

<span data-ttu-id="4d9d1-104">Genera implementazioni per funzioni stub per operazioni di tipo porta.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="4d9d1-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4d9d1-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="4d9d1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="4d9d1-106">Attributes</span></span>

<span data-ttu-id="4d9d1-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4d9d1-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4d9d1-108">Child elements</span></span>



| <span data-ttu-id="4d9d1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4d9d1-109">Element</span></span>                                                         | <span data-ttu-id="4d9d1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d9d1-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d9d1-111">**deallocatore**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="4d9d1-112">Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="4d9d1-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="4d9d1-114">Specifica se gli argomenti di evento correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="4d9d1-115">**Eventi**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="4d9d1-116">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="4d9d1-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="4d9d1-118">Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="4d9d1-119">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="4d9d1-120">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="4d9d1-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="4d9d1-122">Specifica il tipo di deallocatore che deve essere usato dalla funzione stub di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="4d9d1-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="4d9d1-124">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="4d9d1-125">**classe server**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="4d9d1-126">Specifica il nome della classe server sul lato host.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="4d9d1-127">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4d9d1-127">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="4d9d1-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4d9d1-128">Parent elements</span></span>



| <span data-ttu-id="4d9d1-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="4d9d1-129">Element</span></span>                         | <span data-ttu-id="4d9d1-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d9d1-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4d9d1-131">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="4d9d1-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="4d9d1-132">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="4d9d1-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4d9d1-133">Element information</span></span>



| <span data-ttu-id="4d9d1-134">Label</span><span class="sxs-lookup"><span data-stu-id="4d9d1-134">Label</span></span> | <span data-ttu-id="4d9d1-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4d9d1-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="4d9d1-136">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d9d1-136">Minimum supported system</span></span><br/> | <span data-ttu-id="4d9d1-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d9d1-137">Windows Vista</span></span> |
| <span data-ttu-id="4d9d1-138">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="4d9d1-138">Can be empty</span></span>                        | <span data-ttu-id="4d9d1-139">No</span><span class="sxs-lookup"><span data-stu-id="4d9d1-139">No</span></span>            |



 

 




