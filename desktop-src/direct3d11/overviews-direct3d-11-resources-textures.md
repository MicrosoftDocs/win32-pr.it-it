---
title: Trame
description: Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221746"
---
# <a name="textures"></a><span data-ttu-id="79d21-103">Trame</span><span class="sxs-lookup"><span data-stu-id="79d21-103">Textures</span></span>

<span data-ttu-id="79d21-104">Una trama archivia le informazioni di Texel.</span><span class="sxs-lookup"><span data-stu-id="79d21-104">A texture stores texel information.</span></span> <span data-ttu-id="79d21-105">Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.</span><span class="sxs-lookup"><span data-stu-id="79d21-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79d21-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="79d21-106">In this section</span></span>



| <span data-ttu-id="79d21-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="79d21-107">Topic</span></span>                                                                                                    | <span data-ttu-id="79d21-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79d21-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79d21-109">Introduzione alle trame in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="79d21-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="79d21-110">Una risorsa di trama è una raccolta strutturata di dati progettati per archiviare Texel.</span><span class="sxs-lookup"><span data-stu-id="79d21-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="79d21-111">Un Texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="79d21-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="79d21-112">A differenza dei buffer, le trame possono essere filtrate in base ai Sampler di trama Man mano che vengono lette dalle unità dello shader.</span><span class="sxs-lookup"><span data-stu-id="79d21-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="79d21-113">Il tipo di trama influisca sul modo in cui la trama viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="79d21-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="79d21-114">Ogni Texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI definiti dall'enumerazione del \_ formato dxgi.</span><span class="sxs-lookup"><span data-stu-id="79d21-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="79d21-115">Compressione dei blocchi di trama in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="79d21-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="79d21-116">Il supporto per la compressione dei blocchi (BC) per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7.</span><span class="sxs-lookup"><span data-stu-id="79d21-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="79d21-117">BC6H supporta i dati di origine dei colori con intervallo dinamico elevato e BC7 offre una compressione di qualità migliore rispetto alla media con meno elementi per i dati di origine RGB standard.</span><span class="sxs-lookup"><span data-stu-id="79d21-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="79d21-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79d21-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d21-119">Procedura: creare una trama</span><span class="sxs-lookup"><span data-stu-id="79d21-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="79d21-120">Procedura: inizializzare una trama a livello di codice</span><span class="sxs-lookup"><span data-stu-id="79d21-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="79d21-121">Procedura: inizializzare una trama da un file</span><span class="sxs-lookup"><span data-stu-id="79d21-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="79d21-122">Risorse</span><span class="sxs-lookup"><span data-stu-id="79d21-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





