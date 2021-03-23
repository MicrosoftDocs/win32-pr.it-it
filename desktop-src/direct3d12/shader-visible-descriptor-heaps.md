---
title: Heap del descrittore visibile dello shader
description: Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104332"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="d3953-103">Heap del descrittore visibile dello shader</span><span class="sxs-lookup"><span data-stu-id="d3953-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="d3953-104">Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="d3953-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="d3953-105">Overview</span><span class="sxs-lookup"><span data-stu-id="d3953-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="d3953-106">un esempio</span><span class="sxs-lookup"><span data-stu-id="d3953-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="d3953-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3953-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d3953-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d3953-108">Overview</span></span>

<span data-ttu-id="d3953-109">Gli heap del descrittore a cui possono fare riferimento gli shader tramite le tabelle dei descrittori sono disponibili in un paio di varianti: un tipo di heap, D3D12 \_ SRV \_ UAV \_ CBV \_ descrittore \_ , può contenere visualizzazioni di risorse shader, viste di accesso non ordinate e visualizzazioni di buffer costanti, tutte intermiste.</span><span class="sxs-lookup"><span data-stu-id="d3953-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="d3953-110">Qualsiasi posizione specificata nell'heap può essere uno dei tipi elencati dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="d3953-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="d3953-111">Un altro tipo di heap \_ , \_ Sampler di tipo heap del descrittore D3D12 \_ \_ , archivia solo i sampler, che riflettono il fatto che, per la maggior parte dell'hardware, i sampler vengono gestiti separatamente da SRVs, UAV, CBVs.</span><span class="sxs-lookup"><span data-stu-id="d3953-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="d3953-112">È possibile che gli heap dei descrittori di questi tipi siano visibili o meno dello shader quando l'heap viene creato (quest'ultimo non visibile, può essere utile per i descrittori di staging sulla CPU).</span><span class="sxs-lookup"><span data-stu-id="d3953-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="d3953-113">Quando viene richiesto di essere visibile allo shader, ogni tipo di heap precedente potrebbe avere un limite di dimensioni hardware per ogni singola allocazione dell'heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="d3953-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="d3953-114">Le applicazioni possono creare un numero qualsiasi di heap di descrittori e gli heap dei descrittori non visibili per gli shader non sono limitati alle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d3953-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="d3953-115">Se un heap del descrittore visibile dello shader creato dall'applicazione è inferiore al limite delle dimensioni hardware, il driver può scegliere di Sottoallocare l'heap del descrittore da un heap del descrittore sottostante più grande, in modo che più heap descrittore API rientrino in un heap descrittore hardware.</span><span class="sxs-lookup"><span data-stu-id="d3953-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="d3953-116">Il motivo potrebbe essere che, per alcuni componenti hardware, il cambio tra gli heap del descrittore hardware durante l'esecuzione richiede che una GPU attenda inattiva (per assicurarsi che i riferimenti GPU all'heap del descrittore precedente siano finiti).</span><span class="sxs-lookup"><span data-stu-id="d3953-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="d3953-117">Se tutti gli heap del descrittore creati da un'applicazione rientrano nelle capacità massime dell'heap hardware applicabile, non si verificheranno tali attese durante il cambio di heap del descrittore API durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d3953-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="d3953-118">Le applicazioni devono tuttavia consentire la possibilità, tuttavia, che il cambio dell'heap del descrittore corrente possa comportare un'attesa di inattività.</span><span class="sxs-lookup"><span data-stu-id="d3953-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="d3953-119">Per evitare che questa operazione sia interessata da questa possibile attesa di inattività nel commutatore heap del descrittore, le applicazioni possono sfruttare le interruzioni del rendering che potrebbero influire sulla GPU per altri motivi, come il tempo necessario per eseguire le commutazioni dell'heap descrittore, dal momento che è in corso un'attesa per inattività</span><span class="sxs-lookup"><span data-stu-id="d3953-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="d3953-120">Il meccanismo e la semantica per l'identificazione degli heap dei descrittori per gli shader durante la registrazione dell'elenco di comandi/bundle sono descritti nella Guida di riferimento alle API.</span><span class="sxs-lookup"><span data-stu-id="d3953-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="d3953-121">un esempio</span><span class="sxs-lookup"><span data-stu-id="d3953-121">An example</span></span>

<span data-ttu-id="d3953-122">L'immagine seguente mostra due heap dei descrittori che fanno riferimento a due trame 2D separate archiviate in due slot di un heap predefinito di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d3953-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="d3953-123">L'heap del descrittore a cui è visibile lo shader può essere accessibile dalla pipeline grafica (inclusi gli shader), quindi la trama 2D è disponibile per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3953-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![heap di descrittori visibili e non visibili](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="d3953-125">Spesso l'hardware GPU della quantità di memoria locale GPU scrivibile dalla CPU (definito memoria combinata) per gli heap dei descrittori è spesso limitato.</span><span class="sxs-lookup"><span data-stu-id="d3953-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="d3953-126">Questo limite è in genere relativo a 96MB per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="d3953-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="d3953-127">Un heap del descrittore del membro 1 milione, con descrittori 32byte, utilizzerebbe, ad esempio, 32 MB.</span><span class="sxs-lookup"><span data-stu-id="d3953-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="d3953-128">Se necessario, il driver eseguirà il fallback sulla memoria di sistema, anche se è consigliabile non creare un numero elevato di heap descrittori di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d3953-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d3953-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3953-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3953-130">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="d3953-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




