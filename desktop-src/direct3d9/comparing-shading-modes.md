---
description: In modalità ombreggiatura piatta, la piramide seguente viene visualizzata con un bordo acuto tra i visi adiacenti. In modalità ombreggiatura Gouraud, tuttavia, i valori di ombreggiatura vengono interpolati sul bordo e l'aspetto finale è una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Confronto tra modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127778"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="2a69b-104">Confronto tra modalità di ombreggiatura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2a69b-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="2a69b-105">In modalità ombreggiatura piatta, la piramide seguente viene visualizzata con un bordo acuto tra i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="2a69b-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="2a69b-106">In modalità ombreggiatura Gouraud, tuttavia, i valori di ombreggiatura vengono interpolati sul bordo e l'aspetto finale è una superficie curva.</span><span class="sxs-lookup"><span data-stu-id="2a69b-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![illustrazione di una piramide con spigoli acuti e frecce che puntano alle normali del volto](images/shade2.png)

<span data-ttu-id="2a69b-108">Gouraud ombreggiatura illumina le superfici piane in maniera più realistica dell'ombreggiatura semplice.</span><span class="sxs-lookup"><span data-stu-id="2a69b-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="2a69b-109">Una faccia in modalità ombreggiatura piatta è un colore uniforme, ma l'ombreggiatura Gouraud consente di rientrare in modo più corretto in una faccia.</span><span class="sxs-lookup"><span data-stu-id="2a69b-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="2a69b-110">Questo effetto è particolarmente ovvio se è presente un'origine punto vicina.</span><span class="sxs-lookup"><span data-stu-id="2a69b-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="2a69b-111">L'ombreggiatura Gouraud smussa i bordi acuti tra i poligoni visibili con ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="2a69b-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="2a69b-112">Tuttavia, può produrre bande Mach, che sono bande di colore o luce che non sono mescolate in modo uniforme tra poligoni adiacenti.</span><span class="sxs-lookup"><span data-stu-id="2a69b-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="2a69b-113">L'applicazione può ridurre l'aspetto delle bande Mach aumentando il numero di poligoni in un oggetto, aumentando la risoluzione dello schermo o aumentando la profondità di colore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a69b-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="2a69b-114">L'ombreggiatura di Gouraud può non riuscire ad alcuni dettagli.</span><span class="sxs-lookup"><span data-stu-id="2a69b-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="2a69b-115">Nella figura seguente, ad esempio, un oggetto Spotlight è completamente contenuto all'interno di una superficie poligonale.</span><span class="sxs-lookup"><span data-stu-id="2a69b-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![illustrazione di un oggetto Spotlight in una superficie poligonale](images/gouraud.png)

<span data-ttu-id="2a69b-117">In questo caso, l'ombreggiatura Gouraud, che interpola tra i vertici, potrebbe non essere completamente in evidenza; viene eseguito il rendering della faccia come se il Spotlight non esistesse.</span><span class="sxs-lookup"><span data-stu-id="2a69b-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a69b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a69b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a69b-119">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="2a69b-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



