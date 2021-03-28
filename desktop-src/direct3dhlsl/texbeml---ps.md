---
title: texbeml-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake con la correzione della luminanza. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV), una matrice di ambiente Bump 2D e la luminanza.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963408"
---
# <a name="texbeml---ps"></a><span data-ttu-id="efd4b-104">texbeml-PS</span><span class="sxs-lookup"><span data-stu-id="efd4b-104">texbeml - ps</span></span>

<span data-ttu-id="efd4b-105">Applicare una trasformazione della mappa dell'ambiente di Bump Fake con la correzione della luminanza.</span><span class="sxs-lookup"><span data-stu-id="efd4b-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="efd4b-106">Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV), una matrice di ambiente Bump 2D e la luminanza.</span><span class="sxs-lookup"><span data-stu-id="efd4b-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd4b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efd4b-107">Syntax</span></span>



| <span data-ttu-id="efd4b-108">texbeml DST, src</span><span class="sxs-lookup"><span data-stu-id="efd4b-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="efd4b-109">dove</span><span class="sxs-lookup"><span data-stu-id="efd4b-109">where</span></span>

-   <span data-ttu-id="efd4b-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efd4b-110">dst is the destination register.</span></span>
-   <span data-ttu-id="efd4b-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="efd4b-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="efd4b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="efd4b-112">Remarks</span></span>



| <span data-ttu-id="efd4b-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="efd4b-113">Pixel shader versions</span></span> | <span data-ttu-id="efd4b-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="efd4b-114">1\_1</span></span> | <span data-ttu-id="efd4b-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="efd4b-115">1\_2</span></span> | <span data-ttu-id="efd4b-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="efd4b-116">1\_3</span></span> | <span data-ttu-id="efd4b-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="efd4b-117">1\_4</span></span> | <span data-ttu-id="efd4b-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efd4b-118">2\_0</span></span> | <span data-ttu-id="efd4b-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="efd4b-119">2\_x</span></span> | <span data-ttu-id="efd4b-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efd4b-120">2\_sw</span></span> | <span data-ttu-id="efd4b-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efd4b-121">3\_0</span></span> | <span data-ttu-id="efd4b-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efd4b-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="efd4b-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="efd4b-123">texbeml</span></span>               | <span data-ttu-id="efd4b-124">x</span><span class="sxs-lookup"><span data-stu-id="efd4b-124">x</span></span>    | <span data-ttu-id="efd4b-125">x</span><span class="sxs-lookup"><span data-stu-id="efd4b-125">x</span></span>    | <span data-ttu-id="efd4b-126">x</span><span class="sxs-lookup"><span data-stu-id="efd4b-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="efd4b-127">I dati di colore rosso e verde nel registro src vengono interpretati come dati di perturbazione (du, DV).</span><span class="sxs-lookup"><span data-stu-id="efd4b-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="efd4b-128">I dati di colore blu nel registro src vengono interpretati come dati di luminanza.</span><span class="sxs-lookup"><span data-stu-id="efd4b-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="efd4b-129">Questa istruzione trasforma i componenti rosso e verde nel registro di origine usando la matrice di mapping dell'ambiente Bump 2D.</span><span class="sxs-lookup"><span data-stu-id="efd4b-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="efd4b-130">Il risultato viene aggiunto al set di coordinate di trama corrispondente al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efd4b-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="efd4b-131">Viene applicata una correzione della luminanza usando il valore della luminanza e i valori della fase della trama di distorsione.</span><span class="sxs-lookup"><span data-stu-id="efd4b-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="efd4b-132">Il risultato viene usato per campionare la fase di trama corrente.</span><span class="sxs-lookup"><span data-stu-id="efd4b-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="efd4b-133">Questa operazione può essere usata per diverse tecniche in base alla turbativa degli indirizzi, ad esempio il mapping di un ambiente per singolo pixel.</span><span class="sxs-lookup"><span data-stu-id="efd4b-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="efd4b-134">Questa operazione interpreta sempre du e DV come quantità con segno.</span><span class="sxs-lookup"><span data-stu-id="efd4b-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="efd4b-135">Per le versioni 1 \_ 0 e 1 \_ 1, il modificatore di input con [segno di ridimensionamento del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) non è consentito nell'argomento di input.</span><span class="sxs-lookup"><span data-stu-id="efd4b-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="efd4b-136">Questa istruzione genera risultati definiti quando le trame di input contengono dati in formato misto.</span><span class="sxs-lookup"><span data-stu-id="efd4b-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="efd4b-137">Per ulteriori informazioni sui formati di superficie, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="efd4b-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="efd4b-138">In questo esempio vengono illustrati i calcoli eseguiti nell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="efd4b-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="efd4b-139">u ' = TextureCoordinates (fase m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="efd4b-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="efd4b-140">D3DTSS \_ BUMPENVMAT00 (fase m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="efd4b-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="efd4b-141">D3DTSS \_ BUMPENVMAT10 (fase m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="efd4b-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="efd4b-142">v'= TextureCoordinates (fase m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="efd4b-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="efd4b-143">D3DTSS \_ BUMPENVMAT01 (fase m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="efd4b-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="efd4b-144">D3DTSS \_ BUMPENVMAT11 (fase m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="efd4b-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="efd4b-145">t (m)<sub>RGBA</sub> = TextureSample (fase m) con (u ', v') come coordinate</span><span class="sxs-lookup"><span data-stu-id="efd4b-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="efd4b-146">t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="efd4b-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="efd4b-147">\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (fase m)) +</span><span class="sxs-lookup"><span data-stu-id="efd4b-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="efd4b-148">D3DTSS \_ BUMPENVLOFFSET (fase m)\]</span><span class="sxs-lookup"><span data-stu-id="efd4b-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="efd4b-149">I dati che sono stati letti da un'istruzione [texbem](texbem---ps.md) o texbeml non possono essere letti in un secondo momento, ad eccezione di un altro texbem o texbeml.</span><span class="sxs-lookup"><span data-stu-id="efd4b-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="efd4b-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="efd4b-150">Examples</span></span>

<span data-ttu-id="efd4b-151">Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="efd4b-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="efd4b-152">Questo esempio richiede le seguenti trame nelle fasi di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="efd4b-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="efd4b-153">Alla fase 0 viene assegnata una mappa Bump con i dati di perturbazione (du, DV).</span><span class="sxs-lookup"><span data-stu-id="efd4b-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="efd4b-154">Alla fase 1 viene assegnata una mappa di trama con dati di colore.</span><span class="sxs-lookup"><span data-stu-id="efd4b-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="efd4b-155">texbeml imposta i dati della matrice nella fase di trama campionata.</span><span class="sxs-lookup"><span data-stu-id="efd4b-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="efd4b-156">Si tratta di una differenza rispetto alla funzionalità della pipeline della funzione fissa in cui i dati di perturbazione e le matrici occupano la stessa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="efd4b-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efd4b-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efd4b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efd4b-158">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="efd4b-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 