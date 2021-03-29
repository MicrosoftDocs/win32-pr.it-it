---
title: Creazione di pool di riquadri
description: Un pool di sezioni viene creato tramite l'API CreateBuffer di ID3D11Device passando il \_ flag del pool di varie sezioni della risorsa d3d11 \_ \_ \_ nel membro MiscFlags della \_ struttura di descrizione del buffer D3D11 \_ a cui punta il parametro pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992733"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="e91f0-103">Creazione di pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="e91f0-103">Tile pool creation</span></span>

<span data-ttu-id="e91f0-104">Un pool di sezioni viene creato tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando il flag del [**\_ \_ \_ \_ pool di sezioni varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) nel membro **MiscFlags** della struttura della [**\_ \_ Descrizione del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a cui punta il parametro *pDesc* .</span><span class="sxs-lookup"><span data-stu-id="e91f0-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="e91f0-105">Le applicazioni possono creare uno o più pool di riquadri per ogni dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e91f0-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="e91f0-106">La dimensione totale di ogni pool di sezioni è limitata al limite di dimensioni delle risorse di Direct3D 11, che è approssimativamente 1/4 di RAM di unità di elaborazione grafica (GPU).</span><span class="sxs-lookup"><span data-stu-id="e91f0-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="e91f0-107">Un pool di sezioni è costituito da riquadri 64KB, ma il sistema operativo (driver di visualizzazione) gestisce l'intero pool come una o più allocazioni dietro le quinte: la suddivisione non è visibile per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e91f0-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="e91f0-108">Le risorse affiancate definiscono il contenuto posizionando i riquadri all'interno di un pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="e91f0-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="e91f0-109">L'annullamento del mapping di un riquadro da una risorsa affiancata viene eseguito puntando il riquadro a **null**.</span><span class="sxs-lookup"><span data-stu-id="e91f0-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="e91f0-110">Tali riquadri non mappati hanno regole sul comportamento di letture o Scritture.</span><span class="sxs-lookup"><span data-stu-id="e91f0-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="e91f0-111">Per informazioni, vedere [Hazard Tracking versus Tile Pool Resources](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="e91f0-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e91f0-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e91f0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e91f0-113">Mapping inclusi in un pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="e91f0-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




