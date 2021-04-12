---
description: Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232017"
---
# <a name="faultinfo-element"></a><span data-ttu-id="7106f-103">elemento faultInfo</span><span class="sxs-lookup"><span data-stu-id="7106f-103">faultInfo element</span></span>

<span data-ttu-id="7106f-104">Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="7106f-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="7106f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7106f-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="7106f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="7106f-106">Attributes</span></span>

<span data-ttu-id="7106f-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="7106f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7106f-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7106f-108">Child elements</span></span>

<span data-ttu-id="7106f-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="7106f-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7106f-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7106f-110">Parent elements</span></span>



| <span data-ttu-id="7106f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7106f-111">Element</span></span>                                                                         | <span data-ttu-id="7106f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7106f-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7106f-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="7106f-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="7106f-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="7106f-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="7106f-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="7106f-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="7106f-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="7106f-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="7106f-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="7106f-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="7106f-118">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="7106f-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="7106f-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="7106f-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="7106f-120">Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="7106f-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="7106f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7106f-121">Remarks</span></span>

<span data-ttu-id="7106f-122">I valori possibili sono 1 (parametri di errore inclusi) e 0 (parametri di errore esclusi).</span><span class="sxs-lookup"><span data-stu-id="7106f-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="7106f-123">Per impostazione predefinita, i parametri di errore vengono esclusi.</span><span class="sxs-lookup"><span data-stu-id="7106f-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="7106f-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7106f-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7106f-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7106f-125">Minimum supported system</span></span><br/> | <span data-ttu-id="7106f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7106f-126">Windows Vista</span></span> |
| <span data-ttu-id="7106f-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="7106f-127">Can be empty</span></span>                        | <span data-ttu-id="7106f-128">Sì</span><span class="sxs-lookup"><span data-stu-id="7106f-128">Yes</span></span>           |



 

 




