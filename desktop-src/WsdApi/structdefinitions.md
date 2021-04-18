---
description: Genera definizioni della struttura C per i tipi noti.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313664"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="95ae1-103">elemento structDefinitions</span><span class="sxs-lookup"><span data-stu-id="95ae1-103">structDefinitions element</span></span>

<span data-ttu-id="95ae1-104">Genera definizioni della struttura C per i tipi noti.</span><span class="sxs-lookup"><span data-stu-id="95ae1-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="95ae1-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="95ae1-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="95ae1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="95ae1-106">Attributes</span></span>

<span data-ttu-id="95ae1-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="95ae1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="95ae1-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="95ae1-108">Child elements</span></span>

<span data-ttu-id="95ae1-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="95ae1-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="95ae1-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="95ae1-110">Parent elements</span></span>



| <span data-ttu-id="95ae1-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="95ae1-111">Element</span></span>                         | <span data-ttu-id="95ae1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95ae1-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="95ae1-113">**file**</span><span class="sxs-lookup"><span data-stu-id="95ae1-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="95ae1-114">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="95ae1-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="95ae1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="95ae1-115">Remarks</span></span>

<span data-ttu-id="95ae1-116">Alla maggior parte del codice generato e del codice dell'applicazione viene fatto riferimento a strutture per i tipi noti.</span><span class="sxs-lookup"><span data-stu-id="95ae1-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="95ae1-117">Questo elemento viene utilizzato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="95ae1-117">This element is used to generate include files.</span></span> <span data-ttu-id="95ae1-118">Questo elemento deve essere eseguito dopo un elemento [**structDeclarations**](structdeclarations.md) in modo che i riferimenti tra le strutture vengano gestiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="95ae1-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="95ae1-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="95ae1-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="95ae1-120">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95ae1-120">Minimum supported system</span></span><br/> | <span data-ttu-id="95ae1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95ae1-121">Windows Vista</span></span> |
| <span data-ttu-id="95ae1-122">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="95ae1-122">Can be empty</span></span>                        | <span data-ttu-id="95ae1-123">Sì</span><span class="sxs-lookup"><span data-stu-id="95ae1-123">Yes</span></span>           |



 

 




