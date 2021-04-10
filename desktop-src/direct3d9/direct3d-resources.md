---
description: Le risorse sono le trame e i buffer usati per eseguire il rendering di una scena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Risorse Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124497"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="db9b7-103">Risorse Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="db9b7-104">Le risorse sono le trame e i buffer usati per eseguire il rendering di una scena.</span><span class="sxs-lookup"><span data-stu-id="db9b7-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="db9b7-105">Le applicazioni devono creare, caricare, copiare e usare le risorse.</span><span class="sxs-lookup"><span data-stu-id="db9b7-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="db9b7-106">Questa sezione fornisce una breve introduzione alle risorse e ai passaggi e ai metodi usati dalle applicazioni per l'uso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="db9b7-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="db9b7-107">Tutte le risorse, incluse le risorse Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) e [**IDirect3DVertexBuffer9**](/windows/desktop/api), ereditano dall'interfaccia [**IDirect3DResource9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="db9b7-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="db9b7-108">Le risorse di trama, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9**](/windows/desktop/api), ereditano anche dall'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .</span><span class="sxs-lookup"><span data-stu-id="db9b7-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="db9b7-109">Proprietà delle risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="db9b7-110">Manipolazione di risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="db9b7-111">Blocco di risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="db9b7-112">Relazioni tra risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="db9b7-113">Gestione delle risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="db9b7-114">Risorse gestite dall'applicazione e strategie di allocazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="db9b7-115">Buffer di indice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="db9b7-116">Buffer vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db9b7-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="db9b7-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db9b7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db9b7-118">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="db9b7-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
