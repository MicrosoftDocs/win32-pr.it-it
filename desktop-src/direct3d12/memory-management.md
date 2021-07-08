---
title: Gestione della memoria in Direct3D 12
description: Il passaggio a D3D12 comporta l'esecuzione di una corretta sincronizzazione e gestione della residenza della memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481806"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="58646-103">Gestione della memoria in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="58646-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="58646-104">Il passaggio a D3D12 comporta l'esecuzione di una corretta sincronizzazione e gestione della residenza della memoria.</span><span class="sxs-lookup"><span data-stu-id="58646-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="58646-105">La gestione della residenza della memoria significa che è necessario eseguire una sincronizzazione ancora maggiore.</span><span class="sxs-lookup"><span data-stu-id="58646-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="58646-106">Questa sezione illustra le strategie di gestione della memoria e la sottoallocazione all'interno di heap e buffer.</span><span class="sxs-lookup"><span data-stu-id="58646-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="58646-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="58646-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="58646-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58646-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="58646-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="58646-109">In this section</span></span>



| <span data-ttu-id="58646-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="58646-110">Topic</span></span>                                                                       | <span data-ttu-id="58646-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58646-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58646-112">Strategie di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="58646-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="58646-113">Un gestore di memoria per Direct3D 12 può essere molto complicato rapidamente con tutti i diversi livelli di supporto, per schede UMA o discrete (non UMA) e con una notevole gamma di differenze di architettura tra le schede GPU.</span><span class="sxs-lookup"><span data-stu-id="58646-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="58646-114">La strategia consigliata per la gestione della memoria Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".</span><span class="sxs-lookup"><span data-stu-id="58646-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="58646-115">Sottoallocazione all'interno dei buffer</span><span class="sxs-lookup"><span data-stu-id="58646-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="58646-116">I buffer hanno tutte le funzionalità necessarie in D3D12 perché le applicazioni trasferiscono un'ampia gamma di dati temporanei dalla CPU alla GPU.</span><span class="sxs-lookup"><span data-stu-id="58646-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="58646-117">Questa sezione illustra quattro scenari comuni per l'uso e la gestione di risorse e buffer.</span><span class="sxs-lookup"><span data-stu-id="58646-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="58646-118">Sottoallocazione all'interno degli heap</span><span class="sxs-lookup"><span data-stu-id="58646-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="58646-119">Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (read back).</span><span class="sxs-lookup"><span data-stu-id="58646-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="58646-120">Residency</span><span class="sxs-lookup"><span data-stu-id="58646-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="58646-121">Un oggetto viene considerato *residente* quando è accessibile dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="58646-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="58646-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58646-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58646-123">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="58646-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="58646-124">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="58646-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





