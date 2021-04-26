---
description: Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: Elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995858"
---
# <a name="faultinfo-element"></a><span data-ttu-id="74285-103">Elemento faultInfo</span><span class="sxs-lookup"><span data-stu-id="74285-103">faultInfo element</span></span>

<span data-ttu-id="74285-104">Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="74285-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="74285-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="74285-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="74285-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="74285-106">Attributes</span></span>

<span data-ttu-id="74285-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="74285-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="74285-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="74285-108">Child elements</span></span>

<span data-ttu-id="74285-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="74285-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="74285-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="74285-110">Parent elements</span></span>



| <span data-ttu-id="74285-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="74285-111">Element</span></span>                                                                         | <span data-ttu-id="74285-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74285-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74285-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="74285-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="74285-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="74285-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="74285-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="74285-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="74285-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="74285-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="74285-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="74285-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="74285-118">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="74285-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="74285-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="74285-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="74285-120">Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="74285-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="74285-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="74285-121">Remarks</span></span>

<span data-ttu-id="74285-122">I valori possibili sono 1 (parametri di errore inclusi) e 0 (parametri di errore esclusi).</span><span class="sxs-lookup"><span data-stu-id="74285-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="74285-123">Per impostazione predefinita, i parametri di errore sono esclusi.</span><span class="sxs-lookup"><span data-stu-id="74285-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="74285-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="74285-124">Element information</span></span>



| <span data-ttu-id="74285-125">Label</span><span class="sxs-lookup"><span data-stu-id="74285-125">Label</span></span> | <span data-ttu-id="74285-126">Valore</span><span class="sxs-lookup"><span data-stu-id="74285-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="74285-127">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74285-127">Minimum supported system</span></span><br/> | <span data-ttu-id="74285-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74285-128">Windows Vista</span></span> |
| <span data-ttu-id="74285-129">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="74285-129">Can be empty</span></span>                        | <span data-ttu-id="74285-130">Sì</span><span class="sxs-lookup"><span data-stu-id="74285-130">Yes</span></span>           |



 

 




