---
description: Genera dichiarazioni IDL per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: Elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d738dd06ccbf034702cbb7d6494a28a229d07
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995368"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="eced2-103">Elemento subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="eced2-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="eced2-104">Genera dichiarazioni IDL per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="eced2-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="eced2-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="eced2-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="eced2-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="eced2-106">Attributes</span></span>



| <span data-ttu-id="eced2-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="eced2-107">Attribute</span></span>                 | <span data-ttu-id="eced2-108">Type</span><span class="sxs-lookup"><span data-stu-id="eced2-108">Type</span></span>               | <span data-ttu-id="eced2-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="eced2-109">Required</span></span>      | <span data-ttu-id="eced2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eced2-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eced2-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="eced2-111">**extensible**</span></span><br/> | <span data-ttu-id="eced2-112">boolean</span><span class="sxs-lookup"><span data-stu-id="eced2-112">boolean</span></span><br/> | <span data-ttu-id="eced2-113">No</span><span class="sxs-lookup"><span data-stu-id="eced2-113">No</span></span><br/> | <span data-ttu-id="eced2-114">Possibilità di aggiungere punti di estendibilità a funzioni e interfacce.</span><span class="sxs-lookup"><span data-stu-id="eced2-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="eced2-115">Questo valore è sempre impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eced2-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="eced2-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="eced2-116">Child elements</span></span>



| <span data-ttu-id="eced2-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="eced2-117">Element</span></span>                                                           | <span data-ttu-id="eced2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eced2-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eced2-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="eced2-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="eced2-120">Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="eced2-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="eced2-121">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="eced2-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="eced2-122">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="eced2-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="eced2-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="eced2-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="eced2-124">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="eced2-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="eced2-125">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="eced2-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="eced2-126">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="eced2-126">Parent elements</span></span>



| <span data-ttu-id="eced2-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="eced2-127">Element</span></span>                         | <span data-ttu-id="eced2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eced2-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="eced2-129">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="eced2-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="eced2-130">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="eced2-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="eced2-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eced2-131">Element information</span></span>



| <span data-ttu-id="eced2-132">Label</span><span class="sxs-lookup"><span data-stu-id="eced2-132">Label</span></span> | <span data-ttu-id="eced2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="eced2-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="eced2-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eced2-134">Minimum supported system</span></span><br/> | <span data-ttu-id="eced2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eced2-135">Windows Vista</span></span> |
| <span data-ttu-id="eced2-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="eced2-136">Can be empty</span></span>                        | <span data-ttu-id="eced2-137">Sì</span><span class="sxs-lookup"><span data-stu-id="eced2-137">Yes</span></span>           |



 

 




