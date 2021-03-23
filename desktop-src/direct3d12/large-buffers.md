---
title: Sottoallocazione nei buffer
description: I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103651"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="e79bd-104">Sottoallocazione nei buffer</span><span class="sxs-lookup"><span data-stu-id="e79bd-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="e79bd-105">I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU.</span><span class="sxs-lookup"><span data-stu-id="e79bd-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="e79bd-106">Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.</span><span class="sxs-lookup"><span data-stu-id="e79bd-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="e79bd-107">Analogamente a D3D11, le applicazioni in D3D12 devono ancora dichiarare l'utilizzo della memoria durante l'allocazione dei buffer in D3D12 rispetto alle risorse dinamiche/di staging in D3D11, ma in D3D12 gli sviluppatori hanno maggiore flessibilità e un controllo più rigoroso sull'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="e79bd-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="e79bd-108">Per la gestione della memoria di basso livello, i buffer, tramite la suballocazione, hanno tutte le funzionalità necessarie.</span><span class="sxs-lookup"><span data-stu-id="e79bd-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e79bd-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e79bd-109">In this section</span></span>



| <span data-ttu-id="e79bd-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="e79bd-110">Topic</span></span>                                                                                        | <span data-ttu-id="e79bd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e79bd-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e79bd-112">Caricamento di diversi tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="e79bd-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="e79bd-113">Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer.</span><span class="sxs-lookup"><span data-stu-id="e79bd-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="e79bd-114">L'utilizzo di un singolo buffer aumenta la flessibilità di utilizzo della memoria e fornisce alle applicazioni un controllo più rigoroso sull'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="e79bd-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="e79bd-115">Mostra anche le differenze tra i modelli D3D11 e D3D12 per il caricamento di diversi tipi di risorse.</span><span class="sxs-lookup"><span data-stu-id="e79bd-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="e79bd-116">Caricamento dei dati di trama tramite buffer</span><span class="sxs-lookup"><span data-stu-id="e79bd-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="e79bd-117">Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlato al passo della riga.</span><span class="sxs-lookup"><span data-stu-id="e79bd-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="e79bd-118">I buffer possono essere usati in modo ortogonale e simultaneamente da più parti della pipeline grafica e sono molto flessibili.</span><span class="sxs-lookup"><span data-stu-id="e79bd-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="e79bd-119">Eseguire la lettura dei dati tramite un buffer</span><span class="sxs-lookup"><span data-stu-id="e79bd-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="e79bd-120">La lettura dei dati dalla GPU, ad esempio l'acquisizione di uno screenshot, comporta l'uso dell'heap readback.</span><span class="sxs-lookup"><span data-stu-id="e79bd-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e79bd-121">Gestione delle risorse basata su recinzioni</span><span class="sxs-lookup"><span data-stu-id="e79bd-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="e79bd-122">Viene illustrato come gestire il ciclo di vita dei dati delle risorse tenendo traccia dello stato di avanzamento della GPU tramite le recinzioni.</span><span class="sxs-lookup"><span data-stu-id="e79bd-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="e79bd-123">La memoria può essere riutilizzata in modo efficace con le barriere gestendo con attenzione la disponibilità dello spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap di caricamento.</span><span class="sxs-lookup"><span data-stu-id="e79bd-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="e79bd-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e79bd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e79bd-125">Gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="e79bd-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





