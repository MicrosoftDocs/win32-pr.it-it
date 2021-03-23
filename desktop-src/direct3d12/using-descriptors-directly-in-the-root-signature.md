---
title: Uso dei descrittori direttamente nella firma radice
description: Le applicazioni possono inserire descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap del descrittore.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548886"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="b7a14-103">Uso dei descrittori direttamente nella firma radice</span><span class="sxs-lookup"><span data-stu-id="b7a14-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="b7a14-104">Le applicazioni possono inserire descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="b7a14-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="b7a14-105">Questi descrittori hanno una grande quantità di spazio nella firma radice (vedere la sezione limiti della firma radice), per cui le applicazioni devono utilizzarle sporadicamente.</span><span class="sxs-lookup"><span data-stu-id="b7a14-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="b7a14-106">Un esempio di utilizzo è quello di inserire una visualizzazione del buffer costante (CBV) che sta cambiando per disegno nel layout radice in modo che lo spazio dell'heap di descrittore non debba essere allocato dall'applicazione per ogni disegno (e salvare puntando una tabella di descrittori nella nuova posizione nell'heap del descrittore).</span><span class="sxs-lookup"><span data-stu-id="b7a14-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="b7a14-107">Inserendo qualcosa nella firma radice, l'applicazione passa semplicemente la responsabilità del controllo delle versioni al driver, ma si tratta di un'infrastruttura già disponibile.</span><span class="sxs-lookup"><span data-stu-id="b7a14-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="b7a14-108">Per il rendering che utilizza un numero molto ridotto di risorse, l'utilizzo della tabella o dell'heap del descrittore potrebbe non essere necessario se tutti i descrittori necessari possono essere inseriti direttamente nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="b7a14-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="b7a14-109">Gli unici tipi di descrittori supportati nella firma radice sono:</span><span class="sxs-lookup"><span data-stu-id="b7a14-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="b7a14-110">CBVs.</span><span class="sxs-lookup"><span data-stu-id="b7a14-110">CBVs.</span></span>
- <span data-ttu-id="b7a14-111">Viste delle risorse shader (SRVs)/unordered Access views (UAV) delle risorse del buffer in cui il formato SRV/UAV contiene solo componenti FLOAT/UINT/SINT di 32 bit (non è prevista alcuna conversione del formato).</span><span class="sxs-lookup"><span data-stu-id="b7a14-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="b7a14-112">SRVs delle strutture di accelerazione raytracing, in firme radice locali o globali.</span><span class="sxs-lookup"><span data-stu-id="b7a14-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="b7a14-113">UAV nella radice non possono avere contatori associati.</span><span class="sxs-lookup"><span data-stu-id="b7a14-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="b7a14-114">I descrittori nella firma radice vengono visualizzati come singoli descrittori separati &mdash; che non possono essere indicizzati dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="b7a14-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="b7a14-115">Nell'esempio precedente non `mySceneData` può essere dichiarato come una matrice, come in `cbuffer mySceneData[2]` se verrà eseguito il mapping a un descrittore nella firma radice, poiché l'indicizzazione tra i descrittori non è supportata nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="b7a14-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="b7a14-116">L'applicazione può definire singoli buffer costanti distinti e definirli ciascuno come voce distinta nella firma radice, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="b7a14-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="b7a14-117">Si noti che in `mySceneData` precedenza è presente una matrice `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="b7a14-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="b7a14-118">L'indicizzazione dinamica all'interno del buffer costante è valida: un descrittore nella firma radice si comporta esattamente come lo stesso descrittore si comporterebbe in caso di accesso tramite un heap dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="b7a14-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="b7a14-119">Si tratta di un contrasto con le costanti di incorporamento direttamente nella firma radice, che appare anche come un buffer costante, tranne nel caso in cui non sia consentito l'indicizzazione dinamica all'interno delle costanti inline. non è quindi `bar[2]` consentito.</span><span class="sxs-lookup"><span data-stu-id="b7a14-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="b7a14-120">Le API seguenti (dall'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) sono per impostare i descrittori direttamente nella firma radice:</span><span class="sxs-lookup"><span data-stu-id="b7a14-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="b7a14-121">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="b7a14-122">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="b7a14-123">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="b7a14-124">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="b7a14-125">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="b7a14-126">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="b7a14-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="b7a14-127">In Direct3D 12 non esiste alcun concetto di "matrice descrittore radice".</span><span class="sxs-lookup"><span data-stu-id="b7a14-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="b7a14-128">Le matrici di descrittori sono supportate solo negli heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="b7a14-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a14-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7a14-129">Related topics</span></span>

[<span data-ttu-id="b7a14-130">Firme radice</span><span class="sxs-lookup"><span data-stu-id="b7a14-130">Root Signatures</span></span>](root-signatures.md)
