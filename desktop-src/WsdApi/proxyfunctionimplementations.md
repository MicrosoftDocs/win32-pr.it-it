---
description: Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: Elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995758"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="11727-103">Elemento proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="11727-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="11727-104">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="11727-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="11727-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="11727-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="11727-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="11727-106">Attributes</span></span>

<span data-ttu-id="11727-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="11727-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="11727-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="11727-108">Child elements</span></span>



| <span data-ttu-id="11727-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="11727-109">Element</span></span>                                     | <span data-ttu-id="11727-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11727-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11727-111">**async**</span><span class="sxs-lookup"><span data-stu-id="11727-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="11727-112">Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="11727-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="11727-113">**Eventi**</span><span class="sxs-lookup"><span data-stu-id="11727-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="11727-114">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="11727-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="11727-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="11727-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="11727-116">Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="11727-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="11727-117">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="11727-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="11727-118">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="11727-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="11727-119">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="11727-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="11727-120">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="11727-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="11727-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="11727-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="11727-122">Specifica il nome della classe proxy sul lato client.</span><span class="sxs-lookup"><span data-stu-id="11727-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="11727-123">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="11727-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="11727-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="11727-124">Parent elements</span></span>



| <span data-ttu-id="11727-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="11727-125">Element</span></span>                         | <span data-ttu-id="11727-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11727-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="11727-127">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="11727-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="11727-128">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="11727-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="11727-129">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="11727-129">Element information</span></span>



| <span data-ttu-id="11727-130">Label</span><span class="sxs-lookup"><span data-stu-id="11727-130">Label</span></span> | <span data-ttu-id="11727-131">Valore</span><span class="sxs-lookup"><span data-stu-id="11727-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="11727-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11727-132">Minimum supported system</span></span><br/> | <span data-ttu-id="11727-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11727-133">Windows Vista</span></span> |
| <span data-ttu-id="11727-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="11727-134">Can be empty</span></span>                        | <span data-ttu-id="11727-135">Sì</span><span class="sxs-lookup"><span data-stu-id="11727-135">Yes</span></span>           |



 

 




