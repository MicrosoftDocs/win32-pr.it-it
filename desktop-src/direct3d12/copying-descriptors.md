---
title: Copia di descrittori
description: I metodi ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104739"
---
# <a name="copying-descriptors"></a><span data-ttu-id="9b20f-103">Copia di descrittori</span><span class="sxs-lookup"><span data-stu-id="9b20f-103">Copying Descriptors</span></span>

<span data-ttu-id="9b20f-104">I metodi [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori.</span><span class="sxs-lookup"><span data-stu-id="9b20f-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="9b20f-105">Possono essere denominati thread gratuiti purché più thread sulla CPU o sulla GPU non eseguano Scritture potenzialmente in conflitto.</span><span class="sxs-lookup"><span data-stu-id="9b20f-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="9b20f-106">Copia immediata dei descrittori (sequenza temporale CPU)</span><span class="sxs-lookup"><span data-stu-id="9b20f-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="9b20f-107">Il numero di descrittori di origine (da copiare), specificato come set di intervalli di descrittori, deve essere uguale al numero di descrittori di destinazione (da copiare in), specificato come set separato di intervalli di descrittori.</span><span class="sxs-lookup"><span data-stu-id="9b20f-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="9b20f-108">Gli intervalli di origine e di destinazione non devono altrimenti essere allineati.</span><span class="sxs-lookup"><span data-stu-id="9b20f-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="9b20f-109">Un set di descrittori di tipo sparse, ad esempio, può essere copiato in una destinazione contigua, viceversa o in una combinazione.</span><span class="sxs-lookup"><span data-stu-id="9b20f-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="9b20f-110">Nell'operazione di copia possono essere necessari più heap dei descrittori, sia come origine che come destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b20f-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="9b20f-111">L'uso di handle di descrittore come parametri significa che i metodi di copia non sono interessati agli heap in cui si trova un determinato descrittore. si tratta solo di memoria.</span><span class="sxs-lookup"><span data-stu-id="9b20f-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="9b20f-112">I tipi di heap del descrittore che vengono copiati da e a devono corrispondere, quindi i metodi accettano un solo tipo di heap del descrittore come input.</span><span class="sxs-lookup"><span data-stu-id="9b20f-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="9b20f-113">Il driver deve conoscere il tipo di heap di tutti i descrittori nell'operazione di copia specificata, quindi sa quali dimensioni dei dati sono incluse nell'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="9b20f-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="9b20f-114">Il driver potrebbe anche dover eseguire operazioni di copia personalizzate se un determinato tipo di heap del descrittore lo garantisce, ovvero un dettaglio di implementazione.</span><span class="sxs-lookup"><span data-stu-id="9b20f-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="9b20f-115">Si noti che gli handle di descrittore non identificano in altro modo il tipo a cui puntano; Pertanto, per l'operazione di copia è necessario un parametro aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="9b20f-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="9b20f-116">Viene fornita un'API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) per il semplice caso di copiare un singolo intervallo di descrittori da una posizione a un'altra, [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="9b20f-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="9b20f-117">Per questi metodi di copia del descrittore (sequenza temporale CPU) basati su dispositivo, i descrittori di origine devono provenire da un heap dei descrittori non shader visibile.</span><span class="sxs-lookup"><span data-stu-id="9b20f-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="9b20f-118">I descrittori di destinazione possono trovarsi in qualsiasi heap del descrittore che sia visibile alla CPU (visibile o meno dello shader).</span><span class="sxs-lookup"><span data-stu-id="9b20f-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b20f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b20f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b20f-120">Descrittori</span><span class="sxs-lookup"><span data-stu-id="9b20f-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




