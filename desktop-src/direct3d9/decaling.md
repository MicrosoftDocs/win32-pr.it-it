---
description: Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering. Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Decaing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123876"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="cdcaa-104">Decaing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cdcaa-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="cdcaa-105">Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="cdcaa-106">Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="cdcaa-107">Ad esempio, quando si applicano segni di pneumatico e linee gialle a una carreggiata, i contrassegni devono essere visualizzati direttamente sopra la strada.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="cdcaa-108">Tuttavia, i valori z dei contrassegni e della strada sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="cdcaa-109">Il buffer di profondità potrebbe pertanto non produrre una netta separazione tra i due.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="cdcaa-110">È possibile che venga eseguito il rendering di alcuni pixel della primitiva in primo piano sulla primitiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="cdcaa-111">L'immagine risultante sembra riflessi da frame a frame.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="cdcaa-112">Questo effetto è detto *z-Fighting* o *flimmering*.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="cdcaa-113">Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva di sfondo in cui verrà visualizzata la decalcomania.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="cdcaa-114">Disattivare la memorizzazione nel buffer z ed eseguire il rendering dell'immagine della primitiva di primo piano nell'area nascosta della superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="cdcaa-115">Sebbene sia possibile usare la combinazione di più trame per risolvere questo problema, limitare il numero di altri effetti speciali che l'applicazione può produrre.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="cdcaa-116">L'utilizzo del buffer di stencil per applicare le decalcomanie consente di liberare le fasi di combinazione delle trame per altri effetti.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdcaa-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdcaa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdcaa-118">Tecniche del buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="cdcaa-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



