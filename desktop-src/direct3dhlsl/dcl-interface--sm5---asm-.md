---
title: dcl_interface (SM5-ASM)
description: Dichiarare i puntatori a tabella di funzione (interfacce). | dcl_interface (SM5-ASM)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995432"
---
# <a name="dcl_interface-sm5---asm"></a><span data-ttu-id="813ab-104">\_interfaccia DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="813ab-104">dcl\_interface (sm5 - asm)</span></span>

<span data-ttu-id="813ab-105">Dichiarare i puntatori a tabella di funzione (interfacce).</span><span class="sxs-lookup"><span data-stu-id="813ab-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="813ab-106">\_interfaccia DCL FP \# \[ arraySize \] \[ numCallSites \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="813ab-106">dcl\_interface fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="813ab-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="813ab-107">Item</span></span>                                                          | <span data-ttu-id="813ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="813ab-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="813ab-109"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="813ab-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="813ab-110">\[nei \] puntatori della tabella di funzioni.</span><span class="sxs-lookup"><span data-stu-id="813ab-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="813ab-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="813ab-111">Remarks</span></span>

<span data-ttu-id="813ab-112">Ogni interfaccia deve essere associata dall'API prima che lo shader sia utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="813ab-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="813ab-113">Il binding fornisce un riferimento a una delle tabelle di funzioni in modo che sia possibile compilare gli slot del metodo.</span><span class="sxs-lookup"><span data-stu-id="813ab-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="813ab-114">Il compilatore non genererà i puntatori per gli oggetti senza riferimenti.</span><span class="sxs-lookup"><span data-stu-id="813ab-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="813ab-115">Un puntatore a tabella di funzione dispone di un set completo di slot del metodo per evitare il livello aggiuntivo di riferimento indiretto che una rappresentazione da puntatore a puntatore a vtable di C++ richiederebbe.</span><span class="sxs-lookup"><span data-stu-id="813ab-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="813ab-116">Questa operazione richiede anche che i puntatori siano di 5 tuple.</span><span class="sxs-lookup"><span data-stu-id="813ab-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="813ab-117">Nel modello di incorporamento virtuale HLSL è sempre noto quale variabile/input globale viene usato per una chiamata, in modo da poter configurare le tabelle per ogni oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="813ab-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="813ab-118">Le dichiarazioni di puntatore a funzione indicano quali tabelle di funzioni sono valide da usare con loro.</span><span class="sxs-lookup"><span data-stu-id="813ab-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="813ab-119">Ciò consente anche la derivazione delle informazioni sulla correlazione dei metodi.</span><span class="sxs-lookup"><span data-stu-id="813ab-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="813ab-120">Il primo \[ \] di una dichiarazione di interfaccia è la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="813ab-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="813ab-121">Se si utilizza l'indicizzazione dinamica, la dichiarazione indicherà che, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="813ab-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="813ab-122">Una matrice di puntatori di interfaccia può essere indicizzata anche in modo statico, ma non è necessario che le matrici di puntatori di interfaccia significhino l'indicizzazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="813ab-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="813ab-123">Il numero di puntatori a interfaccia inizia da 0 per la prima dichiarazione e successivamente prende in considerazione la dimensione della matrice, quindi il primo puntatore dopo una matrice di quattro voci FP0 \[ 4 \] \[ 1 \] è 4PQ \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="813ab-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="813ab-124">Il secondo \[ \] di una dichiarazione di interfaccia è il numero di siti di chiamata, che deve corrispondere al numero di corpi in ogni tabella a cui viene fatto riferimento nella dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="813ab-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="813ab-125">Non sono previsti limiti per il numero di scelte della tabella function (ft \# ) che possono essere elencate in una dichiarazione di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="813ab-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="813ab-126">Una determinata tabella di funzioni (ft \# ) può comparire più di una volta in una o più dichiarazioni di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="813ab-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="813ab-127">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="813ab-127">Restrictions</span></span>

-   <span data-ttu-id="813ab-128">Il numero di siti degli oggetti in uno shader, ovvero la somma in tutte le *dichiarazioni \# FP* delle \[ \] dichiarazioni arraySize, non deve essere superiore a 253.</span><span class="sxs-lookup"><span data-stu-id="813ab-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="813ab-129">Questo numero corrisponde al numero di **puntatori** che possono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="813ab-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="813ab-130">Il Runtime impone questo limite di 253 per limitare le dimensioni dell'interfaccia DDI per la comunicazione di questi dati del puntatore.</span><span class="sxs-lookup"><span data-stu-id="813ab-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="813ab-131">Il numero di siti di chiamata in uno shader, ovvero la somma in tutte le istruzioni fcall del numero di potenziali destinazioni dei rami, non deve superare 4096.</span><span class="sxs-lookup"><span data-stu-id="813ab-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="813ab-132">Ad esempio, un [fcall](fcall--sm5---asm-.md) che utilizza un indice statico per la prima *dimensione \[ \] \[ \] FP* viene conteggiato come uno:</span><span class="sxs-lookup"><span data-stu-id="813ab-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="813ab-133">Un **fcall** che utilizza un indice dinamico viene conteggiato come numero di elementi nella matrice (prima \[ \] dell' **\_ interfaccia DCL**):</span><span class="sxs-lookup"><span data-stu-id="813ab-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="813ab-134">Questo limite consente ad alcune implementazioni di adattare facilmente le tabelle delle selezioni del corpo della funzione in un archivio costante di tipo buffer.</span><span class="sxs-lookup"><span data-stu-id="813ab-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="813ab-135">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="813ab-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="813ab-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="813ab-136">Vertex</span></span> | <span data-ttu-id="813ab-137">Hull</span><span class="sxs-lookup"><span data-stu-id="813ab-137">Hull</span></span> | <span data-ttu-id="813ab-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="813ab-138">Domain</span></span> | <span data-ttu-id="813ab-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="813ab-139">Geometry</span></span> | <span data-ttu-id="813ab-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="813ab-140">Pixel</span></span> | <span data-ttu-id="813ab-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="813ab-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="813ab-142">X</span><span class="sxs-lookup"><span data-stu-id="813ab-142">X</span></span>      | <span data-ttu-id="813ab-143">X</span><span class="sxs-lookup"><span data-stu-id="813ab-143">X</span></span>    | <span data-ttu-id="813ab-144">X</span><span class="sxs-lookup"><span data-stu-id="813ab-144">X</span></span>      | <span data-ttu-id="813ab-145">X</span><span class="sxs-lookup"><span data-stu-id="813ab-145">X</span></span>        | <span data-ttu-id="813ab-146">X</span><span class="sxs-lookup"><span data-stu-id="813ab-146">X</span></span>     | <span data-ttu-id="813ab-147">X</span><span class="sxs-lookup"><span data-stu-id="813ab-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="813ab-148">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="813ab-148">Minimum Shader Model</span></span>

<span data-ttu-id="813ab-149">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="813ab-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="813ab-150">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="813ab-150">Shader Model</span></span>                                              | <span data-ttu-id="813ab-151">Supportato</span><span class="sxs-lookup"><span data-stu-id="813ab-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="813ab-152">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="813ab-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="813ab-153">sì</span><span class="sxs-lookup"><span data-stu-id="813ab-153">yes</span></span>       |
| [<span data-ttu-id="813ab-154">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="813ab-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="813ab-155">no</span><span class="sxs-lookup"><span data-stu-id="813ab-155">no</span></span>        |
| [<span data-ttu-id="813ab-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="813ab-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="813ab-157">no</span><span class="sxs-lookup"><span data-stu-id="813ab-157">no</span></span>        |
| [<span data-ttu-id="813ab-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="813ab-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="813ab-159">no</span><span class="sxs-lookup"><span data-stu-id="813ab-159">no</span></span>        |
| [<span data-ttu-id="813ab-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="813ab-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="813ab-161">no</span><span class="sxs-lookup"><span data-stu-id="813ab-161">no</span></span>        |
| [<span data-ttu-id="813ab-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="813ab-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="813ab-163">no</span><span class="sxs-lookup"><span data-stu-id="813ab-163">no</span></span>        |



 

<span data-ttu-id="813ab-164">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="813ab-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="813ab-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="813ab-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="813ab-166">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="813ab-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





