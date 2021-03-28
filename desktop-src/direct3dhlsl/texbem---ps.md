---
title: texbem-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV) e una matrice di ambiente urto 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976695"
---
# <a name="texbem---ps"></a><span data-ttu-id="0fdce-104">texbem-PS</span><span class="sxs-lookup"><span data-stu-id="0fdce-104">texbem - ps</span></span>

<span data-ttu-id="0fdce-105">Applicare una trasformazione della mappa dell'ambiente di Bump Fake.</span><span class="sxs-lookup"><span data-stu-id="0fdce-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="0fdce-106">Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV) e una matrice di ambiente urto 2D.</span><span class="sxs-lookup"><span data-stu-id="0fdce-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fdce-107">Syntax</span></span>



| <span data-ttu-id="0fdce-108">texbem DST, src</span><span class="sxs-lookup"><span data-stu-id="0fdce-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="0fdce-109">dove</span><span class="sxs-lookup"><span data-stu-id="0fdce-109">where</span></span>

-   <span data-ttu-id="0fdce-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0fdce-110">dst is the destination register.</span></span>
-   <span data-ttu-id="0fdce-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="0fdce-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fdce-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fdce-112">Remarks</span></span>



| <span data-ttu-id="0fdce-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0fdce-113">Pixel shader versions</span></span> | <span data-ttu-id="0fdce-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0fdce-114">1\_1</span></span> | <span data-ttu-id="0fdce-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0fdce-115">1\_2</span></span> | <span data-ttu-id="0fdce-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0fdce-116">1\_3</span></span> | <span data-ttu-id="0fdce-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0fdce-117">1\_4</span></span> | <span data-ttu-id="0fdce-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fdce-118">2\_0</span></span> | <span data-ttu-id="0fdce-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0fdce-119">2\_x</span></span> | <span data-ttu-id="0fdce-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0fdce-120">2\_sw</span></span> | <span data-ttu-id="0fdce-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fdce-121">3\_0</span></span> | <span data-ttu-id="0fdce-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0fdce-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0fdce-123">texbem</span><span class="sxs-lookup"><span data-stu-id="0fdce-123">texbem</span></span>                | <span data-ttu-id="0fdce-124">x</span><span class="sxs-lookup"><span data-stu-id="0fdce-124">x</span></span>    | <span data-ttu-id="0fdce-125">x</span><span class="sxs-lookup"><span data-stu-id="0fdce-125">x</span></span>    | <span data-ttu-id="0fdce-126">x</span><span class="sxs-lookup"><span data-stu-id="0fdce-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0fdce-127">I dati di colore rosso e verde nel registro src vengono interpretati come dati di perturbazione (du, DV).</span><span class="sxs-lookup"><span data-stu-id="0fdce-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="0fdce-128">Questa istruzione trasforma i componenti rossi e verdi nel registro di origine usando la matrice di mapping dell'ambiente Bump 2D.</span><span class="sxs-lookup"><span data-stu-id="0fdce-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="0fdce-129">Il risultato viene aggiunto al set di coordinate di trama corrispondente al numero di registro di destinazione e viene usato per campionare la fase di trama corrente.</span><span class="sxs-lookup"><span data-stu-id="0fdce-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="0fdce-130">Questa operazione interpreta sempre du e DV come quantità con segno.</span><span class="sxs-lookup"><span data-stu-id="0fdce-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="0fdce-131">Per le versioni 1 \_ 0 e 1 \_ 1, il modificatore di input con [segno di ridimensionamento del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) non è consentito nell'argomento di input.</span><span class="sxs-lookup"><span data-stu-id="0fdce-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="0fdce-132">Questa istruzione genera risultati definiti quando le trame di input contengono dati in formato firmato.</span><span class="sxs-lookup"><span data-stu-id="0fdce-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="0fdce-133">I dati in formato misto funzionano solo se i primi due canali contengono dati firmati.</span><span class="sxs-lookup"><span data-stu-id="0fdce-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="0fdce-134">Per ulteriori informazioni sui formati di superficie, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="0fdce-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="0fdce-135">Questo può essere usato per diverse tecniche in base alla turbativa degli indirizzi, tra cui il mapping dell'ambiente per pixel Fake e l'illuminazione diffusa (bump mapping).</span><span class="sxs-lookup"><span data-stu-id="0fdce-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="0fdce-136">Quando si utilizza questa istruzione, i registri di trama devono seguire la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="0fdce-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="0fdce-137">I calcoli eseguiti nell'istruzione sono riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="0fdce-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="0fdce-138">u ' = TextureCoordinates (fase m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (fase m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (fase m) \* t (n)<sub>g</sub> v'= TextureCoordinates (fase m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (fase m) \* t (n)<sub>r</sub> + D3DTSS \_ BUMPENVMAT11 (fase m) \* t (n)<sub>g</sub> t (m)<sub>RGBA</sub> = TextureSample (fase m)</span><span class="sxs-lookup"><span data-stu-id="0fdce-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="0fdce-139">uso di (u ', v') come coordinate</span><span class="sxs-lookup"><span data-stu-id="0fdce-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="0fdce-140">Registrare i dati letti da un'istruzione texbem-PS o [texbeml-PS](texbeml---ps.md) non possono essere letti in un secondo momento, ad eccezione di un altro texbem-PS o texbeml-PS.</span><span class="sxs-lookup"><span data-stu-id="0fdce-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="0fdce-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="0fdce-141">Examples</span></span>

<span data-ttu-id="0fdce-142">Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="0fdce-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="0fdce-143">texbem richiede le seguenti trame nelle fasi di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="0fdce-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="0fdce-144">Alla fase 0 viene assegnata una mappa Bump con i dati di perturbazione (du, DV).</span><span class="sxs-lookup"><span data-stu-id="0fdce-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="0fdce-145">La fase 1 USA una mappa di trama con dati di colore.</span><span class="sxs-lookup"><span data-stu-id="0fdce-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="0fdce-146">Questa istruzione imposta i dati della matrice nella fase di trama campionata.</span><span class="sxs-lookup"><span data-stu-id="0fdce-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="0fdce-147">Si tratta di una differenza rispetto alla funzionalità della pipeline della funzione fissa in cui i dati di perturbazione e le matrici occupano la stessa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="0fdce-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fdce-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fdce-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fdce-149">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0fdce-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 