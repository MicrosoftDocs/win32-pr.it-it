---
description: Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: events - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995929"
---
# <a name="events-element"></a><span data-ttu-id="f65fa-103">elemento events</span><span class="sxs-lookup"><span data-stu-id="f65fa-103">events element</span></span>

<span data-ttu-id="f65fa-104">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="f65fa-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="f65fa-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f65fa-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="f65fa-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="f65fa-106">Attributes</span></span>

<span data-ttu-id="f65fa-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f65fa-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f65fa-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f65fa-108">Child elements</span></span>

<span data-ttu-id="f65fa-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f65fa-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f65fa-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f65fa-110">Parent elements</span></span>



| <span data-ttu-id="f65fa-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="f65fa-111">Element</span></span>                                                                         | <span data-ttu-id="f65fa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f65fa-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f65fa-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f65fa-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="f65fa-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="f65fa-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="f65fa-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f65fa-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="f65fa-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="f65fa-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="f65fa-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="f65fa-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="f65fa-118">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="f65fa-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="f65fa-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f65fa-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="f65fa-120">Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="f65fa-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="f65fa-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f65fa-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="f65fa-122">Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="f65fa-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="f65fa-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f65fa-123">Remarks</span></span>

<span data-ttu-id="f65fa-124">I valori possibili sono 1 (eventi inclusi) e 0 (impostazione predefinita, eventi esclusi).</span><span class="sxs-lookup"><span data-stu-id="f65fa-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="f65fa-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f65fa-125">Element information</span></span>



| <span data-ttu-id="f65fa-126">Label</span><span class="sxs-lookup"><span data-stu-id="f65fa-126">Label</span></span> | <span data-ttu-id="f65fa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f65fa-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f65fa-128">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f65fa-128">Minimum supported system</span></span><br/> | <span data-ttu-id="f65fa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f65fa-129">Windows Vista</span></span> |
| <span data-ttu-id="f65fa-130">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f65fa-130">Can be empty</span></span>                        | <span data-ttu-id="f65fa-131">Sì</span><span class="sxs-lookup"><span data-stu-id="f65fa-131">Yes</span></span>           |



 

 




