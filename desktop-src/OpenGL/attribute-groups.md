---
title: Gruppi di attributi
description: Gruppi di attributi
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL, gruppi di attributi
- Riferimento OpenGL, gruppi di attributi
- informazioni di riferimento per OpenGL, gruppi di attributi
- gruppi di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298186"
---
# <a name="attribute-groups"></a><span data-ttu-id="77042-107">Gruppi di attributi</span><span class="sxs-lookup"><span data-stu-id="77042-107">Attribute Groups</span></span>



| <span data-ttu-id="77042-108">Bit maschera</span><span class="sxs-lookup"><span data-stu-id="77042-108">Mask bit</span></span>                  | <span data-ttu-id="77042-109">Gruppo di attributi</span><span class="sxs-lookup"><span data-stu-id="77042-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="77042-110">\_bit del buffer di accut GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="77042-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="77042-111">accut-buffer</span><span class="sxs-lookup"><span data-stu-id="77042-111">accum-buffer</span></span>    |
| <span data-ttu-id="77042-112">\_tutti i \_ \_ bit attrib (GL)</span><span class="sxs-lookup"><span data-stu-id="77042-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="77042-113">\_bit del \_ buffer dei colori GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="77042-114">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="77042-114">color-buffer</span></span>    |
| <span data-ttu-id="77042-115">\_bit corrente \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="77042-116">corrente</span><span class="sxs-lookup"><span data-stu-id="77042-116">current</span></span>         |
| <span data-ttu-id="77042-117">\_ \_ bit buffer di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="77042-118">buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="77042-118">depth-buffer</span></span>    |
| <span data-ttu-id="77042-119">\_bit di abilitazione GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="77042-120">abilitare</span><span class="sxs-lookup"><span data-stu-id="77042-120">enable</span></span>          |
| <span data-ttu-id="77042-121">BIT valutazione GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="77042-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="77042-122">eval</span><span class="sxs-lookup"><span data-stu-id="77042-122">eval</span></span>            |
| <span data-ttu-id="77042-123">\_bit di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="77042-124">nebbia</span><span class="sxs-lookup"><span data-stu-id="77042-124">fog</span></span>             |
| <span data-ttu-id="77042-125">\_bit suggerimento \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="77042-126">hint</span><span class="sxs-lookup"><span data-stu-id="77042-126">hint</span></span>            |
| <span data-ttu-id="77042-127">\_bit di illuminazione GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="77042-128">illuminazione</span><span class="sxs-lookup"><span data-stu-id="77042-128">lighting</span></span>        |
| <span data-ttu-id="77042-129">\_bit linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="77042-130">line</span><span class="sxs-lookup"><span data-stu-id="77042-130">line</span></span>            |
| <span data-ttu-id="77042-131">\_bit elenco \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="77042-132">list</span><span class="sxs-lookup"><span data-stu-id="77042-132">list</span></span>            |
| <span data-ttu-id="77042-133">\_bit in \_ modalità GL pixel \_</span><span class="sxs-lookup"><span data-stu-id="77042-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="77042-134">pixel</span><span class="sxs-lookup"><span data-stu-id="77042-134">pixel</span></span>           |
| <span data-ttu-id="77042-135">\_bit punto \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="77042-136">point</span><span class="sxs-lookup"><span data-stu-id="77042-136">point</span></span>           |
| <span data-ttu-id="77042-137">\_bit poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="77042-138">polygon</span><span class="sxs-lookup"><span data-stu-id="77042-138">polygon</span></span>         |
| <span data-ttu-id="77042-139">\_bit stipple poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="77042-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="77042-140">poligono-stipple</span><span class="sxs-lookup"><span data-stu-id="77042-140">polygon-stipple</span></span> |
| <span data-ttu-id="77042-141">\_bit a forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="77042-142">ritaglio</span><span class="sxs-lookup"><span data-stu-id="77042-142">scissor</span></span>         |
| <span data-ttu-id="77042-143">\_ \_ bit buffer dello stencil GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="77042-144">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="77042-144">stencil-buffer</span></span>  |
| <span data-ttu-id="77042-145">\_bit trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="77042-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="77042-146">trama</span><span class="sxs-lookup"><span data-stu-id="77042-146">texture</span></span>         |
| <span data-ttu-id="77042-147">\_bit di trasformazione GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="77042-148">trasformazione</span><span class="sxs-lookup"><span data-stu-id="77042-148">transform</span></span>       |
| <span data-ttu-id="77042-149">\_bit del viewport GL \_</span><span class="sxs-lookup"><span data-stu-id="77042-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="77042-150">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="77042-150">viewport</span></span>        |



 

 

 




