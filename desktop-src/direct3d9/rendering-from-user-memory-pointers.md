---
description: Un set secondario di interfacce di rendering supporta il passaggio di dati vertex e index direttamente da puntatori di memoria utente. Queste interfacce supportano un solo flusso di dati dei vertici. Per ulteriori informazioni, vedere gli argomenti di riferimento seguenti.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Rendering da puntatori di memoria utente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225433"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a><span data-ttu-id="9f3c9-105">Rendering da puntatori di memoria utente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9f3c9-105">Rendering from User Memory Pointers (Direct3D 9)</span></span>

<span data-ttu-id="9f3c9-106">Un set secondario di interfacce di rendering supporta il passaggio di dati vertex e index direttamente da puntatori di memoria utente.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-106">A secondary set of rendering interfaces supports passing vertex and index data directly from user memory pointers.</span></span> <span data-ttu-id="9f3c9-107">Queste interfacce supportano un solo flusso di dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-107">These interfaces support a single stream of vertex data only.</span></span> <span data-ttu-id="9f3c9-108">Per ulteriori informazioni, vedere gli argomenti di riferimento seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-108">For more information, see the following reference topics.</span></span>

-   [<span data-ttu-id="9f3c9-109">**IDirect3DDevice9::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9f3c9-109">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [<span data-ttu-id="9f3c9-110">**IDirect3DDevice9::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9f3c9-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

<span data-ttu-id="9f3c9-111">Questi metodi eseguono il rendering con i dati specificati dai puntatori della memoria utente, anziché i buffer di Vertex e index.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-111">These methods render with data specified by user memory pointers, instead of vertex and index buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f3c9-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f3c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f3c9-113">Primitive di rendering</span><span class="sxs-lookup"><span data-stu-id="9f3c9-113">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
