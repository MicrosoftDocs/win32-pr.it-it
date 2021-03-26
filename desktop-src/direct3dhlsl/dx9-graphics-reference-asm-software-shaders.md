---
title: Shader software
description: Gli shader software sono implementati per consentire lo sviluppo di shader senza supporto hardware sottostante. Supportano il set completo di funzionalità. Poiché sono implementate nel software, non produrranno le prestazioni migliori.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045386"
---
# <a name="software-shaders"></a><span data-ttu-id="7d9f9-105">Shader software</span><span class="sxs-lookup"><span data-stu-id="7d9f9-105">Software Shaders</span></span>

<span data-ttu-id="7d9f9-106">Gli shader software sono implementati per consentire lo sviluppo di shader senza supporto hardware sottostante.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="7d9f9-107">Supportano il set completo di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-107">They support the full feature set.</span></span> <span data-ttu-id="7d9f9-108">Poiché sono implementate nel software, non produrranno le prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="7d9f9-109">Versione</span><span class="sxs-lookup"><span data-stu-id="7d9f9-109">Version</span></span>   | <span data-ttu-id="7d9f9-110">Set di funzionalità</span><span class="sxs-lookup"><span data-stu-id="7d9f9-110">Feature Set</span></span>                  | <span data-ttu-id="7d9f9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d9f9-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="7d9f9-112">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d9f9-112">vs\_2\_sw</span></span> | <span data-ttu-id="7d9f9-113">Tutte le funzionalità di vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d9f9-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="7d9f9-114">Supportato solo dall'elaborazione dei vertici software e da un dispositivo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="7d9f9-115">Visual Studio \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d9f9-115">vs\_3\_sw</span></span> | <span data-ttu-id="7d9f9-116">Tutte le funzionalità di vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d9f9-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="7d9f9-117">Supportato solo dall'elaborazione dei vertici software e da un dispositivo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="7d9f9-118">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d9f9-118">ps\_2\_sw</span></span> | <span data-ttu-id="7d9f9-119">Tutte le funzionalità di PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d9f9-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="7d9f9-120">Supportato solo da un dispositivo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="7d9f9-121">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d9f9-121">ps\_3\_sw</span></span> | <span data-ttu-id="7d9f9-122">Tutte le funzionalità di PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d9f9-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="7d9f9-123">Supportato solo da un dispositivo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="7d9f9-124">Alcune convalide sono rilassate per gli shader software.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="7d9f9-125">Questa operazione è utile a scopo di debug e creazione di prototipi.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="7d9f9-126">Le convalide seguenti sono rilassate: (tutte le altre convalide rimangono invariate)</span><span class="sxs-lookup"><span data-stu-id="7d9f9-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="7d9f9-127">Validation type (Tipo di convalida)</span><span class="sxs-lookup"><span data-stu-id="7d9f9-127">Validation type</span></span>                                 | <span data-ttu-id="7d9f9-128">Relax</span><span class="sxs-lookup"><span data-stu-id="7d9f9-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9f9-129">Conteggi istruzioni:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-129">Instruction Counts:</span></span>                             | <span data-ttu-id="7d9f9-130">Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d9f9-131">Sono consentite istruzioni illimitate.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="7d9f9-132">Conteggi costanti float:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="7d9f9-133">Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d9f9-134">Sono consentite fino a 8192 costanti.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d9f9-135">Conteggi costanti integer:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="7d9f9-136">Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d9f9-137">Sono consentite fino a 2048 costanti.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d9f9-138">Conteggi costanti booleane:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="7d9f9-139">Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d9f9-140">Sono consentite fino a 2048 costanti.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d9f9-141">Profondità lettura dipendente:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="7d9f9-142">Questo è rilassato per PS \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="7d9f9-143">Come in vs \_ 3 \_ 0 e PS \_ 3 \_ 0, sono consentite letture dipendenti illimitate.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d9f9-144">Numero di istruzioni ed etichette per il controllo di flusso:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="7d9f9-145">Questo è rilassato per vs \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="7d9f9-146">Sono consentite istruzioni di controllo di flusso illimitate e fino a 2048 etichette.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d9f9-147">Conteggio cicli/avvio/passaggio:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="7d9f9-148">Questi sono rilassati per vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="7d9f9-149">Le dimensioni dei passaggi di inizio e di interoperabilità delle iterazioni per le istruzioni Rep e loop sono con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="7d9f9-150">Il numero di interzioni può essere massimo \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="7d9f9-151">Limiti di lettura-porta:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-151">Read-port limits:</span></span>                               | <span data-ttu-id="7d9f9-152">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW non hanno limiti di lettura della porta.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="7d9f9-153">Numero di interpolatori:</span><span class="sxs-lookup"><span data-stu-id="7d9f9-153">Number of interpolators:</span></span>                        | <span data-ttu-id="7d9f9-154">Sono presenti 16 [registri-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) in vs \_ 3 \_ SW e 10 [PS \_ 3 \_ 0 registri](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) per PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d9f9-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7d9f9-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d9f9-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d9f9-156">Informazioni di riferimento su ASM shader</span><span class="sxs-lookup"><span data-stu-id="7d9f9-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




