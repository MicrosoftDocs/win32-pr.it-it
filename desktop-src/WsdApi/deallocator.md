---
description: Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento deallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226928"
---
# <a name="deallocator-element"></a><span data-ttu-id="988f8-103">elemento deallocator</span><span class="sxs-lookup"><span data-stu-id="988f8-103">deallocator element</span></span>

<span data-ttu-id="988f8-104">Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.</span><span class="sxs-lookup"><span data-stu-id="988f8-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="988f8-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="988f8-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="988f8-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="988f8-106">Attributes</span></span>

<span data-ttu-id="988f8-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="988f8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="988f8-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="988f8-108">Child elements</span></span>

<span data-ttu-id="988f8-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="988f8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="988f8-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="988f8-110">Parent elements</span></span>



| <span data-ttu-id="988f8-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="988f8-111">Element</span></span>                                               | <span data-ttu-id="988f8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="988f8-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="988f8-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="988f8-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="988f8-114">Genera implementazioni per le funzioni stub per le operazioni di tipo porta.</span><span class="sxs-lookup"><span data-stu-id="988f8-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="988f8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="988f8-115">Remarks</span></span>

<span data-ttu-id="988f8-116">Il tipo di deallocatore deve essere racchiuso in una coppia di <deallocator></deallocator> tag.</span><span class="sxs-lookup"><span data-stu-id="988f8-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="988f8-117">Le stringhe seguenti sono valori di deallocator validi:</span><span class="sxs-lookup"><span data-stu-id="988f8-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="988f8-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="988f8-118">none</span></span>
-   <span data-ttu-id="988f8-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="988f8-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="988f8-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="988f8-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="988f8-121">free</span><span class="sxs-lookup"><span data-stu-id="988f8-121">free</span></span>
-   <span data-ttu-id="988f8-122">eliminare</span><span class="sxs-lookup"><span data-stu-id="988f8-122">delete</span></span>
-   <span data-ttu-id="988f8-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="988f8-123">deleteArray</span></span>
-   <span data-ttu-id="988f8-124">Versione</span><span class="sxs-lookup"><span data-stu-id="988f8-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="988f8-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="988f8-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="988f8-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="988f8-126">Minimum supported system</span></span><br/> | <span data-ttu-id="988f8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="988f8-127">Windows Vista</span></span> |
| <span data-ttu-id="988f8-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="988f8-128">Can be empty</span></span>                        | <span data-ttu-id="988f8-129">Sì</span><span class="sxs-lookup"><span data-stu-id="988f8-129">Yes</span></span>           |



 

 




