---
description: Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995318"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="662d3-103">subscriptionProxyFunctionImplementations - elemento</span><span class="sxs-lookup"><span data-stu-id="662d3-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="662d3-104">Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="662d3-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="662d3-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="662d3-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="662d3-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="662d3-106">Attributes</span></span>



| <span data-ttu-id="662d3-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="662d3-107">Attribute</span></span>                 | <span data-ttu-id="662d3-108">Type</span><span class="sxs-lookup"><span data-stu-id="662d3-108">Type</span></span>               | <span data-ttu-id="662d3-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="662d3-109">Required</span></span>      | <span data-ttu-id="662d3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="662d3-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="662d3-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="662d3-111">**extensible**</span></span><br/> | <span data-ttu-id="662d3-112">boolean</span><span class="sxs-lookup"><span data-stu-id="662d3-112">boolean</span></span><br/> | <span data-ttu-id="662d3-113">No</span><span class="sxs-lookup"><span data-stu-id="662d3-113">No</span></span><br/> | <span data-ttu-id="662d3-114">Possibilità di aggiungere punti di estendibilità a funzioni e interfacce.</span><span class="sxs-lookup"><span data-stu-id="662d3-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="662d3-115">Questo valore è sempre impostato su true.</span><span class="sxs-lookup"><span data-stu-id="662d3-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="662d3-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="662d3-116">Child elements</span></span>



| <span data-ttu-id="662d3-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="662d3-117">Element</span></span>                                                           | <span data-ttu-id="662d3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="662d3-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="662d3-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="662d3-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="662d3-120">Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="662d3-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="662d3-121">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="662d3-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="662d3-122">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="662d3-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="662d3-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="662d3-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="662d3-124">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="662d3-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="662d3-125">**classe proxy**</span><span class="sxs-lookup"><span data-stu-id="662d3-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="662d3-126">Specifica il nome della classe proxy lato client.</span><span class="sxs-lookup"><span data-stu-id="662d3-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="662d3-127">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="662d3-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="662d3-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="662d3-128">Parent elements</span></span>



| <span data-ttu-id="662d3-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="662d3-129">Element</span></span>                         | <span data-ttu-id="662d3-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="662d3-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="662d3-131">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="662d3-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="662d3-132">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="662d3-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="662d3-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="662d3-133">Element information</span></span>



| <span data-ttu-id="662d3-134">Label</span><span class="sxs-lookup"><span data-stu-id="662d3-134">Label</span></span> | <span data-ttu-id="662d3-135">Valore</span><span class="sxs-lookup"><span data-stu-id="662d3-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="662d3-136">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="662d3-136">Minimum supported system</span></span><br/> | <span data-ttu-id="662d3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="662d3-137">Windows Vista</span></span> |
| <span data-ttu-id="662d3-138">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="662d3-138">Can be empty</span></span>                        | <span data-ttu-id="662d3-139">Sì</span><span class="sxs-lookup"><span data-stu-id="662d3-139">Yes</span></span>           |



 

 




