---
title: Compressione di mipmap
description: A seconda del livello di supporto per le risorse affiancate, mipmap con determinate dimensioni non seguono le forme standard del riquadro e sono considerate tutte raggruppate tra loro in modo che sia opaco per l'applicazione.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044424"
---
# <a name="mipmap-packing"></a><span data-ttu-id="a0d65-103">Compressione di mipmap</span><span class="sxs-lookup"><span data-stu-id="a0d65-103">Mipmap packing</span></span>

<span data-ttu-id="a0d65-104">A seconda del [livello](tiled-resources-features-tiers.md) di supporto per le risorse affiancate, mipmap con determinate dimensioni non seguono le forme standard del riquadro e sono considerate tutte raggruppate tra loro in modo che sia opaco per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0d65-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="a0d65-105">I livelli di supporto più elevati hanno garanzie più ampie sui tipi di dimensioni di superficie che si adattano alle forme di sezione standard (e possono quindi essere mappati singolarmente dalle applicazioni).</span><span class="sxs-lookup"><span data-stu-id="a0d65-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="a0d65-106">Ciò che può variare tra le implementazioni è che, date le dimensioni, il formato, il numero di mipmap e le sezioni di matrice di una risorsa affiancata, un numero di milioni di MIPS (per ogni sezione della matrice) può essere compresso in un numero N di riquadri.</span><span class="sxs-lookup"><span data-stu-id="a0d65-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="a0d65-107">L'API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) esiste per consentire al driver di segnalare all'applicazione quali M e N sono, tra gli altri dettagli relativi alla superficie segnalata dall'API, che sono standard e non variano in base al fornitore dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a0d65-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="a0d65-108">Il set di riquadri per i MIP compressi è ancora 64KB e può essere mappato singolarmente in posizioni diverse in un pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="a0d65-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="a0d65-109">Tuttavia, la forma pixel dei riquadri e il modo in cui mipmap si adattano al set di riquadri sono specifici di un fornitore di hardware ed è troppo complesso da esporre.</span><span class="sxs-lookup"><span data-stu-id="a0d65-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="a0d65-110">In questo modo, le applicazioni devono eseguire il mapping di tutti i riquadri designati come compressi o nessuno per volta.</span><span class="sxs-lookup"><span data-stu-id="a0d65-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="a0d65-111">In caso contrario, il comportamento per l'accesso alla risorsa affiancata non è definito.</span><span class="sxs-lookup"><span data-stu-id="a0d65-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="a0d65-112">Per le superfici con matrici, il set di MIPS compresso e il numero di riquadri compressi che archiviano tali MIPS (M e N descritti in precedenza) si applica singolarmente per ogni sezione della matrice.</span><span class="sxs-lookup"><span data-stu-id="a0d65-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="a0d65-113">Le API dedicate per la copia dei riquadri ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) non possono accedere a MIPS compressi.</span><span class="sxs-lookup"><span data-stu-id="a0d65-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="a0d65-114">Le applicazioni che vogliono copiare i dati da e verso i pacchetti MIPS possono eseguire questa operazione usando tutte le API specifiche delle risorse non affiancate per la copia e il rendering nelle superfici.</span><span class="sxs-lookup"><span data-stu-id="a0d65-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0d65-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0d65-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d65-116">Come affiancare l'area di una risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="a0d65-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




