---
title: Gestione della memoria in Direct3D 12
description: Il passaggio a D3D12 comporta una corretta sincronizzazione e gestione della residenza di memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103649"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="d7962-103">Gestione della memoria in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d7962-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="d7962-104">Il passaggio a D3D12 comporta una corretta sincronizzazione e gestione della residenza di memoria.</span><span class="sxs-lookup"><span data-stu-id="d7962-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="d7962-105">La gestione della residenza della memoria significa che è necessario eseguire ancora più sincronizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d7962-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="d7962-106">In questa sezione vengono illustrate le strategie di gestione della memoria e le sottoallocazioni all'interno di heap e buffer.</span><span class="sxs-lookup"><span data-stu-id="d7962-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="d7962-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="d7962-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="d7962-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7962-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="d7962-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d7962-109">In this section</span></span>



| <span data-ttu-id="d7962-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="d7962-110">Topic</span></span>                                                                       | <span data-ttu-id="d7962-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7962-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7962-112">Strategie di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="d7962-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="d7962-113">Un gestore della memoria per Direct3D 12 potrebbe essere molto complicato rapidamente con tutti i diversi livelli di supporto, per gli adapter UMA o discreti (non-UMA) e con una vasta gamma di differenze di architettura tra gli adattatori GPU.</span><span class="sxs-lookup"><span data-stu-id="d7962-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discreet (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="d7962-114">La strategia consigliata per la gestione della memoria di Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".</span><span class="sxs-lookup"><span data-stu-id="d7962-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="d7962-115">Sottoallocazione nei buffer</span><span class="sxs-lookup"><span data-stu-id="d7962-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="d7962-116">I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU.</span><span class="sxs-lookup"><span data-stu-id="d7962-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="d7962-117">Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.</span><span class="sxs-lookup"><span data-stu-id="d7962-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="d7962-118">Sottoallocazione negli heap</span><span class="sxs-lookup"><span data-stu-id="d7962-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="d7962-119">Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro).</span><span class="sxs-lookup"><span data-stu-id="d7962-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="d7962-120">Residenza</span><span class="sxs-lookup"><span data-stu-id="d7962-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="d7962-121">Un oggetto viene considerato *residente* quando è accessibile dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="d7962-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="d7962-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7962-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7962-123">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d7962-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d7962-124">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="d7962-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





