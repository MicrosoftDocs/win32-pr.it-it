---
title: Funzioni helper per D3D12
description: Queste funzioni helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in d3dx12.h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funzioni helper
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102136"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="cf1fd-105">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="cf1fd-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="cf1fd-106">Queste funzioni helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in **d3dx12.h**.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cf1fd-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cf1fd-107">In this section</span></span>



| <span data-ttu-id="cf1fd-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="cf1fd-108">Topic</span></span>                                                                                             | <span data-ttu-id="cf1fd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf1fd-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf1fd-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-110">**CommandListCast**</span></span>](commandlistcast.md)<br/>                                     | <span data-ttu-id="cf1fd-111">Questo modello di funzione esegue il cast di un puntatore costante a qualsiasi elenco di comandi in un puntatore const a id3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="cf1fd-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="cf1fd-113">Calcola un indice di sottorisorsa per una trama.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="cf1fd-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="cf1fd-115">Restituisce la sezione mip, la sezione di matrice e la sezione del piano che corrispondono all'indice di sottorisorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="cf1fd-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="cf1fd-117">Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata **(ID3D12Device).**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="cf1fd-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="cf1fd-119">Indica se il layout è opaco.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="cf1fd-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="cf1fd-121">Restituisce il tipo di oggetto secondario che corrisponde alla classe di base del tipo di oggetto secondario passato.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="cf1fd-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="cf1fd-123">Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di oggetto secondario analizzata.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="cf1fd-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="cf1fd-125">Consente di abilitare le funzionalità della firma radice 1.1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la compilazione delle firme radice.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="cf1fd-126">Questo metodo helper ricostruisce una firma radice della versione 1.0 quando la versione 1.1 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="cf1fd-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="cf1fd-128">Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="cf1fd-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="cf1fd-130">Copia una sottorisorsa riga per riga.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="cf1fd-131">**Aggiornamentiubresources**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="cf1fd-132">Aggiorna le sottorisorse. Tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device::GetCopyablePrints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="cf1fd-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="cf1fd-133">**Updatesubresources (allocazione heap)**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="cf1fd-134">Aggiorna le sottorisorse con un'implementazione di allocazione heap.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="cf1fd-135">**Updatesubresources (allocazione dello stack)**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="cf1fd-136">Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="cf1fd-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf1fd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf1fd-138">Informazioni di riferimento su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cf1fd-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="cf1fd-139">Strutture e funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="cf1fd-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





