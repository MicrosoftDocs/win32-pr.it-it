---
description: Informazioni sulla fusione alfa. La fusione alfa viene usata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262003"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="e97e8-104">Fusione alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="e97e8-105">La fusione alfa viene usata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.</span><span class="sxs-lookup"><span data-stu-id="e97e8-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="e97e8-106">Oltre a un canale di colori rosso, verde e blu, ogni pixel in una bitmap alfa ha un componente di trasparenza noto come canale alfa.</span><span class="sxs-lookup"><span data-stu-id="e97e8-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="e97e8-107">Il canale alfa contiene in genere tutti i bit di un canale di colore.</span><span class="sxs-lookup"><span data-stu-id="e97e8-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="e97e8-108">Ad esempio, un canale alfa a 8 bit può rappresentare 256 livelli di trasparenza, da 0 (l'intero pixel è trasparente) a 255 (l'intero pixel è opaco).</span><span class="sxs-lookup"><span data-stu-id="e97e8-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="e97e8-109">L'elenco seguente mostra alcuni effetti speciali che è possibile creare usando la fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="e97e8-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="e97e8-110">Il colore può essere definito con o senza valori alfa.</span><span class="sxs-lookup"><span data-stu-id="e97e8-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="e97e8-111">Il colore senza alfa è il colore RGB con alfa archiviato come ARGB.</span><span class="sxs-lookup"><span data-stu-id="e97e8-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="e97e8-112">I dati sui vertici, i dati sui materiali e i dati di trama possono essere usati per fornire la trasparenza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e97e8-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="e97e8-113">Il buffer dei frame può essere usato anche per generare effetti di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="e97e8-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="e97e8-114">Vertice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="e97e8-115">Alfa materiale (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="e97e8-116">Alfa trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="e97e8-117">Frame Buffer Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="e97e8-118">Eseguire il rendering del valore alfa di destinazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="e97e8-119">Gli esempi che illustrano i caratteri alfa includono:</span><span class="sxs-lookup"><span data-stu-id="e97e8-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="e97e8-120">Confronto (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="e97e8-121">Cloud, Smoke e Trails (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="e97e8-122">Incendio, flare ed esplosione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e97e8-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="e97e8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e97e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97e8-124">Direct3D Rendering</span><span class="sxs-lookup"><span data-stu-id="e97e8-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



