---
description: Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: elemento async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994958"
---
# <a name="async-element"></a><span data-ttu-id="0ade9-103">elemento async</span><span class="sxs-lookup"><span data-stu-id="0ade9-103">async element</span></span>

<span data-ttu-id="0ade9-104">Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="0ade9-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="0ade9-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ade9-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="0ade9-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0ade9-106">Attributes</span></span>

<span data-ttu-id="0ade9-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0ade9-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0ade9-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0ade9-108">Child elements</span></span>

<span data-ttu-id="0ade9-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="0ade9-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0ade9-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0ade9-110">Parent elements</span></span>



| <span data-ttu-id="0ade9-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ade9-111">Element</span></span>                                                                         | <span data-ttu-id="0ade9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ade9-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ade9-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="0ade9-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="0ade9-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="0ade9-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="0ade9-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="0ade9-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="0ade9-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="0ade9-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="0ade9-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="0ade9-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="0ade9-118">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="0ade9-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="0ade9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ade9-119">Remarks</span></span>

<span data-ttu-id="0ade9-120">I valori possibili sono 1 (operazioni asincrone incluse) e 0 (impostazione predefinita, operazioni asincrone escluse).</span><span class="sxs-lookup"><span data-stu-id="0ade9-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="0ade9-121">Un proxy può avere versioni asincrone e sincrone delle stesse operazioni.</span><span class="sxs-lookup"><span data-stu-id="0ade9-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="0ade9-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0ade9-122">Element information</span></span>



| <span data-ttu-id="0ade9-123">Label</span><span class="sxs-lookup"><span data-stu-id="0ade9-123">Label</span></span> | <span data-ttu-id="0ade9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0ade9-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0ade9-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ade9-125">Minimum supported system</span></span><br/> | <span data-ttu-id="0ade9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ade9-126">Windows Vista</span></span> |
| <span data-ttu-id="0ade9-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0ade9-127">Can be empty</span></span>                        | <span data-ttu-id="0ade9-128">Sì</span><span class="sxs-lookup"><span data-stu-id="0ade9-128">Yes</span></span>           |



 

 




