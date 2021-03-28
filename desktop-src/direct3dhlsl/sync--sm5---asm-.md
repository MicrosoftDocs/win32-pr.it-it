---
title: sincronizzazione (SM5-ASM)
description: Sincronizzazione del gruppo di thread o barriera di memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993264"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="2e51d-103">sincronizzazione (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2e51d-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="2e51d-104">Sincronizzazione del gruppo di thread o barriera di memoria.</span><span class="sxs-lookup"><span data-stu-id="2e51d-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="2e51d-105">uglobal di sincronizzazione \[ \_ </span><span class="sxs-lookup"><span data-stu-id="2e51d-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="2e51d-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="2e51d-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="2e51d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e51d-107">Remarks</span></span>

<span data-ttu-id="2e51d-108">Per la **sincronizzazione** sono disponibili \_ le opzioni uglobal, \_ ugroup, \_ g e \_ t.</span><span class="sxs-lookup"><span data-stu-id="2e51d-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="2e51d-109">Nel pixel shader è consentito solo **\_ uglobal di sincronizzazione** .</span><span class="sxs-lookup"><span data-stu-id="2e51d-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="2e51d-110">Nel compute shader, \_ è necessario specificare (uglobal o \_ ugroup \* ) e/o \_ g.</span><span class="sxs-lookup"><span data-stu-id="2e51d-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="2e51d-111">\_t è inoltre facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2e51d-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="2e51d-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="2e51d-112">\_uglobal</span></span>

<span data-ttu-id="2e51d-113">\#Recinzione della memoria globale u (UAV).</span><span class="sxs-lookup"><span data-stu-id="2e51d-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="2e51d-114">Tutte le \# letture e scritture di memoria u precedenti eseguite da questo thread nell'ordine del programma vengono rese visibili a tutti i thread sull'intera GPU prima di qualsiasi accesso alla memoria u successivo da parte del \# thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="2e51d-115">L'intera parte GPU della definizione viene sostituita da un ambito meno globale in un caso, descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="2e51d-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="2e51d-116">Si applica a tutti i limiti di memoria UAV nella fase corrente dello shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="2e51d-117">\_uglobal è disponibile nel compute shader o pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="2e51d-118">Per tutti gli UAV associati che non sono stati dichiarati dallo shader come coerenti a livello globale, il limite di \_ memoria uglobal u \# è visibile solo all'interno del gruppo di thread del compute shader corrente per tale UAV, come se fosse \_ ugroup anziché \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="2e51d-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="2e51d-119">Questo problema si applica solo al compute shader, perché il pixel shader deve dichiarare tutti i UAV come coerenti a livello globale.</span><span class="sxs-lookup"><span data-stu-id="2e51d-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="2e51d-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="2e51d-120">\_ugroup</span></span>

<span data-ttu-id="2e51d-121">Limite di memoria u \# (UAV) dell'ambito del gruppo di thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="2e51d-122">Tutte le \# letture o scritture della memoria u precedenti da questo thread nell'ordine del programma vengono rese visibili a tutti i thread del gruppo di thread prima di qualsiasi accesso alla memoria u successivo da parte del \# thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="2e51d-123">Si applica a tutti i limiti di memoria UAV nella fase corrente dello shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="2e51d-124">\_ugroup è disponibile solo nel compute shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="2e51d-125">Se \_ ugroup è esposto, per alcune implementazioni.</span><span class="sxs-lookup"><span data-stu-id="2e51d-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="2e51d-126">Il vantaggio di specificare \_ ugroup anziché \_ uglobal è che l'operazione di **sincronizzazione** può essere completata più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2e51d-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="2e51d-127">Altre implementazioni non distinguono \_ ugroup da \_ uglobal, pertanto entrambe le operazioni sono equivalenti e si comportano come \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="2e51d-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="2e51d-128">Le applicazioni possono specificare il loro scopo richiedendo l'ambito di **sincronizzazione** più restrittivo necessario.</span><span class="sxs-lookup"><span data-stu-id="2e51d-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="2e51d-129">Anche se un determinato UAV viene dichiarato come coerente a livello globale, un' \_ operazione di **sincronizzazione** ugroup funzionerà in modo più efficiente in tale UAV se non è necessaria una barriera globale.</span><span class="sxs-lookup"><span data-stu-id="2e51d-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="2e51d-130">\_g</span><span class="sxs-lookup"><span data-stu-id="2e51d-130">\_g</span></span>

<span data-ttu-id="2e51d-131">limite di \# memoria condivisa del gruppo di thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="2e51d-132">Tutte le operazioni \# di lettura o scrittura di memoria precedenti da parte di questo thread nell'ordine del programma vengono rese visibili a tutti i thread del gruppo di thread prima di eventuali accessi successivi alla memoria g da parte del \# thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="2e51d-133">Questo vale per tutti i file di memoria condivisa g del gruppo di thread corrente \# .</span><span class="sxs-lookup"><span data-stu-id="2e51d-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="2e51d-134">\_g è disponibile solo nel compute shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="2e51d-135">\_t</span><span class="sxs-lookup"><span data-stu-id="2e51d-135">\_t</span></span>

<span data-ttu-id="2e51d-136">Sincronizzazione del gruppo di thread. Tutti i thread all'interno di un singolo gruppo di thread (quelli che possono condividere l'accesso a un set comune di spazio del registro condiviso) verranno eseguiti fino al punto in cui raggiungono questa istruzione prima che un thread possa continuare.</span><span class="sxs-lookup"><span data-stu-id="2e51d-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="2e51d-137">\_t non può essere inserito nel controllo dinamico del flusso, (rami che possono variare all'interno di un gruppo di thread), ma può essere presente in un controllo di flusso uniforme, in cui tutti i thread del gruppo scelgono lo stesso percorso.</span><span class="sxs-lookup"><span data-stu-id="2e51d-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="2e51d-138">\_t è disponibile solo nel compute shader.</span><span class="sxs-lookup"><span data-stu-id="2e51d-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="2e51d-139">Di seguito è riportato un elenco di varianti di Compute Shader "Sync".</span><span class="sxs-lookup"><span data-stu-id="2e51d-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="2e51d-140">Sincronizza \_ g</span><span class="sxs-lookup"><span data-stu-id="2e51d-140">sync\_g</span></span>
-   <span data-ttu-id="2e51d-141">Sincronizza \_ ugroup\*</span><span class="sxs-lookup"><span data-stu-id="2e51d-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="2e51d-142">Sincronizza \_ uglobal</span><span class="sxs-lookup"><span data-stu-id="2e51d-142">sync\_uglobal</span></span>
-   <span data-ttu-id="2e51d-143">Sincronizza \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="2e51d-143">sync\_g\_t</span></span>
-   <span data-ttu-id="2e51d-144">ugroup di sincronizzazione \_ \_ t\*</span><span class="sxs-lookup"><span data-stu-id="2e51d-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="2e51d-145">uglobal di sincronizzazione \_ \_ t</span><span class="sxs-lookup"><span data-stu-id="2e51d-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="2e51d-146">Sincronizza \_ ugroup \_ g\*</span><span class="sxs-lookup"><span data-stu-id="2e51d-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="2e51d-147">Sincronizza \_ uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="2e51d-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="2e51d-148">ugroup di sincronizzazione \_ \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="2e51d-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="2e51d-149">uglobal di sincronizzazione \_ \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="2e51d-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="2e51d-150">\*Le varianti con \_ ugroup potrebbero non essere destinate al compilatore HLSL, in base alla precedente discussione nella \_ sezione ugroup precedente.</span><span class="sxs-lookup"><span data-stu-id="2e51d-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="2e51d-151">L'elenco di pixel shader varianti di sincronizzazione include \_ solo uglobal di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e51d-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="2e51d-152">Le barriere di memoria impediscono il riordinamento delle istruzioni interessate da parte dei compilatori o dell'hardware attraverso la recinzione.</span><span class="sxs-lookup"><span data-stu-id="2e51d-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="2e51d-153">Più letture dallo stesso indirizzo tramite una chiamata dello shader che non sono separate da barriere di memoria o scritture nell'indirizzo possono essere compresse insieme.</span><span class="sxs-lookup"><span data-stu-id="2e51d-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="2e51d-154">Lo stesso vale per le operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="2e51d-154">The same applies to writes.</span></span> <span data-ttu-id="2e51d-155">Gli accessi separati da una barriera non possono essere Uniti o spostati attraverso la barriera.</span><span class="sxs-lookup"><span data-stu-id="2e51d-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="2e51d-156">Le barriere di memoria non sono necessarie per il corretto funzionamento delle operazioni atomiche per un determinato indirizzo da thread diversi.</span><span class="sxs-lookup"><span data-stu-id="2e51d-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="2e51d-157">I limiti sono necessari quando le operazioni atomiche e/o di caricamento/archiviazione devono essere sincronizzate l'una rispetto all'altra, perché appaiono nei singoli thread dal punto di vista di altri thread.</span><span class="sxs-lookup"><span data-stu-id="2e51d-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="2e51d-158">Nel pixel shader, le istruzioni di [eliminazione](discard--sm4---asm-.md) implicano un limite di sincronizzazione \_ uglobal, in quanto non è possibile riordinare le istruzioni in uno **scarto**.</span><span class="sxs-lookup"><span data-stu-id="2e51d-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="2e51d-159">sincronizzare \_ uglobal nei pixel Helper (che vengono eseguiti solo per supportare i derivati) o i pixel rimossi possono avere o meno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="2e51d-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="2e51d-160">Non è consentito per l'helper o i pixel scartati di scrivere in UAV se, nel caso di scarto, le scritture vengono rilasciate dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="2e51d-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="2e51d-161">I valori restituiti da UAV non possono contribuire ai calcoli derivati.</span><span class="sxs-lookup"><span data-stu-id="2e51d-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="2e51d-162">Per questo motivo, se \_ la sincronizzazione u viene rispettata per i pixel helper o quando viene rilasciata, dopo uno scarto è discutibile.</span><span class="sxs-lookup"><span data-stu-id="2e51d-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="2e51d-163">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="2e51d-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="2e51d-164">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e51d-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2e51d-165">Vertice</span><span class="sxs-lookup"><span data-stu-id="2e51d-165">Vertex</span></span> | <span data-ttu-id="2e51d-166">Hull</span><span class="sxs-lookup"><span data-stu-id="2e51d-166">Hull</span></span> | <span data-ttu-id="2e51d-167">Dominio</span><span class="sxs-lookup"><span data-stu-id="2e51d-167">Domain</span></span> | <span data-ttu-id="2e51d-168">Geometria</span><span class="sxs-lookup"><span data-stu-id="2e51d-168">Geometry</span></span> | <span data-ttu-id="2e51d-169">Pixel</span><span class="sxs-lookup"><span data-stu-id="2e51d-169">Pixel</span></span> | <span data-ttu-id="2e51d-170">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2e51d-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2e51d-171">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-171">X</span></span>     | <span data-ttu-id="2e51d-172">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-172">X</span></span>       |



 

<span data-ttu-id="2e51d-173">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, la variante **\_ uglobal di sincronizzazione** di questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e51d-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2e51d-174">Vertice</span><span class="sxs-lookup"><span data-stu-id="2e51d-174">Vertex</span></span> | <span data-ttu-id="2e51d-175">Hull</span><span class="sxs-lookup"><span data-stu-id="2e51d-175">Hull</span></span> | <span data-ttu-id="2e51d-176">Dominio</span><span class="sxs-lookup"><span data-stu-id="2e51d-176">Domain</span></span> | <span data-ttu-id="2e51d-177">Geometria</span><span class="sxs-lookup"><span data-stu-id="2e51d-177">Geometry</span></span> | <span data-ttu-id="2e51d-178">Pixel</span><span class="sxs-lookup"><span data-stu-id="2e51d-178">Pixel</span></span> | <span data-ttu-id="2e51d-179">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2e51d-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2e51d-180">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-180">X</span></span>      | <span data-ttu-id="2e51d-181">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-181">X</span></span>    | <span data-ttu-id="2e51d-182">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-182">X</span></span>      | <span data-ttu-id="2e51d-183">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-183">X</span></span>        | <span data-ttu-id="2e51d-184">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-184">X</span></span>     | <span data-ttu-id="2e51d-185">X</span><span class="sxs-lookup"><span data-stu-id="2e51d-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2e51d-186">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2e51d-186">Minimum Shader Model</span></span>

<span data-ttu-id="2e51d-187">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e51d-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2e51d-188">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2e51d-188">Shader Model</span></span>                                              | <span data-ttu-id="2e51d-189">Supportato</span><span class="sxs-lookup"><span data-stu-id="2e51d-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2e51d-190">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2e51d-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2e51d-191">sì</span><span class="sxs-lookup"><span data-stu-id="2e51d-191">yes</span></span>       |
| [<span data-ttu-id="2e51d-192">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2e51d-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2e51d-193">no</span><span class="sxs-lookup"><span data-stu-id="2e51d-193">no</span></span>        |
| [<span data-ttu-id="2e51d-194">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2e51d-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2e51d-195">no</span><span class="sxs-lookup"><span data-stu-id="2e51d-195">no</span></span>        |
| [<span data-ttu-id="2e51d-196">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e51d-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2e51d-197">no</span><span class="sxs-lookup"><span data-stu-id="2e51d-197">no</span></span>        |
| [<span data-ttu-id="2e51d-198">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e51d-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2e51d-199">no</span><span class="sxs-lookup"><span data-stu-id="2e51d-199">no</span></span>        |
| [<span data-ttu-id="2e51d-200">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e51d-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2e51d-201">no</span><span class="sxs-lookup"><span data-stu-id="2e51d-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2e51d-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e51d-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e51d-203">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e51d-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




