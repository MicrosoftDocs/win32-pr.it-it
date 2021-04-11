---
description: La fusione alfa viene utilizzata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127239"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="204f1-103">Fusione alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="204f1-104">La fusione alfa viene utilizzata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.</span><span class="sxs-lookup"><span data-stu-id="204f1-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="204f1-105">Oltre a un canale di colore rosso, verde e blu, ogni pixel in una bitmap alfa presenta un componente di trasparenza noto come canale alfa.</span><span class="sxs-lookup"><span data-stu-id="204f1-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="204f1-106">Il canale alfa contiene in genere tutti i bit di un canale colori.</span><span class="sxs-lookup"><span data-stu-id="204f1-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="204f1-107">Un canale alfa a 8 bit, ad esempio, può rappresentare 256 livelli di trasparenza, da 0 (l'intero pixel è trasparente) a 255 (l'intero pixel è opaco).</span><span class="sxs-lookup"><span data-stu-id="204f1-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="204f1-108">L'elenco seguente illustra alcuni effetti speciali che è possibile creare usando la fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="204f1-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="204f1-109">Il colore può essere definito con o senza valori alfa.</span><span class="sxs-lookup"><span data-stu-id="204f1-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="204f1-110">Il colore senza alfa è il colore RGB con alfa viene archiviato come ARGB.</span><span class="sxs-lookup"><span data-stu-id="204f1-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="204f1-111">I dati dei vertici, i dati del materiale e i dati di trama possono essere utilizzati per garantire la trasparenza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="204f1-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="204f1-112">Il buffer del frame può essere usato anche per generare effetti di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="204f1-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="204f1-113">Alfa vertice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="204f1-114">Materiale Alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="204f1-115">Trama alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="204f1-116">Buffer frame alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="204f1-117">Alfa destinazione rendering (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="204f1-118">Gli esempi che dimostrano Alpha includono:</span><span class="sxs-lookup"><span data-stu-id="204f1-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="204f1-119">Billboard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="204f1-120">Percorsi cloud, fumo e Vapor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="204f1-121">Incendi, flare ed esplosioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="204f1-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="204f1-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="204f1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="204f1-123">Rendering Direct3D</span><span class="sxs-lookup"><span data-stu-id="204f1-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



