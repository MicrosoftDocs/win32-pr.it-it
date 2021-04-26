---
description: Specifica il deallocatore di tipo che deve essere utilizzato da una funzione stub di operazioni.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994288"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="fa8d0-103">elemento operationDeallocator</span><span class="sxs-lookup"><span data-stu-id="fa8d0-103">operationDeallocator element</span></span>

<span data-ttu-id="fa8d0-104">Specifica il deallocatore di tipo che deve essere usato dalla funzione stub di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="fa8d0-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fa8d0-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="fa8d0-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="fa8d0-106">Attributes</span></span>



| <span data-ttu-id="fa8d0-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="fa8d0-107">Attribute</span></span>                  | <span data-ttu-id="fa8d0-108">Type</span><span class="sxs-lookup"><span data-stu-id="fa8d0-108">Type</span></span>                         | <span data-ttu-id="fa8d0-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fa8d0-109">Required</span></span>       | <span data-ttu-id="fa8d0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa8d0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8d0-111">**deallocatore**</span><span class="sxs-lookup"><span data-stu-id="fa8d0-111">**deallocator**</span></span><br/> | <span data-ttu-id="fa8d0-112">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="fa8d0-112">character\_string</span></span><br/> | <span data-ttu-id="fa8d0-113">Sì</span><span class="sxs-lookup"><span data-stu-id="fa8d0-113">Yes</span></span><br/> | <span data-ttu-id="fa8d0-114">Deallocatore da utilizzare per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="fa8d0-115">Le stringhe seguenti sono valori validi.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="fa8d0-116"><span id="none"></span><span id="NONE"></span><dt>***Nessuno\*\*\*\*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>***WSDFreeLinkedMemory***</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt> <span id="free"></span> <span id="FREE"></span> <dt>***Gratuito\*\*\*\*</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>\*\*\*\*elimina\*\*\*\*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>\*\*\*\*deleteArray\*\*\*\*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>\*\*\*\*Versione\*\*\*\*</dt></span><span class="sxs-lookup"><span data-stu-id="fa8d0-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="fa8d0-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="fa8d0-117">**operation**</span></span><br/>   | <span data-ttu-id="fa8d0-118">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="fa8d0-118">character\_string</span></span><br/> | <span data-ttu-id="fa8d0-119">Sì</span><span class="sxs-lookup"><span data-stu-id="fa8d0-119">Yes</span></span><br/> | <span data-ttu-id="fa8d0-120">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="fa8d0-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fa8d0-121">Child elements</span></span>

<span data-ttu-id="fa8d0-122">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fa8d0-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fa8d0-123">Parent elements</span></span>



| <span data-ttu-id="fa8d0-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa8d0-124">Element</span></span>                                               | <span data-ttu-id="fa8d0-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa8d0-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa8d0-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="fa8d0-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="fa8d0-127">Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="fa8d0-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fa8d0-128">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fa8d0-128">Element information</span></span>



| <span data-ttu-id="fa8d0-129">Label</span><span class="sxs-lookup"><span data-stu-id="fa8d0-129">Label</span></span> | <span data-ttu-id="fa8d0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="fa8d0-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fa8d0-131">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa8d0-131">Minimum supported system</span></span><br/> | <span data-ttu-id="fa8d0-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa8d0-132">Windows Vista</span></span> |
| <span data-ttu-id="fa8d0-133">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="fa8d0-133">Can be empty</span></span>                        | <span data-ttu-id="fa8d0-134">Sì</span><span class="sxs-lookup"><span data-stu-id="fa8d0-134">Yes</span></span>           |



 

 




