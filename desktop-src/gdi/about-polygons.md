---
description: Un poligono è una forma riempita con lati dritti.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informazioni sui poligoni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049737"
---
# <a name="about-polygons"></a><span data-ttu-id="0318f-103">Informazioni sui poligoni</span><span class="sxs-lookup"><span data-stu-id="0318f-103">About Polygons</span></span>

<span data-ttu-id="0318f-104">Un *poligono* è una forma riempita con lati dritti.</span><span class="sxs-lookup"><span data-stu-id="0318f-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="0318f-105">I lati di un poligono vengono disegnati usando la penna corrente.</span><span class="sxs-lookup"><span data-stu-id="0318f-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="0318f-106">Quando il sistema compila un poligono, usa il pennello corrente e la modalità di riempimento del poligono corrente.</span><span class="sxs-lookup"><span data-stu-id="0318f-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="0318f-107">Le due modalità di riempimento, alternative (impostazione predefinita) e Winding, determinano se le aree all'interno di un poligono complesso vengono riempite o lasciate non verniciate.</span><span class="sxs-lookup"><span data-stu-id="0318f-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="0318f-108">Un'applicazione può selezionare una delle due modalità chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="0318f-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="0318f-109">Per ulteriori informazioni sulle modalità di riempimento poligono, vedere [Regions](regions.md).</span><span class="sxs-lookup"><span data-stu-id="0318f-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="0318f-110">La figura seguente mostra un poligono disegnato usando [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span><span class="sxs-lookup"><span data-stu-id="0318f-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![illustrazione di un poligono nella forma di una stella a cinque punte](images/csfsh-04.png)

<span data-ttu-id="0318f-112">Oltre a disegnare un singolo poligono usando [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), un'applicazione può disegnare più poligoni usando la funzione [**polipolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .</span><span class="sxs-lookup"><span data-stu-id="0318f-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
