---
description: Elenca le funzioni del piano fornite da DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funzioni del piano della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309293"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="c2fc2-103">Funzioni del piano della libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c2fc2-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="c2fc2-104">Elenca le funzioni del piano fornite da DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="c2fc2-105">Queste funzioni usano un vettore XMVECTOR 4 per rappresentare i coefficienti dell'equazione del piano, ax + by + CZ + D = 0, dove il componente X è un, il componente Y è B, il componente Z è C e il componente W è D.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2fc2-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c2fc2-106">In this section</span></span>



| <span data-ttu-id="c2fc2-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="c2fc2-107">Topic</span></span>                                                               | <span data-ttu-id="c2fc2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2fc2-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2fc2-109">**XMPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="c2fc2-110">Calcola il prodotto punto tra un piano di input e un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="c2fc2-111">**XMPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="c2fc2-112">Calcola il prodotto punto tra un piano di input e un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="c2fc2-113">**XMPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="c2fc2-114">Calcola il prodotto punto tra il vettore normale di un piano e un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="c2fc2-115">**XMPlaneEqual**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="c2fc2-116">Determina se due piani sono uguali.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="c2fc2-117">**XMPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="c2fc2-118">Calcola l'equazione di un piano costruito da un punto nel piano e da un vettore normale.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="c2fc2-119">**XMPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="c2fc2-120">Calcola l'equazione di un piano costruito da tre punti del piano.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="c2fc2-121">**XMPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="c2fc2-122">Trova l'intersezione tra un piano e una linea.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="c2fc2-123">**XMPlaneIntersectPlane**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="c2fc2-124">Trova l'intersezione di due piani.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="c2fc2-125">**XMPlaneIsInfinite**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="c2fc2-126">Verifica se uno dei coefficienti di un piano è un valore infinito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="c2fc2-127">**XMPlaneIsNaN**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="c2fc2-128">Verifica se uno dei coefficienti di un piano è NaN.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="c2fc2-129">**XMPlaneNearEqual**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="c2fc2-130">Determina se due piani sono quasi uguali.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="c2fc2-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="c2fc2-132">Normalizza i coefficienti di un piano in modo che i coefficienti di x, y e z formino un vettore di unità normale.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="c2fc2-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="c2fc2-134">Stima i coefficienti di un piano in modo che i coefficienti di x, y e z formino un vettore di unità normale.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="c2fc2-135">**XMPlaneNotEqual**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="c2fc2-136">Determina se due piani sono diversi.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="c2fc2-137">**XMPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="c2fc2-138">Trasforma un piano in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="c2fc2-139">**XMPlaneTransformStream**</span><span class="sxs-lookup"><span data-stu-id="c2fc2-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="c2fc2-140">Trasforma un flusso di piani in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="c2fc2-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2fc2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2fc2-142">Funzioni della libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c2fc2-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
