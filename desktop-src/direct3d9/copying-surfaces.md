---
description: Il termine blit è la sintassi abbreviata per &\# 0034; trasferimento di blocchi di bit &\# 0034, ovvero il processo di trasferimento di blocchi di dati da una posizione in memoria a un'altra.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copia di superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305110"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="185eb-103">Copia di superfici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="185eb-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="185eb-104">Il termine blit è la sintassi abbreviata per "bit Block Transfer", che è il processo di trasferimento di blocchi di dati da una posizione in memoria a un'altra.</span><span class="sxs-lookup"><span data-stu-id="185eb-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="185eb-105">L'interfaccia DDI (Device Driver Interface) blitting continua a essere usata in Direct3D 9 come meccanismo principale per lo spostando rettangoli di grandi dimensioni di pixel in base ai singoli fotogrammi, il meccanismo dietro il metodo [**IDirect3DDevice9::P**](/windows/desktop/api) reinviato.</span><span class="sxs-lookup"><span data-stu-id="185eb-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="185eb-106">Il trasporto di artwork nell'operazione blit viene eseguito dal metodo [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="185eb-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="185eb-107">Le immagini possono anche essere copiate in Direct3D 9 usando il metodo [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , che copia un subset rettangolare di pixel.</span><span class="sxs-lookup"><span data-stu-id="185eb-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="185eb-108">Direct3D 9 fornisce funzioni D3DX che consentono di caricare immagini da file, applicare la conversione dei colori e ridimensionare le immagini.</span><span class="sxs-lookup"><span data-stu-id="185eb-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="185eb-109">Per altre informazioni sulle funzioni disponibili, vedere [funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="185eb-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="185eb-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="185eb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="185eb-111">Superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="185eb-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="185eb-112">**IDirect3DDevice9:: StretchRect**</span><span class="sxs-lookup"><span data-stu-id="185eb-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="185eb-113">**IDirect3DDevice9:: StretchRect**</span><span class="sxs-lookup"><span data-stu-id="185eb-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
