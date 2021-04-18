---
description: Specifica il deallocatore del tipo che deve essere utilizzato da una funzione stub delle operazioni.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312684"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="c35dd-103">elemento operationDeallocator</span><span class="sxs-lookup"><span data-stu-id="c35dd-103">operationDeallocator element</span></span>

<span data-ttu-id="c35dd-104">Specifica il deallocatore di tipo che deve essere utilizzato dalla funzione stub di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="c35dd-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="c35dd-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c35dd-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="c35dd-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="c35dd-106">Attributes</span></span>



| <span data-ttu-id="c35dd-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="c35dd-107">Attribute</span></span>                  | <span data-ttu-id="c35dd-108">Type</span><span class="sxs-lookup"><span data-stu-id="c35dd-108">Type</span></span>                         | <span data-ttu-id="c35dd-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c35dd-109">Required</span></span>       | <span data-ttu-id="c35dd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c35dd-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c35dd-111">**deallocatore**</span><span class="sxs-lookup"><span data-stu-id="c35dd-111">**deallocator**</span></span><br/> | <span data-ttu-id="c35dd-112">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="c35dd-112">character\_string</span></span><br/> | <span data-ttu-id="c35dd-113">Sì</span><span class="sxs-lookup"><span data-stu-id="c35dd-113">Yes</span></span><br/> | <span data-ttu-id="c35dd-114">Il deallocatore da utilizzare per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c35dd-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="c35dd-115">Le stringhe seguenti sono valori validi.</span><span class="sxs-lookup"><span data-stu-id="c35dd-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="c35dd-116"><span id="none"></span><span id="NONE"></span>\* \* \* \* <dt>Nessuna \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* \* \* \* <dt>WSDFreeLinkedMemory \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* \* \* \* \* <dt>CoTaskMemFree \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* <dt></dt> <span id="delete"></span> <span id="DELETE"></span> \* \* \* \* <dt>Elimina \* \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* \* \* <dt>deleteArray \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* \* \* \* <dt>Versione \*</dt> \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c35dd-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="c35dd-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="c35dd-117">**operation**</span></span><br/>   | <span data-ttu-id="c35dd-118">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="c35dd-118">character\_string</span></span><br/> | <span data-ttu-id="c35dd-119">Sì</span><span class="sxs-lookup"><span data-stu-id="c35dd-119">Yes</span></span><br/> | <span data-ttu-id="c35dd-120">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c35dd-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="c35dd-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c35dd-121">Child elements</span></span>

<span data-ttu-id="c35dd-122">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="c35dd-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c35dd-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c35dd-123">Parent elements</span></span>



| <span data-ttu-id="c35dd-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="c35dd-124">Element</span></span>                                               | <span data-ttu-id="c35dd-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c35dd-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c35dd-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="c35dd-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="c35dd-127">Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="c35dd-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c35dd-128">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c35dd-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c35dd-129">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c35dd-129">Minimum supported system</span></span><br/> | <span data-ttu-id="c35dd-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c35dd-130">Windows Vista</span></span> |
| <span data-ttu-id="c35dd-131">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="c35dd-131">Can be empty</span></span>                        | <span data-ttu-id="c35dd-132">Sì</span><span class="sxs-lookup"><span data-stu-id="c35dd-132">Yes</span></span>           |



 

 




