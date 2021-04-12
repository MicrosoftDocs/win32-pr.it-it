---
description: Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234315"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="68dd3-103">elemento subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="68dd3-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="68dd3-104">Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="68dd3-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="68dd3-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="68dd3-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="68dd3-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="68dd3-106">Attributes</span></span>



| <span data-ttu-id="68dd3-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="68dd3-107">Attribute</span></span>                 | <span data-ttu-id="68dd3-108">Type</span><span class="sxs-lookup"><span data-stu-id="68dd3-108">Type</span></span>               | <span data-ttu-id="68dd3-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="68dd3-109">Required</span></span>      | <span data-ttu-id="68dd3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68dd3-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68dd3-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="68dd3-111">**extensible**</span></span><br/> | <span data-ttu-id="68dd3-112">boolean</span><span class="sxs-lookup"><span data-stu-id="68dd3-112">boolean</span></span><br/> | <span data-ttu-id="68dd3-113">No</span><span class="sxs-lookup"><span data-stu-id="68dd3-113">No</span></span><br/> | <span data-ttu-id="68dd3-114">Possibilità di aggiungere punti di estensibilità alle funzioni e alle interfacce.</span><span class="sxs-lookup"><span data-stu-id="68dd3-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="68dd3-115">Questo valore è sempre impostato su true.</span><span class="sxs-lookup"><span data-stu-id="68dd3-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="68dd3-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="68dd3-116">Child elements</span></span>



| <span data-ttu-id="68dd3-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="68dd3-117">Element</span></span>                                                           | <span data-ttu-id="68dd3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68dd3-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68dd3-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="68dd3-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="68dd3-120">Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="68dd3-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="68dd3-121">**operazione**</span><span class="sxs-lookup"><span data-stu-id="68dd3-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="68dd3-122">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="68dd3-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="68dd3-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="68dd3-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="68dd3-124">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="68dd3-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="68dd3-125">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="68dd3-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="68dd3-126">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="68dd3-126">Parent elements</span></span>



| <span data-ttu-id="68dd3-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="68dd3-127">Element</span></span>                         | <span data-ttu-id="68dd3-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68dd3-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="68dd3-129">**file**</span><span class="sxs-lookup"><span data-stu-id="68dd3-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="68dd3-130">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="68dd3-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="68dd3-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="68dd3-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="68dd3-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68dd3-132">Minimum supported system</span></span><br/> | <span data-ttu-id="68dd3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68dd3-133">Windows Vista</span></span> |
| <span data-ttu-id="68dd3-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="68dd3-134">Can be empty</span></span>                        | <span data-ttu-id="68dd3-135">Sì</span><span class="sxs-lookup"><span data-stu-id="68dd3-135">Yes</span></span>           |



 

 




