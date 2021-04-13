---
description: L'applicazione modifica le risorse per eseguire il rendering di una scena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipolazione di risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401041"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="ce6bc-103">Manipolazione di risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ce6bc-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="ce6bc-104">L'applicazione modifica le risorse per eseguire il rendering di una scena.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="ce6bc-105">Per prima cosa, un'applicazione deve creare una risorsa di trama con uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce6bc-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="ce6bc-106">**IDirect3DDevice9:: CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="ce6bc-107">**IDirect3DDevice9:: CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="ce6bc-108">**IDirect3DDevice9:: CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="ce6bc-109">È invece possibile creare una risorsa di trama con una delle funzioni di texturing di D3DXCreatexxx.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="ce6bc-110">Gli oggetti trama restituiti dai metodi di creazione della trama sono contenitori per superfici o volumi; questi contenitori sono noti in modo generico come buffer.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="ce6bc-111">I buffer di proprietà della risorsa ereditano gli utilizzi, il formato e il pool della risorsa, ma hanno un proprio tipo.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="ce6bc-112">Per altre informazioni, vedere [proprietà delle risorse (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="ce6bc-113">L'applicazione ottiene l'accesso alle superfici contenute, allo scopo di caricare le illustrazioni, chiamando i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="ce6bc-114">Per informazioni dettagliate, vedere [blocco di risorse (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="ce6bc-115">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="ce6bc-116">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="ce6bc-117">**IDirect3DVolumeTexture9:: archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="ce6bc-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="ce6bc-118">I metodi di blocco accettano argomenti che indicano la superficie contenuta, ad esempio il sottolivello o il lato del cubo mipmap della trama, e restituiscono puntatori ai pixel.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="ce6bc-119">L'applicazione tipica non utilizza mai direttamente un oggetto Surface.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="ce6bc-120">Creare risorse orientate alla geometria chiamando [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/desktop/api) o [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="ce6bc-121">Bloccare e riempire le risorse del buffer chiamando [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) o [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), a seconda della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="ce6bc-122">Per le risorse di trama gestite, il processo di creazione delle risorse termina qui.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="ce6bc-123">Per le risorse di trama non gestite, un'applicazione promuove le risorse di memoria di sistema a risorse accessibili dal dispositivo (per l'accelerazione hardware) chiamando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="ce6bc-124">Per presentare le immagini sottoposte a rendering dalle risorse, l'applicazione necessita anche di buffer di colore e di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="ce6bc-125">Per le applicazioni tipiche, il buffer dei colori appartiene alla catena di scambio del dispositivo, che è una raccolta di superfici di back-buffer e viene creata in modo implicito con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce6bc-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="ce6bc-126">Le superfici dello stencil Depth possono essere create in modo implicito o create in modo esplicito tramite il metodo [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ce6bc-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ce6bc-127">L'applicazione associa un dispositivo e il relativo buffer di profondità e colore con una chiamata a [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) o [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="ce6bc-128">Per informazioni dettagliate sulla presentazione dell'immagine finale, vedere [presentazione di una scena (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="ce6bc-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce6bc-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce6bc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce6bc-130">Risorse Direct3D</span><span class="sxs-lookup"><span data-stu-id="ce6bc-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
