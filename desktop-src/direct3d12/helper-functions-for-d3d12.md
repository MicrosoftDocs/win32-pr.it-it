---
title: Funzioni helper per D3D12
description: Queste funzioni helper contribuiscono in particolare alla gestione delle sottorisorse e vengono dichiarate in d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funzioni helper
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298465"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="79807-105">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="79807-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="79807-106">Queste funzioni helper contribuiscono in particolare alla gestione delle sottorisorse e vengono dichiarate in **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="79807-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79807-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="79807-107">In this section</span></span>



| <span data-ttu-id="79807-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="79807-108">Topic</span></span>                                                                                             | <span data-ttu-id="79807-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79807-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79807-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="79807-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="79807-111">Questo modello di funzione esegue il cast di un puntatore costante a un elenco di comandi in un puntatore const a un ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="79807-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="79807-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="79807-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="79807-113">Calcola un indice di una sottorisorsa per una trama.</span><span class="sxs-lookup"><span data-stu-id="79807-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="79807-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="79807-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="79807-115">Restituisce la sezione MIP, la sezione della matrice e la sezione del piano che corrispondono all'indice della sottorisorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="79807-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="79807-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="79807-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="79807-117">Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata ( **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="79807-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="79807-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="79807-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="79807-119">Indica se il layout è opaco.</span><span class="sxs-lookup"><span data-stu-id="79807-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="79807-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="79807-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="79807-121">Restituisce il tipo di sottooggetto che corrisponde alla classe di base del tipo di sottooggetto passato.</span><span class="sxs-lookup"><span data-stu-id="79807-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="79807-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="79807-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="79807-123">Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata.</span><span class="sxs-lookup"><span data-stu-id="79807-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="79807-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="79807-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="79807-125">Consente di abilitare le funzionalità della firma radice 1,1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la creazione di firme radice.</span><span class="sxs-lookup"><span data-stu-id="79807-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="79807-126">Questo metodo helper ricostruisce una firma radice della versione 1,0 quando la versione 1,1 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="79807-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="79807-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="79807-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="79807-128">Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="79807-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="79807-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="79807-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="79807-130">Copia una sottorisorsa riga per riga.</span><span class="sxs-lookup"><span data-stu-id="79807-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="79807-131">**Updatesubresources con**</span><span class="sxs-lookup"><span data-stu-id="79807-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="79807-132">Aggiorna le sottorisorse, tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="79807-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="79807-133">**Updatesubresources con (allocazione heap)**</span><span class="sxs-lookup"><span data-stu-id="79807-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="79807-134">Aggiorna le sottorisorse con un'implementazione di allocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="79807-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="79807-135">**Updatesubresources con (allocazione dello stack)**</span><span class="sxs-lookup"><span data-stu-id="79807-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="79807-136">Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.</span><span class="sxs-lookup"><span data-stu-id="79807-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="79807-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79807-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79807-138">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="79807-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="79807-139">Funzioni e strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="79807-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





