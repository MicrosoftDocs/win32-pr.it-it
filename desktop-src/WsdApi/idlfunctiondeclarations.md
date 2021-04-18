---
description: Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310302"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="ebca8-103">elemento idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="ebca8-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="ebca8-104">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="ebca8-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="ebca8-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ebca8-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="ebca8-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="ebca8-106">Attributes</span></span>

<span data-ttu-id="ebca8-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="ebca8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ebca8-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ebca8-108">Child elements</span></span>



| <span data-ttu-id="ebca8-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebca8-109">Element</span></span>                                   | <span data-ttu-id="ebca8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebca8-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebca8-111">**async**</span><span class="sxs-lookup"><span data-stu-id="ebca8-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="ebca8-112">Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="ebca8-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="ebca8-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="ebca8-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="ebca8-114">Specifica se gli argomenti dell'evento correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="ebca8-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="ebca8-115">**eventi**</span><span class="sxs-lookup"><span data-stu-id="ebca8-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="ebca8-116">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="ebca8-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="ebca8-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="ebca8-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="ebca8-118">Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="ebca8-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="ebca8-119">**operazione**</span><span class="sxs-lookup"><span data-stu-id="ebca8-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="ebca8-120">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="ebca8-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="ebca8-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="ebca8-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="ebca8-122">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="ebca8-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="ebca8-123">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ebca8-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="ebca8-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ebca8-124">Parent elements</span></span>



| <span data-ttu-id="ebca8-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebca8-125">Element</span></span>                         | <span data-ttu-id="ebca8-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebca8-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ebca8-127">**file**</span><span class="sxs-lookup"><span data-stu-id="ebca8-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ebca8-128">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="ebca8-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ebca8-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebca8-129">Remarks</span></span>

<span data-ttu-id="ebca8-130">Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto.</span><span class="sxs-lookup"><span data-stu-id="ebca8-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="ebca8-131">Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte del compilatore MIDL e vengono in genere utilizzate nei file IDL.</span><span class="sxs-lookup"><span data-stu-id="ebca8-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="ebca8-132">Esempio:</span><span class="sxs-lookup"><span data-stu-id="ebca8-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="ebca8-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ebca8-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ebca8-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebca8-134">Minimum supported system</span></span><br/> | <span data-ttu-id="ebca8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebca8-135">Windows Vista</span></span> |
| <span data-ttu-id="ebca8-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="ebca8-136">Can be empty</span></span>                        | <span data-ttu-id="ebca8-137">Sì</span><span class="sxs-lookup"><span data-stu-id="ebca8-137">Yes</span></span>           |



 

 




