---
description: Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento deallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994938"
---
# <a name="deallocator-element"></a><span data-ttu-id="ae7cb-103">elemento deallocator</span><span class="sxs-lookup"><span data-stu-id="ae7cb-103">deallocator element</span></span>

<span data-ttu-id="ae7cb-104">Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.</span><span class="sxs-lookup"><span data-stu-id="ae7cb-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="ae7cb-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ae7cb-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="ae7cb-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="ae7cb-106">Attributes</span></span>

<span data-ttu-id="ae7cb-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="ae7cb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ae7cb-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ae7cb-108">Child elements</span></span>

<span data-ttu-id="ae7cb-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="ae7cb-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ae7cb-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ae7cb-110">Parent elements</span></span>



| <span data-ttu-id="ae7cb-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="ae7cb-111">Element</span></span>                                               | <span data-ttu-id="ae7cb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae7cb-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae7cb-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ae7cb-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="ae7cb-114">Genera implementazioni per funzioni stub per operazioni di tipo porta.</span><span class="sxs-lookup"><span data-stu-id="ae7cb-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ae7cb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae7cb-115">Remarks</span></span>

<span data-ttu-id="ae7cb-116">Il tipo di deallocatore deve essere racchiuso in una coppia di <deallocator></deallocator> tag.</span><span class="sxs-lookup"><span data-stu-id="ae7cb-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="ae7cb-117">Le stringhe seguenti sono valori deallocatori validi:</span><span class="sxs-lookup"><span data-stu-id="ae7cb-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="ae7cb-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ae7cb-118">none</span></span>
-   <span data-ttu-id="ae7cb-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="ae7cb-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="ae7cb-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="ae7cb-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="ae7cb-121">free</span><span class="sxs-lookup"><span data-stu-id="ae7cb-121">free</span></span>
-   <span data-ttu-id="ae7cb-122">eliminare</span><span class="sxs-lookup"><span data-stu-id="ae7cb-122">delete</span></span>
-   <span data-ttu-id="ae7cb-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="ae7cb-123">deleteArray</span></span>
-   <span data-ttu-id="ae7cb-124">Versione</span><span class="sxs-lookup"><span data-stu-id="ae7cb-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="ae7cb-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ae7cb-125">Element information</span></span>



| <span data-ttu-id="ae7cb-126">Label</span><span class="sxs-lookup"><span data-stu-id="ae7cb-126">Label</span></span> | <span data-ttu-id="ae7cb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ae7cb-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ae7cb-128">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7cb-128">Minimum supported system</span></span><br/> | <span data-ttu-id="ae7cb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae7cb-129">Windows Vista</span></span> |
| <span data-ttu-id="ae7cb-130">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="ae7cb-130">Can be empty</span></span>                        | <span data-ttu-id="ae7cb-131">Sì</span><span class="sxs-lookup"><span data-stu-id="ae7cb-131">Yes</span></span>           |



 

 




