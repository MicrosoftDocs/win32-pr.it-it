---
description: Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema. Le superfici vengono gestite dall'interfaccia IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superfici Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745399"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="85171-104">Superfici Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="85171-105">Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="85171-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="85171-106">Le superfici vengono gestite dall'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="85171-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="85171-107">Buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="85171-107">Front Buffer.</span></span> <span data-ttu-id="85171-108">Un rettangolo di memoria convertito dalla scheda grafica e visualizzato sul monitor.</span><span class="sxs-lookup"><span data-stu-id="85171-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="85171-109">In Direct3D un'applicazione non scrive mai direttamente nel buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="85171-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="85171-110">Buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="85171-110">Back Buffer.</span></span> <span data-ttu-id="85171-111">Un rettangolo di memoria in cui un'applicazione può scrivere direttamente.</span><span class="sxs-lookup"><span data-stu-id="85171-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="85171-112">Il buffer nascosto non viene mai visualizzato direttamente sul monitor.</span><span class="sxs-lookup"><span data-stu-id="85171-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="85171-113">Capovolgimento di superfici.</span><span class="sxs-lookup"><span data-stu-id="85171-113">Flipping surfaces.</span></span> <span data-ttu-id="85171-114">Processo di trasferimento del buffer nascosto nel buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="85171-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="85171-115">Catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="85171-115">Swap chain.</span></span> <span data-ttu-id="85171-116">Raccolta di uno o più buffer back che possono essere presentati in modo seriale al buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="85171-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="85171-117">Recupero di una superficie</span><span class="sxs-lookup"><span data-stu-id="85171-117">Getting a Surface</span></span>

<span data-ttu-id="85171-118">Creare una superficie chiamando uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="85171-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="85171-119">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="85171-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="85171-120">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="85171-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="85171-121">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="85171-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="85171-122">I formati di superficie determinano come vengono interpretati i dati per ogni pixel nella memoria di superficie.</span><span class="sxs-lookup"><span data-stu-id="85171-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="85171-123">Direct3D usa il membro [D3DFORMAT](d3dformat.md) della struttura [**D3DSURFACE \_ desc**](d3dsurface-desc.md) per descrivere il formato della superficie.</span><span class="sxs-lookup"><span data-stu-id="85171-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="85171-124">È possibile recuperare il formato di una superficie esistente chiamando il metodo [**getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .</span><span class="sxs-lookup"><span data-stu-id="85171-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="85171-125">Una volta creata una superficie, è possibile ottenere un puntatore chiamando uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="85171-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="85171-126">**GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="85171-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="85171-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="85171-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="85171-128">**GetDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="85171-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="85171-129">**GetFrontBufferData**</span><span class="sxs-lookup"><span data-stu-id="85171-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="85171-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="85171-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="85171-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="85171-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="85171-132">**GetSurfaceLevel**</span><span class="sxs-lookup"><span data-stu-id="85171-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="85171-133">L'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) consente di accedere indirettamente alla memoria tramite il metodo [**UpdateSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="85171-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="85171-134">Questo metodo consente di copiare un'area rettangolare di pixel da un'interfaccia **IDirect3DSurface9** a un'altra interfaccia **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="85171-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="85171-135">L'interfaccia Surface dispone inoltre di metodi per accedere direttamente alla memoria di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="85171-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="85171-136">Ad esempio, è possibile usare il metodo [**LockRect**](/windows/desktop/api) per bloccare un'area rettangolare della memoria di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="85171-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="85171-137">È importante chiamare [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) dopo aver terminato di utilizzare l'area rettangolare bloccata sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="85171-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="85171-138">Argomenti aggiuntivi sull'area</span><span class="sxs-lookup"><span data-stu-id="85171-138">Additional Surface Topics</span></span>

<span data-ttu-id="85171-139">Scopri di più su come usare le superfici con uno di questi argomenti:</span><span class="sxs-lookup"><span data-stu-id="85171-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="85171-140">Formati di superficie (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="85171-141">Che cos'è una catena di scambio? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="85171-142">Spessore rispetto a pitch (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="85171-143">Capovolgimento di superfici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="85171-144">Capovolgimento della pagina e buffering indietro (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="85171-145">Copia in superfici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="85171-146">Copia di superfici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="85171-147">Accesso diretto alla memoria di Surface (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="85171-148">Dati della superficie privata (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="85171-149">Controlli gamma (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85171-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="85171-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85171-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85171-151">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="85171-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
