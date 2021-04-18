---
description: Per fare in modo che un'applicazione esegua il rendering realistico di una scena 3D, è necessario tenere in considerazione l'effetto delle fonti di luce sull'aspetto della scena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mapping chiaro con trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304096"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="99803-103">Mapping chiaro con trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99803-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="99803-104">Per fare in modo che un'applicazione esegua il rendering realistico di una scena 3D, è necessario tenere in considerazione l'effetto delle fonti di luce sull'aspetto della scena.</span><span class="sxs-lookup"><span data-stu-id="99803-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="99803-105">Sebbene le tecniche, ad esempio l'ombreggiatura flat e Gouraud, siano strumenti preziosi in questo senso, possono essere insufficienti per le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="99803-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="99803-106">Direct3D supporta il Multipass e la combinazione di più trame.</span><span class="sxs-lookup"><span data-stu-id="99803-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="99803-107">Queste funzionalità consentono all'applicazione di eseguire il rendering di scene con un aspetto più realistico rispetto alle scene sottoposte a rendering solo con tecniche di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="99803-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="99803-108">Applicando una o più mappe chiare, l'applicazione può mappare le aree di luce e ombreggiatura alle relative primitive.</span><span class="sxs-lookup"><span data-stu-id="99803-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="99803-109">Una mappa leggera è una trama o un gruppo di trame che contiene informazioni sull'illuminazione in una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="99803-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="99803-110">È possibile archiviare le informazioni sull'illuminazione nei valori alfa della mappa chiara, nei valori dei colori o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="99803-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="99803-111">Se si implementa il mapping chiaro con la combinazione di trame MultiPASS, l'applicazione deve eseguire il rendering della mappa chiara sulle primitive al primo passaggio.</span><span class="sxs-lookup"><span data-stu-id="99803-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="99803-112">Deve usare un secondo passaggio per eseguire il rendering della trama di base.</span><span class="sxs-lookup"><span data-stu-id="99803-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="99803-113">L'eccezione è rappresentata dal mapping chiaro speculare.</span><span class="sxs-lookup"><span data-stu-id="99803-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="99803-114">In tal caso, eseguire prima il rendering della trama di base; quindi aggiungere la mappa chiara.</span><span class="sxs-lookup"><span data-stu-id="99803-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="99803-115">La combinazione di più trame consente all'applicazione di eseguire il rendering della mappa chiara e della trama di base in un unico passaggio.</span><span class="sxs-lookup"><span data-stu-id="99803-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="99803-116">Se l'hardware dell'utente fornisce la combinazione di più trame, l'applicazione deve sfruttarla quando esegue il mapping chiaro.</span><span class="sxs-lookup"><span data-stu-id="99803-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="99803-117">Ciò migliora significativamente le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99803-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="99803-118">Con le mappe leggere, un'applicazione Direct3D può ottenere un'ampia gamma di effetti di illuminazione quando esegue il rendering delle primitive.</span><span class="sxs-lookup"><span data-stu-id="99803-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="99803-119">Consente di eseguire il mapping non solo di luci monocromatiche e colorate in una scena, ma anche di aggiungere dettagli come evidenziazioni speculari e illuminazione diffusa.</span><span class="sxs-lookup"><span data-stu-id="99803-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="99803-120">Per informazioni sull'uso della combinazione di trame Direct3D per eseguire il mapping chiaro, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="99803-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="99803-121">Mappe chiare monocromatiche (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99803-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="99803-122">Mappe per la luce del colore (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99803-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="99803-123">Mappe chiare speculari (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99803-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="99803-124">Mappe chiare diffuse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99803-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="99803-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99803-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99803-126">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="99803-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 



