---
description: Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129099"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="601ee-103">elemento subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="601ee-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="601ee-104">Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="601ee-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="601ee-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="601ee-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="601ee-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="601ee-106">Attributes</span></span>



| <span data-ttu-id="601ee-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="601ee-107">Attribute</span></span>                 | <span data-ttu-id="601ee-108">Type</span><span class="sxs-lookup"><span data-stu-id="601ee-108">Type</span></span>               | <span data-ttu-id="601ee-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="601ee-109">Required</span></span>      | <span data-ttu-id="601ee-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601ee-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="601ee-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="601ee-111">**extensible**</span></span><br/> | <span data-ttu-id="601ee-112">boolean</span><span class="sxs-lookup"><span data-stu-id="601ee-112">boolean</span></span><br/> | <span data-ttu-id="601ee-113">No</span><span class="sxs-lookup"><span data-stu-id="601ee-113">No</span></span><br/> | <span data-ttu-id="601ee-114">Possibilità di aggiungere punti di estensibilità alle funzioni e alle interfacce.</span><span class="sxs-lookup"><span data-stu-id="601ee-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="601ee-115">Questo valore è sempre impostato su true.</span><span class="sxs-lookup"><span data-stu-id="601ee-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="601ee-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="601ee-116">Child elements</span></span>



| <span data-ttu-id="601ee-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="601ee-117">Element</span></span>                                                           | <span data-ttu-id="601ee-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601ee-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="601ee-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="601ee-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="601ee-120">Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="601ee-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="601ee-121">**operazione**</span><span class="sxs-lookup"><span data-stu-id="601ee-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="601ee-122">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="601ee-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="601ee-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="601ee-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="601ee-124">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="601ee-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="601ee-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="601ee-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="601ee-126">Specifica il nome della classe proxy sul lato client.</span><span class="sxs-lookup"><span data-stu-id="601ee-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="601ee-127">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="601ee-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="601ee-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="601ee-128">Parent elements</span></span>



| <span data-ttu-id="601ee-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="601ee-129">Element</span></span>                         | <span data-ttu-id="601ee-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601ee-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="601ee-131">**file**</span><span class="sxs-lookup"><span data-stu-id="601ee-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="601ee-132">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="601ee-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="601ee-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="601ee-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="601ee-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="601ee-134">Minimum supported system</span></span><br/> | <span data-ttu-id="601ee-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="601ee-135">Windows Vista</span></span> |
| <span data-ttu-id="601ee-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="601ee-136">Can be empty</span></span>                        | <span data-ttu-id="601ee-137">Sì</span><span class="sxs-lookup"><span data-stu-id="601ee-137">Yes</span></span>           |



 

 




