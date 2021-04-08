---
description: Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: Async (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058131"
---
# <a name="async-element"></a><span data-ttu-id="2461d-103">Async (elemento)</span><span class="sxs-lookup"><span data-stu-id="2461d-103">async element</span></span>

<span data-ttu-id="2461d-104">Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.</span><span class="sxs-lookup"><span data-stu-id="2461d-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="2461d-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2461d-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="2461d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="2461d-106">Attributes</span></span>

<span data-ttu-id="2461d-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="2461d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2461d-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2461d-108">Child elements</span></span>

<span data-ttu-id="2461d-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="2461d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2461d-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2461d-110">Parent elements</span></span>



| <span data-ttu-id="2461d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="2461d-111">Element</span></span>                                                                         | <span data-ttu-id="2461d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2461d-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2461d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2461d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="2461d-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="2461d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="2461d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2461d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="2461d-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="2461d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="2461d-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="2461d-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="2461d-118">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="2461d-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="2461d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2461d-119">Remarks</span></span>

<span data-ttu-id="2461d-120">I valori possibili sono 1 (operazioni asincrone incluse) e 0 (le operazioni asincrone predefinite sono escluse).</span><span class="sxs-lookup"><span data-stu-id="2461d-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="2461d-121">Un proxy può includere sia versioni asincrone che sincrone delle stesse operazioni.</span><span class="sxs-lookup"><span data-stu-id="2461d-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="2461d-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2461d-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2461d-123">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2461d-123">Minimum supported system</span></span><br/> | <span data-ttu-id="2461d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2461d-124">Windows Vista</span></span> |
| <span data-ttu-id="2461d-125">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="2461d-125">Can be empty</span></span>                        | <span data-ttu-id="2461d-126">Sì</span><span class="sxs-lookup"><span data-stu-id="2461d-126">Yes</span></span>           |



 

 




