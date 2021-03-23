---
title: Impostazione e popolamento degli heap descrittore
description: I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548813"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="f80ae-103">Impostazione e popolamento degli heap descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="f80ae-104">I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta).</span><span class="sxs-lookup"><span data-stu-id="f80ae-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="f80ae-105">Impostazione degli heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="f80ae-106">Popolamento degli heap descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="f80ae-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f80ae-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="f80ae-108">Impostazione degli heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-108">Setting descriptor heaps</span></span>

<span data-ttu-id="f80ae-109">I tipi di heap dei descrittori che è possibile impostare in un elenco di comandi sono:</span><span class="sxs-lookup"><span data-stu-id="f80ae-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="f80ae-110">Gli heap impostati nell'elenco dei comandi devono essere anche stati creati come shader visibile.</span><span class="sxs-lookup"><span data-stu-id="f80ae-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="f80ae-111">Sono disponibili tre tipi di elenco di comandi: DIRECT, BUNDLE e COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="f80ae-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="f80ae-112">Dopo aver impostato un heap dei descrittori in un elenco di comandi, le chiamate successive che definiscono le tabelle dei descrittori fanno riferimento all'heap descrittore corrente.</span><span class="sxs-lookup"><span data-stu-id="f80ae-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="f80ae-113">Lo stato della tabella descrittore non è definito all'inizio di un elenco di comandi e dopo che gli heap del descrittore sono stati modificati in un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="f80ae-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="f80ae-114">L'impostazione ridondante dello stesso heap del descrittore non determina l'indefinizione delle impostazioni della tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="f80ae-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="f80ae-115">In un bundle, al contrario, gli heap del descrittore possono essere impostati solo una volta (le chiamate ridondanti che imposta lo stesso heap due volte non generano un errore); in caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="f80ae-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="f80ae-116">Gli heap del descrittore impostati devono corrispondere allo stato quando un elenco di comandi chiama il bundle; in caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="f80ae-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="f80ae-117">In questo modo, i bundle possono ereditare e modificare le impostazioni della tabella descrittore dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f80ae-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="f80ae-118">I bundle che non modificano le tabelle dei descrittori (ereditano solo) non devono necessariamente impostare un heap del descrittore e erediteranno solo dall'elenco dei comandi chiamante.</span><span class="sxs-lookup"><span data-stu-id="f80ae-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="f80ae-119">Quando gli heap del descrittore sono impostati (usando [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), tutti gli heap usati vengono impostati in una singola chiamata (e tutti gli heap impostati in precedenza vengono annullati dalla chiamata).</span><span class="sxs-lookup"><span data-stu-id="f80ae-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="f80ae-120">Nella chiamata è possibile impostare al massimo un heap di ogni tipo elencato sopra.</span><span class="sxs-lookup"><span data-stu-id="f80ae-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="f80ae-121">Popolamento degli heap descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-121">Populating descriptor heaps</span></span>

<span data-ttu-id="f80ae-122">Dopo che un'applicazione ha creato un heap del descrittore, può usare i metodi del dispositivo per generare descrittori direttamente nell'heap o copiare i descrittori da una posizione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="f80ae-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="f80ae-123">Il contenuto iniziale della memoria heap del descrittore non è definito, pertanto chiedere alla GPU o al driver di fare riferimento alla memoria non inizializzata per il rendering può causare risultati non definiti, ad esempio la reimpostazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f80ae-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="f80ae-124">Se l'applicazione configura un heap del descrittore in modo che sia visibile alla CPU, la CPU può chiamare i metodi per creare descrittori nell'heap e copiarli da una posizione all'altra (inclusi gli heap) in modo immediato e senza thread.</span><span class="sxs-lookup"><span data-stu-id="f80ae-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="f80ae-125">Se l'heap è stato configurato come SHADER_VISIBLE, la lettura dalla CPU non è consentita.</span><span class="sxs-lookup"><span data-stu-id="f80ae-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="f80ae-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f80ae-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80ae-127">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="f80ae-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




