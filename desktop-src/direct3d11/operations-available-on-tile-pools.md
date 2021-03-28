---
title: Operazioni disponibili nei pool di riquadri
description: Questa sezione elenca le operazioni che è possibile eseguire nei pool di sezioni.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223923"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="a5123-103">Operazioni disponibili nei pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="a5123-103">Operations available on tile pools</span></span>

<span data-ttu-id="a5123-104">Questa sezione elenca le operazioni che è possibile eseguire nei pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="a5123-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="a5123-105">La durata dei pool di riquadri funziona come qualsiasi altra risorsa Direct3D, supportata dal conteggio dei riferimenti, anche in questo caso il rilevamento dei mapping dalle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="a5123-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="a5123-106">Quando l'applicazione non fa più riferimento a un pool di sezioni e i mapping dei riquadri alla memoria sono finiti e gli accessi di unità di elaborazione grafica (GPU) sono stati completati, il sistema operativo dealloca il pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="a5123-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="a5123-107">Le API correlate alla condivisione di superficie e alla sincronizzazione funzionano per i pool di sezioni (ma non direttamente sulle risorse affiancate).</span><span class="sxs-lookup"><span data-stu-id="a5123-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="a5123-108">Analogamente al comportamento per i pool di sezioni offerti, i comandi Direct3D che accedono a risorse affiancate che puntano a un pool di sezioni vengono eliminati se il pool di sezioni è stato condiviso e attualmente acquisito da un altro dispositivo e processo.</span><span class="sxs-lookup"><span data-stu-id="a5123-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="a5123-109">Operazione [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)</span><span class="sxs-lookup"><span data-stu-id="a5123-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="a5123-110">Operazioni [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) : queste API per restituire temporaneamente memoria al sistema operano sull'intero pool di sezioni (e non sono disponibili per le singole risorse affiancate).</span><span class="sxs-lookup"><span data-stu-id="a5123-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="a5123-111">Se una risorsa affiancata punta a un riquadro in un pool di sezioni offerto, la risorsa affiancata si comporta come se venisse offerta. ad esempio, il runtime elimina i comandi che vi fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="a5123-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="a5123-112">I dati non possono essere copiati direttamente da e verso la memoria del pool di riquadri.</span><span class="sxs-lookup"><span data-stu-id="a5123-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="a5123-113">Gli accessi alla memoria vengono sempre eseguiti tramite risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="a5123-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5123-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5123-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5123-115">Creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="a5123-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 