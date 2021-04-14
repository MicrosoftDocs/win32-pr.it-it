---
description: Per definire un rettangolo, un'applicazione deve usare una struttura RECT.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordinate rettangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993901"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="a2280-103">Coordinate rettangolo</span><span class="sxs-lookup"><span data-stu-id="a2280-103">Rectangle Coordinates</span></span>

<span data-ttu-id="a2280-104">Per definire un rettangolo, un'applicazione deve usare una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2280-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="a2280-105">La struttura specifica le coordinate di due punti: gli angoli superiore sinistro e inferiore destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="a2280-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="a2280-106">I lati del rettangolo si estendono da questi due punti e sono paralleli all'asse x e all'asse y.</span><span class="sxs-lookup"><span data-stu-id="a2280-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="a2280-107">I valori delle coordinate per un rettangolo sono espressi come interi con segno.</span><span class="sxs-lookup"><span data-stu-id="a2280-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="a2280-108">Il valore della coordinata del lato destro di un rettangolo deve essere maggiore di quello del lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="a2280-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="a2280-109">Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.</span><span class="sxs-lookup"><span data-stu-id="a2280-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="a2280-110">Poiché le applicazioni possono utilizzare rettangoli per molti scopi diversi, le funzioni Rectangle non utilizzano un'unità di misura esplicita.</span><span class="sxs-lookup"><span data-stu-id="a2280-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="a2280-111">Al contrario, tutte le coordinate e le dimensioni del rettangolo vengono specificate nei valori logici firmati.</span><span class="sxs-lookup"><span data-stu-id="a2280-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="a2280-112">La modalità di mapping e la funzione in cui viene utilizzato il rettangolo determinano le unità di misura.</span><span class="sxs-lookup"><span data-stu-id="a2280-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="a2280-113">Per ulteriori informazioni sulle coordinate e sulle modalità di mapping, vedere [Coordinate spaces and Transformations](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="a2280-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
