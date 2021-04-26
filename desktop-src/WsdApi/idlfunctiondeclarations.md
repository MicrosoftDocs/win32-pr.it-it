---
description: Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: Elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994738"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="59c2f-103">Elemento idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="59c2f-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="59c2f-104">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="59c2f-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="59c2f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="59c2f-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="59c2f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="59c2f-106">Attributes</span></span>

<span data-ttu-id="59c2f-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="59c2f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="59c2f-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="59c2f-108">Child elements</span></span>



| <span data-ttu-id="59c2f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="59c2f-109">Element</span></span>                                   | <span data-ttu-id="59c2f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c2f-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c2f-111">**async**</span><span class="sxs-lookup"><span data-stu-id="59c2f-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="59c2f-112">Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="59c2f-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="59c2f-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="59c2f-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="59c2f-114">Specifica se gli argomenti dell'evento correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="59c2f-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="59c2f-115">**Eventi**</span><span class="sxs-lookup"><span data-stu-id="59c2f-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="59c2f-116">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="59c2f-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="59c2f-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="59c2f-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="59c2f-118">Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="59c2f-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="59c2f-119">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="59c2f-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="59c2f-120">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="59c2f-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="59c2f-121">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="59c2f-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="59c2f-122">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="59c2f-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="59c2f-123">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="59c2f-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="59c2f-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="59c2f-124">Parent elements</span></span>



| <span data-ttu-id="59c2f-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="59c2f-125">Element</span></span>                         | <span data-ttu-id="59c2f-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c2f-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="59c2f-127">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="59c2f-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="59c2f-128">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="59c2f-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="59c2f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="59c2f-129">Remarks</span></span>

<span data-ttu-id="59c2f-130">Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto.</span><span class="sxs-lookup"><span data-stu-id="59c2f-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="59c2f-131">Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte del compilatore MIDL e vengono in genere usate nei file con estensione idl.</span><span class="sxs-lookup"><span data-stu-id="59c2f-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="59c2f-132">Esempio:</span><span class="sxs-lookup"><span data-stu-id="59c2f-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="59c2f-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="59c2f-133">Element information</span></span>



| <span data-ttu-id="59c2f-134">Label</span><span class="sxs-lookup"><span data-stu-id="59c2f-134">Label</span></span> | <span data-ttu-id="59c2f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="59c2f-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="59c2f-136">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c2f-136">Minimum supported system</span></span><br/> | <span data-ttu-id="59c2f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59c2f-137">Windows Vista</span></span> |
| <span data-ttu-id="59c2f-138">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="59c2f-138">Can be empty</span></span>                        | <span data-ttu-id="59c2f-139">Sì</span><span class="sxs-lookup"><span data-stu-id="59c2f-139">Yes</span></span>           |



 

 




