---
description: Specifica se gli eventi correlati sono inclusi nelle funzioni generate.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: Elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226927"
---
# <a name="events-element"></a><span data-ttu-id="03f83-103">Elemento Events</span><span class="sxs-lookup"><span data-stu-id="03f83-103">events element</span></span>

<span data-ttu-id="03f83-104">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="03f83-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="03f83-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="03f83-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="03f83-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="03f83-106">Attributes</span></span>

<span data-ttu-id="03f83-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="03f83-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="03f83-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="03f83-108">Child elements</span></span>

<span data-ttu-id="03f83-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="03f83-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="03f83-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="03f83-110">Parent elements</span></span>



| <span data-ttu-id="03f83-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="03f83-111">Element</span></span>                                                                         | <span data-ttu-id="03f83-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03f83-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03f83-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="03f83-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="03f83-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="03f83-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="03f83-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="03f83-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="03f83-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="03f83-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="03f83-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="03f83-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="03f83-118">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="03f83-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="03f83-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="03f83-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="03f83-120">Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="03f83-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="03f83-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="03f83-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="03f83-122">Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="03f83-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="03f83-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="03f83-123">Remarks</span></span>

<span data-ttu-id="03f83-124">I valori possibili sono 1 (eventi inclusi) e 0 (impostazione predefinita, eventi esclusi).</span><span class="sxs-lookup"><span data-stu-id="03f83-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="03f83-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03f83-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="03f83-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03f83-126">Minimum supported system</span></span><br/> | <span data-ttu-id="03f83-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f83-127">Windows Vista</span></span> |
| <span data-ttu-id="03f83-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="03f83-128">Can be empty</span></span>                        | <span data-ttu-id="03f83-129">Sì</span><span class="sxs-lookup"><span data-stu-id="03f83-129">Yes</span></span>           |



 

 




