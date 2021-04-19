---
description: Direct3D 10 supporta più rappresentazioni a virgola mobile diverse. Tutti i calcoli a virgola mobile operano in un subset definito del comportamento a virgola mobile a precisione singola IEEE 754 32 bit.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Regole del punto di FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304803"
---
# <a name="floating-point-rules-direct3d-10"></a><span data-ttu-id="c3f30-104">Regole a virgola mobile (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c3f30-104">Floating-point rules (Direct3D 10)</span></span>

<span data-ttu-id="c3f30-105">Direct3D 10 supporta più rappresentazioni a virgola mobile diverse.</span><span class="sxs-lookup"><span data-stu-id="c3f30-105">Direct3D 10 supports several different floating-point representations.</span></span> <span data-ttu-id="c3f30-106">Tutti i calcoli a virgola mobile operano in un subset definito del comportamento a virgola mobile a precisione singola IEEE 754 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c3f30-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point behavior.</span></span>

-   [<span data-ttu-id="c3f30-107">Regole Floating-Point a 32 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-107">32-bit Floating-Point Rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="c3f30-108">Regole IEEE-754 rispettate</span><span class="sxs-lookup"><span data-stu-id="c3f30-108">Honored IEEE-754 Rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="c3f30-109">Deviazioni o requisiti aggiuntivi da regole IEEE-754</span><span class="sxs-lookup"><span data-stu-id="c3f30-109">Deviations or Additional Requirements from IEEE-754 Rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="c3f30-110">Regole Floating-Point a 16 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-110">16-bit Floating-Point Rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="c3f30-111">Regole di Floating-Point a 11 e 10 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-111">11-bit and 10-bit Floating-Point Rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="c3f30-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3f30-112">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="c3f30-113">Regole Floating-Point a 32 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-113">32-bit Floating-Point Rules</span></span>

<span data-ttu-id="c3f30-114">Sono disponibili due set di regole: quelle conformi a IEEE-754 e quelle che si scostano dallo standard.</span><span class="sxs-lookup"><span data-stu-id="c3f30-114">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="c3f30-115">Regole IEEE-754 rispettate</span><span class="sxs-lookup"><span data-stu-id="c3f30-115">Honored IEEE-754 Rules</span></span>

<span data-ttu-id="c3f30-116">Alcune di queste regole sono una singola opzione in cui IEEE-754 offre opzioni.</span><span class="sxs-lookup"><span data-stu-id="c3f30-116">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="c3f30-117">Divide per 0 produce +/-INF, eccetto 0/0, che restituisce NaN.</span><span class="sxs-lookup"><span data-stu-id="c3f30-117">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="c3f30-118">log di (+/-) 0 produce-INF.</span><span class="sxs-lookup"><span data-stu-id="c3f30-118">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="c3f30-119">il log di un valore negativo (diverso da-0) produce NaN.</span><span class="sxs-lookup"><span data-stu-id="c3f30-119">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="c3f30-120">La radice quadrata reciproca (RSQ) o radice quadrata (sqrt) di un numero negativo produce NaN.</span><span class="sxs-lookup"><span data-stu-id="c3f30-120">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="c3f30-121">L'eccezione è-0; sqrt (-0) produce-0 e RSQ (-0) produce-INF.</span><span class="sxs-lookup"><span data-stu-id="c3f30-121">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="c3f30-122">INF-INF = NaN</span><span class="sxs-lookup"><span data-stu-id="c3f30-122">INF - INF = NaN</span></span>
-   <span data-ttu-id="c3f30-123">(+/-) INF/(+/-) INF = NaN</span><span class="sxs-lookup"><span data-stu-id="c3f30-123">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="c3f30-124">(+/-) INF \* 0 = Nan</span><span class="sxs-lookup"><span data-stu-id="c3f30-124">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="c3f30-125">NaN (any OP) any-value = NaN</span><span class="sxs-lookup"><span data-stu-id="c3f30-125">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="c3f30-126">I confronti EQ, GT, GE, LT e LE, quando uno o entrambi gli operandi è NaN restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c3f30-126">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="c3f30-127">I confronti ignorano il segno di 0 (quindi + 0 è uguale a-0).</span><span class="sxs-lookup"><span data-stu-id="c3f30-127">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="c3f30-128">Il confronto NE, quando uno o entrambi gli operandi è NaN restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="c3f30-128">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="c3f30-129">I confronti di qualsiasi valore non NaN rispetto a +/-INF restituiscono il risultato corretto.</span><span class="sxs-lookup"><span data-stu-id="c3f30-129">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="c3f30-130">Deviazioni o requisiti aggiuntivi da regole IEEE-754</span><span class="sxs-lookup"><span data-stu-id="c3f30-130">Deviations or Additional Requirements from IEEE-754 Rules</span></span>

-   <span data-ttu-id="c3f30-131">IEEE-754 richiede che le operazioni a virgola mobile producano un risultato che rappresenta il valore rappresentabile più vicino a un risultato preciso all'infinito, noto come arrotondato al più vicino.</span><span class="sxs-lookup"><span data-stu-id="c3f30-131">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="c3f30-132">Direct3D 10, tuttavia, definisce un requisito più flessibile: le operazioni a virgola mobile a 32 bit producono un risultato che si trova all'interno di un'unità-Last-Place (1 ULP rispetto) del risultato preciso all'infinito.</span><span class="sxs-lookup"><span data-stu-id="c3f30-132">Direct3D 10, however, defines a looser requirement: 32-bit floating-point operations produce a result that is within one unit-last-place (1 ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="c3f30-133">Ciò significa che, ad esempio, l'hardware può troncare i risultati a 32 bit, anziché eseguire il round-to-the-even più vicino, perché questo genera un errore al massimo di un ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="c3f30-133">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most one ULP.</span></span>
-   <span data-ttu-id="c3f30-134">Non è previsto alcun supporto per eccezioni a virgola mobile, bit di stato o trap.</span><span class="sxs-lookup"><span data-stu-id="c3f30-134">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="c3f30-135">Le denormazioni vengono scaricate allo zero senza segno per l'input e l'output di qualsiasi operazione matematica a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c3f30-135">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="c3f30-136">Vengono eseguite eccezioni per qualsiasi operazione di I/O o spostamento dei dati che non modifica i dati.</span><span class="sxs-lookup"><span data-stu-id="c3f30-136">Exceptions are made for any I/O or data movement operation that does not manipulate the data.</span></span>
-   <span data-ttu-id="c3f30-137">Gli Stati che contengono valori a virgola mobile, ad esempio viewport MinDepth/MaxDepth, i valori BorderColor e così via, possono essere forniti come valori denorm e possono essere scaricati o meno prima dell'utilizzo da parte dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="c3f30-137">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values etc., may be provided as denorm values and may or may not be flushed before use by the hardware.</span></span>
-   <span data-ttu-id="c3f30-138">Le operazioni minime o massime scaricano le denormazioni per il confronto, ma il risultato può essere scaricato o meno.</span><span class="sxs-lookup"><span data-stu-id="c3f30-138">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="c3f30-139">L'input NaN in un'operazione produce sempre NaN nell'output. Tuttavia, non è necessario che lo schema di bit esatto di NaN sia uguale, a meno che l'operazione non sia un'istruzione di spostamento non elaborata, che non modifica i dati.</span><span class="sxs-lookup"><span data-stu-id="c3f30-139">NaN input to an operation always produces NaN on output, however the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which does not alter data at all.)</span></span>
-   <span data-ttu-id="c3f30-140">Le operazioni min o Max per le quali un solo operando è NaN restituiscono l'altro operando come risultato (contrariamente alle regole di confronto precedenti).</span><span class="sxs-lookup"><span data-stu-id="c3f30-140">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules above).</span></span> <span data-ttu-id="c3f30-141">Si tratta di una nuova regola IEEE (IEEE 754R), necessaria in Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="c3f30-141">This is a new IEEE rule (IEEE 754R), required in Direct3D 10.</span></span>
-   <span data-ttu-id="c3f30-142">Un'altra nuova regola IEEE 754R è che min (-0, + 0) = = min (+ 0,-0) = =-0 e Max (-0, + 0) = = Max (+ 0,-0) = = + 0, che rispettano il segno, a differenza delle regole di confronto per zero con segno (sopra indicato).</span><span class="sxs-lookup"><span data-stu-id="c3f30-142">Another new IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honor the sign, in contrast to the comparison rules for signed zero (stated above).</span></span> <span data-ttu-id="c3f30-143">Direct3D 10 consiglia il comportamento IEEE 754R qui, ma non verrà applicato; è possibile che il risultato del confronto degli zeri sia dipendente dall'ordine dei parametri, usando un confronto che ignora i segni.</span><span class="sxs-lookup"><span data-stu-id="c3f30-143">Direct3D 10 recommends the IEEE 754R behavior here, but it will not be enforced; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="c3f30-144">x \* 1.0 f restituisce sempre x (eccetto la denormazione scaricata).</span><span class="sxs-lookup"><span data-stu-id="c3f30-144">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="c3f30-145">x/1.0 f restituisce sempre x (eccetto la denormazione scaricata).</span><span class="sxs-lookup"><span data-stu-id="c3f30-145">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="c3f30-146">x +/-0,0 f restituisce sempre x (eccetto la denormazione scaricata).</span><span class="sxs-lookup"><span data-stu-id="c3f30-146">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="c3f30-147">Ma-0 + 0 = + 0.</span><span class="sxs-lookup"><span data-stu-id="c3f30-147">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="c3f30-148">Le operazioni fuse, ad esempio Mad, DP3, producono risultati che non sono meno accurati rispetto al peggiore ordine seriale possibile di valutazione dell'espansione non fusa dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c3f30-148">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="c3f30-149">Si noti che la definizione del peggiore ordinamento possibile, per finalità di tolleranza, non è una definizione fissa per un'operazione di cui è stata eseguita la fusione. dipende dai valori specifici degli input.</span><span class="sxs-lookup"><span data-stu-id="c3f30-149">Note that the definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="c3f30-150">I singoli passaggi nell'espansione non fusa sono consentiti per ciascuna tolleranza ULP rispetto (o per tutte le istruzioni che Direct3D 10 chiama con una tolleranza di lassismo maggiore di 1 ULP rispetto, maggiore è la tolleranza di lassismo).</span><span class="sxs-lookup"><span data-stu-id="c3f30-150">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D 10 calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="c3f30-151">Le operazioni fuse rispettano le stesse regole NaN delle operazioni non fuse.</span><span class="sxs-lookup"><span data-stu-id="c3f30-151">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="c3f30-152">Multiply e divide each operano a livello di precisione a virgola mobile a 32 bit (accuratezza su 1 ULP rispetto).</span><span class="sxs-lookup"><span data-stu-id="c3f30-152">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 1 ULP).</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="c3f30-153">Regole Floating-Point a 16 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-153">16-bit Floating-Point Rules</span></span>

<span data-ttu-id="c3f30-154">Direct3D 10 supporta inoltre le rappresentazioni a 16 bit dei numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c3f30-154">Direct3D 10 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="c3f30-155">Formato:</span><span class="sxs-lookup"><span data-stu-id="c3f30-155">Format:</span></span>

-   <span data-ttu-id="c3f30-156">1 bit/i di segno nella posizione del bit MSB</span><span class="sxs-lookup"><span data-stu-id="c3f30-156">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="c3f30-157">5 bit di esponente polarizzato (e)</span><span class="sxs-lookup"><span data-stu-id="c3f30-157">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="c3f30-158">10 bit di frazione (f), con un bit nascosto aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="c3f30-158">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="c3f30-159">Un valore float16 (v) segue le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3f30-159">A float16 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="c3f30-160">Se e = = 31 e f! = 0, v è NaN indipendentemente da s</span><span class="sxs-lookup"><span data-stu-id="c3f30-160">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="c3f30-161">Se e = = 31 e f = = 0, v = (-1) s \* Infinity (Signed Infinity)</span><span class="sxs-lookup"><span data-stu-id="c3f30-161">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="c3f30-162">Se e è compreso tra 0 e 31, v = (-1) s \* 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="c3f30-162">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="c3f30-163">Se e = = 0 e f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (numeri denormalizzati)</span><span class="sxs-lookup"><span data-stu-id="c3f30-163">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="c3f30-164">Se e = = 0 e f = = 0, v = (-1) s \* 0 (con segno zero)</span><span class="sxs-lookup"><span data-stu-id="c3f30-164">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="c3f30-165">le regole a virgola mobile a 32 bit sono disponibili anche per i numeri a virgola mobile a 16 bit, adattati per il layout di bit descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c3f30-165">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="c3f30-166">Alcune eccezioni:</span><span class="sxs-lookup"><span data-stu-id="c3f30-166">Exceptions to this include:</span></span>

-   <span data-ttu-id="c3f30-167">Precisione: le operazioni non fuse sui numeri a virgola mobile a 16 bit producono un risultato che rappresenta il valore rappresentabile più vicino a un risultato preciso all'infinito (arrotondato al più vicino anche per IEEE-754, applicato ai valori a 16 bit).</span><span class="sxs-lookup"><span data-stu-id="c3f30-167">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="c3f30-168">le regole a virgola mobile a 32 bit rispettano una tolleranza ULP rispetto, le regole a virgola mobile a 16 bit sono conformi a 0,5 ULP rispetto per le operazioni non fuse e 0,6 ULP rispetto per le operazioni fuse.</span><span class="sxs-lookup"><span data-stu-id="c3f30-168">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="c3f30-169">i numeri a virgola mobile a 16 bit conservano le norme.</span><span class="sxs-lookup"><span data-stu-id="c3f30-169">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="c3f30-170">Regole di Floating-Point a 11 e 10 bit</span><span class="sxs-lookup"><span data-stu-id="c3f30-170">11-bit and 10-bit Floating-Point Rules</span></span>

<span data-ttu-id="c3f30-171">Direct3D 10 supporta inoltre formati a virgola mobile a 11 e 10 bit.</span><span class="sxs-lookup"><span data-stu-id="c3f30-171">Direct3D 10 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="c3f30-172">Formato:</span><span class="sxs-lookup"><span data-stu-id="c3f30-172">Format:</span></span>

-   <span data-ttu-id="c3f30-173">Nessun bit di segno</span><span class="sxs-lookup"><span data-stu-id="c3f30-173">No sign bit</span></span>
-   <span data-ttu-id="c3f30-174">5 bit di esponente polarizzato (e)</span><span class="sxs-lookup"><span data-stu-id="c3f30-174">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="c3f30-175">6 bit della frazione (f) per un formato a 11 bit, a 5 bit di frazione (f) per un formato a 10 bit, con un bit nascosto aggiuntivo in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="c3f30-175">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="c3f30-176">Un valore float11/float10 (v) segue le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3f30-176">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="c3f30-177">Se e = = 31 e f! = 0, v è NaN</span><span class="sxs-lookup"><span data-stu-id="c3f30-177">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="c3f30-178">Se e = = 31 e f = = 0, v = + Infinity</span><span class="sxs-lookup"><span data-stu-id="c3f30-178">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="c3f30-179">Se e è compreso tra 0 e 31, v = 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="c3f30-179">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="c3f30-180">Se e = = 0 e f! = 0, v = \* 2 (e-14) \* (0. f) (numeri denormalizzati)</span><span class="sxs-lookup"><span data-stu-id="c3f30-180">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="c3f30-181">Se e = = 0 e f = = 0, v = 0 (zero)</span><span class="sxs-lookup"><span data-stu-id="c3f30-181">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="c3f30-182">le regole a virgola mobile a 32 bit sono inoltre disponibili per i numeri a virgola mobile a 11 e 10 bit, adattati per il layout di bit descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c3f30-182">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="c3f30-183">Le eccezioni sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3f30-183">Exceptions include:</span></span>

-   <span data-ttu-id="c3f30-184">Precisione: le regole a virgola mobile a 32 bit aderiscono a 0,5 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="c3f30-184">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="c3f30-185">i numeri a virgola mobile 10/11 bit conservano le norme.</span><span class="sxs-lookup"><span data-stu-id="c3f30-185">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="c3f30-186">Qualsiasi operazione che comporterebbe un numero minore di zero, viene fissata su zero.</span><span class="sxs-lookup"><span data-stu-id="c3f30-186">Any operation that would result in a number less than zero, is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3f30-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3f30-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3f30-188">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c3f30-188">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



