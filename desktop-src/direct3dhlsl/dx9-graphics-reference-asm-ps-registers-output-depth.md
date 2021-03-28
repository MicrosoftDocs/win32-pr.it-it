---
title: Registro profondità output
description: Il registro di profondità dell'output pixel shader (oDepth) è un registro scalare di sola scrittura con l'intervallo \ 0.. 1 \ che restituisce un nuovo valore di profondità per un test di profondità sul buffer di stencil di profondità.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332604"
---
# <a name="output-depth-register"></a><span data-ttu-id="5a03a-103">Registro profondità output</span><span class="sxs-lookup"><span data-stu-id="5a03a-103">Output Depth Register</span></span>

<span data-ttu-id="5a03a-104">Il registro di profondità dell'output pixel shader (oDepth) è un registro scalare di sola scrittura con l'intervallo \[ 0.. 1 \] che restituisce un nuovo valore di profondità per un test di profondità sul buffer dello stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="5a03a-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="5a03a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a03a-105">Syntax</span></span>



| <span data-ttu-id="5a03a-106">oDepth</span><span class="sxs-lookup"><span data-stu-id="5a03a-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="5a03a-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="5a03a-107">Where:</span></span>



| <span data-ttu-id="5a03a-108">Nome</span><span class="sxs-lookup"><span data-stu-id="5a03a-108">Name</span></span>   | <span data-ttu-id="5a03a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a03a-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="5a03a-110">oDepth</span><span class="sxs-lookup"><span data-stu-id="5a03a-110">oDepth</span></span> | <span data-ttu-id="5a03a-111">Nuovo valore di profondità per un test di profondità sul buffer di stencil Depth</span><span class="sxs-lookup"><span data-stu-id="5a03a-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="5a03a-112">È importante tenere presente che la scrittura in oDepth causa la perdita di tutti gli algoritmi di ottimizzazione del buffer di profondità specifici dell'hardware (ovvero la Z gerarchica) che accelerano le prestazioni dei test di profondità.</span><span class="sxs-lookup"><span data-stu-id="5a03a-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="5a03a-113">La replica di swizzle di origine (con estensione x. \| \| z. \| w) è obbligatoria quando si scrive in oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="5a03a-114">Non sono consentite maschere di scrittura esplicite.</span><span class="sxs-lookup"><span data-stu-id="5a03a-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="5a03a-115">La scrittura nel registro oDepth sostituisce il valore di profondità interpolata (ignorando eventuali distorsioni di profondità/slopescale renderstates).</span><span class="sxs-lookup"><span data-stu-id="5a03a-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="5a03a-116">Se non è stato creato o collegato alcun buffer di profondità al dispositivo, la scrittura in oDepth viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="5a03a-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="5a03a-117">Se si esegue il campionamento multiplo e si scrive in oDepth, poiché il pixel shader viene eseguito una sola volta per pixel, il valore di profondità viene replicato per tutte le posizioni sottocampionate coperte.</span><span class="sxs-lookup"><span data-stu-id="5a03a-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="5a03a-118">Il test di profondità si verifica ancora per campione, ma non è presente un valore di profondità per campione che entra nel confronto dal pixel shader come se non fosse stato scritto oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="5a03a-119">Se un'applicazione dispone di un w-buffer impostato come buffer di profondità, è necessario prenderlo in considerazione durante la scrittura in oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="5a03a-120">Potrebbe potenzialmente dover inviare informazioni di intervallo w al pixel shader e calcolare l'intervallo w per ridimensionare i valori w scritti in oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="5a03a-121">\_restrizioni PS 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a03a-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="5a03a-122">oDepth può essere scritto solo con l'istruzione [MOV-PS](mov---ps.md) e può essere eseguito solo una volta.</span><span class="sxs-lookup"><span data-stu-id="5a03a-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="5a03a-123">Non è consentito alcun modificatore di origine durante la scrittura in oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="5a03a-124">Nessun modificatore di istruzione consentito durante la scrittura in oDepth.</span><span class="sxs-lookup"><span data-stu-id="5a03a-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="5a03a-125">Nessuna scrittura in oDepth dall'interno di un costrutto di controllo di flusso o quando si usa predicazione.</span><span class="sxs-lookup"><span data-stu-id="5a03a-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="5a03a-126">Restrizioni di PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a03a-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="5a03a-127">Per PS \_ 3 \_ 0, i registri di output OC # e od \# possono essere scritti un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="5a03a-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="5a03a-128">L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="5a03a-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="5a03a-129">Se non si verifica una scrittura in un registro di output, probabilmente a causa del controllo di flusso o se lo shader non lo scrive, non viene aggiornata anche la destinazione di rendering corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5a03a-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="5a03a-130">Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.</span><span class="sxs-lookup"><span data-stu-id="5a03a-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="5a03a-131">È possibile scrivere in oDepth all'interno del controllo di flusso o predicazione a condizione che tutti i percorsi possibili vengano scritti nel registro.</span><span class="sxs-lookup"><span data-stu-id="5a03a-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="5a03a-132">Non è possibile eseguire alcun calcolo sfumato (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) all'interno delle istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso).</span><span class="sxs-lookup"><span data-stu-id="5a03a-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="5a03a-133">L'istruzione predicazione non è considerata il controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="5a03a-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a03a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a03a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a03a-135">Registri</span><span class="sxs-lookup"><span data-stu-id="5a03a-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




