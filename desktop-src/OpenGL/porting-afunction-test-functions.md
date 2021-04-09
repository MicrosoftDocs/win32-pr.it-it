---
title: Porting di funzioni di test AFunction
description: La tabella seguente elenca le funzioni di test di IRIS GL Alpha disponibili e le relative funzioni OpenGL equivalenti.
ms.assetid: cd4082fe-2fd6-43d8-a9a7-37fd448c084b
keywords:
- Porting di IRIS GL, funzioni di test AFunction
- porting da IRIS GL, funzioni di test AFunction
- porting in OpenGL da IRIS GL, funzioni di test di AFunction
- Porting OpenGL da IRIS GL, funzioni di test AFunction
- funzioni di test di AFunction
- funzioni di test Alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abfd3ba46d99f8b70ecfb97c0160efea944ccd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856881"
---
# <a name="porting-afunction-test-functions"></a><span data-ttu-id="ccc30-109">Porting di funzioni di test AFunction</span><span class="sxs-lookup"><span data-stu-id="ccc30-109">Porting afunction Test Functions</span></span>

<span data-ttu-id="ccc30-110">La tabella seguente elenca le funzioni di test di IRIS GL Alpha disponibili e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="ccc30-110">The following table lists the available IRIS GL alpha test functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ccc30-111">afunction</span><span class="sxs-lookup"><span data-stu-id="ccc30-111">afunction</span></span>    | <span data-ttu-id="ccc30-112">glAlphaFunc</span><span class="sxs-lookup"><span data-stu-id="ccc30-112">glAlphaFunc</span></span>  |
|--------------|--------------|
| <span data-ttu-id="ccc30-113">\_NOTEQUAL AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-113">AF\_NOTEQUAL</span></span> | <span data-ttu-id="ccc30-114">\_NOTEQUAL GL</span><span class="sxs-lookup"><span data-stu-id="ccc30-114">GL\_NOTEQUAL</span></span> |
| <span data-ttu-id="ccc30-115">\_sempre AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-115">AF\_ALWAYS</span></span>   | <span data-ttu-id="ccc30-116">GL \_ Always</span><span class="sxs-lookup"><span data-stu-id="ccc30-116">GL\_ALWAYS</span></span>   |
| <span data-ttu-id="ccc30-117">\_mai AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-117">AF\_NEVER</span></span>    | <span data-ttu-id="ccc30-118">GL \_ mai</span><span class="sxs-lookup"><span data-stu-id="ccc30-118">GL\_NEVER</span></span>    |
| <span data-ttu-id="ccc30-119">\_meno AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-119">AF\_LESS</span></span>     | <span data-ttu-id="ccc30-120">\_meno GL</span><span class="sxs-lookup"><span data-stu-id="ccc30-120">GL\_LESS</span></span>     |
| <span data-ttu-id="ccc30-121">uguale a AF \_</span><span class="sxs-lookup"><span data-stu-id="ccc30-121">AF\_EQUAL</span></span>    | <span data-ttu-id="ccc30-122">GL \_ uguale</span><span class="sxs-lookup"><span data-stu-id="ccc30-122">GL\_EQUAL</span></span>    |
| <span data-ttu-id="ccc30-123">\_LEQUAL AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-123">AF\_LEQUAL</span></span>   | <span data-ttu-id="ccc30-124">\_LEQUAL GL</span><span class="sxs-lookup"><span data-stu-id="ccc30-124">GL\_LEQUAL</span></span>   |
| <span data-ttu-id="ccc30-125">\_maggiore AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-125">AF\_GREATER</span></span>  | <span data-ttu-id="ccc30-126">maggiore di GL \_</span><span class="sxs-lookup"><span data-stu-id="ccc30-126">GL\_GREATER</span></span>  |
| <span data-ttu-id="ccc30-127">\_GEQUAL AF</span><span class="sxs-lookup"><span data-stu-id="ccc30-127">AF\_GEQUAL</span></span>   | <span data-ttu-id="ccc30-128">\_GEQUAL GL</span><span class="sxs-lookup"><span data-stu-id="ccc30-128">GL\_GEQUAL</span></span>   |



 

 

 




