---
description: Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884246"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="8a618-103">elemento subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="8a618-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="8a618-104">Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="8a618-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="8a618-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8a618-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="8a618-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="8a618-106">Attributes</span></span>



| <span data-ttu-id="8a618-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="8a618-107">Attribute</span></span>                 | <span data-ttu-id="8a618-108">Type</span><span class="sxs-lookup"><span data-stu-id="8a618-108">Type</span></span>               | <span data-ttu-id="8a618-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="8a618-109">Required</span></span>      | <span data-ttu-id="8a618-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a618-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a618-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="8a618-111">**extensible**</span></span><br/> | <span data-ttu-id="8a618-112">boolean</span><span class="sxs-lookup"><span data-stu-id="8a618-112">boolean</span></span><br/> | <span data-ttu-id="8a618-113">No</span><span class="sxs-lookup"><span data-stu-id="8a618-113">No</span></span><br/> | <span data-ttu-id="8a618-114">Possibilità di aggiungere punti di estensibilità alle funzioni e alle interfacce.</span><span class="sxs-lookup"><span data-stu-id="8a618-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="8a618-115">Questo valore è sempre impostato su true.</span><span class="sxs-lookup"><span data-stu-id="8a618-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8a618-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8a618-116">Child elements</span></span>



| <span data-ttu-id="8a618-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a618-117">Element</span></span>                                                           | <span data-ttu-id="8a618-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a618-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a618-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="8a618-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="8a618-120">Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="8a618-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="8a618-121">**operazione**</span><span class="sxs-lookup"><span data-stu-id="8a618-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="8a618-122">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="8a618-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="8a618-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="8a618-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="8a618-124">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="8a618-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="8a618-125">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8a618-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8a618-126">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8a618-126">Parent elements</span></span>



| <span data-ttu-id="8a618-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a618-127">Element</span></span>                         | <span data-ttu-id="8a618-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a618-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8a618-129">**file**</span><span class="sxs-lookup"><span data-stu-id="8a618-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8a618-130">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="8a618-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8a618-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8a618-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8a618-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a618-132">Minimum supported system</span></span><br/> | <span data-ttu-id="8a618-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a618-133">Windows Vista</span></span> |
| <span data-ttu-id="8a618-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="8a618-134">Can be empty</span></span>                        | <span data-ttu-id="8a618-135">Sì</span><span class="sxs-lookup"><span data-stu-id="8a618-135">Yes</span></span>           |



 

 




