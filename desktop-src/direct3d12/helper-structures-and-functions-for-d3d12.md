---
title: Funzioni e strutture helper per D3D12
description: Queste strutture helper e funzioni helper sono dichiarate in d3dx12. h.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funzioni helper
- Strutture Helper
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298463"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="343d0-106">Funzioni e strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="343d0-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="343d0-107">Queste strutture helper e funzioni helper sono dichiarate in **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="343d0-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="343d0-108">È possibile utilizzare queste strutture helper per creare e inizializzare le strutture Direct3D.</span><span class="sxs-lookup"><span data-stu-id="343d0-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="343d0-109">Queste strutture Helper si comportano come le classi C++.</span><span class="sxs-lookup"><span data-stu-id="343d0-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="343d0-110">Ogni struttura di supporto in genere ha un costruttore predefinito, un costruttore esplicito, un distruttore e un operatore cast per la struttura D3D12 associata.</span><span class="sxs-lookup"><span data-stu-id="343d0-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="343d0-111">Ogni struttura di supporto presenta un prefisso ' c'ed è associata a una struttura D3D12 che non dispone del prefisso ' c'.</span><span class="sxs-lookup"><span data-stu-id="343d0-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="343d0-112">La maggior parte delle strutture Helper contengono metodi membri di inizializzazione, alcuni contengono funzioni di confronto.</span><span class="sxs-lookup"><span data-stu-id="343d0-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="343d0-113">**d3dx12. h** è disponibile separatamente dalle intestazioni Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="343d0-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="343d0-114">È possibile scaricare **d3dx12. h** dalla [libreria helper di D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span><span class="sxs-lookup"><span data-stu-id="343d0-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="343d0-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="343d0-115">In this section</span></span>



| <span data-ttu-id="343d0-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="343d0-116">Topic</span></span>                                                                     | <span data-ttu-id="343d0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343d0-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="343d0-118">Interfacce helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="343d0-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="343d0-119">Queste interfacce Helper contribuiscono in particolare alla gestione delle sottorisorse e vengono dichiarate in **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="343d0-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="343d0-120">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="343d0-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="343d0-121">Queste strutture helper consentono di inizializzare molte delle strutture Direct3D 12 e vengono dichiarate in **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="343d0-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="343d0-122">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="343d0-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="343d0-123">Queste funzioni helper contribuiscono in particolare alla gestione delle sottorisorse e vengono dichiarate in **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="343d0-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="343d0-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="343d0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343d0-125">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="343d0-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





