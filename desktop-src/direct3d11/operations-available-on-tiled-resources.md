---
title: Operazioni disponibili sulle risorse affiancate
description: In questa sezione sono elencate le operazioni che è possibile eseguire sulle risorse affiancate.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045138"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="29fb5-103">Operazioni disponibili sulle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="29fb5-103">Operations available on tiled resources</span></span>

<span data-ttu-id="29fb5-104">In questa sezione sono elencate le operazioni che è possibile eseguire sulle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="29fb5-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="29fb5-105">void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations-questi punti del punto di operazioni in una risorsa affiancata alle posizioni nei pool di sezioni, o a null o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="29fb5-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="29fb5-106">Queste operazioni possono aggiornare un subset non contiguo dei puntatori a sezioni.</span><span class="sxs-lookup"><span data-stu-id="29fb5-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="29fb5-107">\*Operazioni Copy () e Update \* (): tutte le API in grado di copiare dati da e verso una superficie del pool predefinita (ad esempio, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) e [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funzionano per le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="29fb5-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="29fb5-108">La lettura da riquadri non mappati produce 0 e le scritture nei riquadri non mappati vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="29fb5-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="29fb5-109">Operazioni [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) : queste operazioni sono disponibili per copiare i riquadri con granularità 64KB da e verso qualsiasi risorsa affiancata e una risorsa buffer in un layout di memoria canonico.</span><span class="sxs-lookup"><span data-stu-id="29fb5-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="29fb5-110">Il driver di visualizzazione e l'hardware eseguono qualsiasi memoria "swizzling" necessaria per la risorsa affiancata.</span><span class="sxs-lookup"><span data-stu-id="29fb5-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="29fb5-111">Le associazioni della pipeline Direct3D e le creazioni/associazioni di visualizzazione che funzionano su risorse non affiancate funzionano anche con le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="29fb5-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="29fb5-112">I controlli riquadro sono disponibili in contesti immediati o posticipati (proprio come gli aggiornamenti alle risorse tipiche) e, al momento dell'esecuzione, gli accessi successivi ai riquadri (non le operazioni inviate in precedenza).</span><span class="sxs-lookup"><span data-stu-id="29fb5-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29fb5-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29fb5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29fb5-114">Creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="29fb5-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




