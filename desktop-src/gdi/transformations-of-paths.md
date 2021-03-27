---
description: I percorsi vengono definiti usando le unità logiche e le trasformazioni correnti.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Trasformazioni di percorsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980295"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="5b1ec-103">Trasformazioni di percorsi</span><span class="sxs-lookup"><span data-stu-id="5b1ec-103">Transformations of Paths</span></span>

<span data-ttu-id="5b1ec-104">I percorsi vengono definiti usando le unità logiche e le trasformazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="5b1ec-105">Se è stata chiamata la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , le unità logiche sono unità internazionali. in caso contrario, le unità logiche sono unità di pagina. Un'applicazione può usare le trasformazioni globali per ridimensionare, ruotare, tagliare, tradurre e riflettere le linee e le curve di Bézier che definiscono un percorso.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="5b1ec-106">Una trasformazione globale all'interno di una parentesi del percorso influiscono solo sulle linee e sulle curve disegnate dopo l'impostazione della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="5b1ec-107">Non avrà alcun effetto su tali linee e curve disegnate prima di essere impostate.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="5b1ec-108">Per una descrizione della trasformazione globale, vedere [spazi di coordinate e trasformazioni](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="5b1ec-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="5b1ec-109">Un'applicazione può anche usare [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per delineare la forma della penna usata per delineare un percorso se la penna è una penna geometrica.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="5b1ec-110">Per una descrizione delle penne geometriche, vedere [penne](pens.md).</span><span class="sxs-lookup"><span data-stu-id="5b1ec-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



