---
title: texld - ps_1_4
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate della trama. La trama campionata è la trama associata al numero di registro di destinazione.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996868"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="09bd5-104">texld - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="09bd5-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="09bd5-105">Carica il registro di destinazione con i dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="09bd5-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="09bd5-106">La trama campionata è la trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09bd5-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="09bd5-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="09bd5-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="09bd5-108">Registri</span><span class="sxs-lookup"><span data-stu-id="09bd5-108">Registers</span></span>



|          |                      | <span data-ttu-id="09bd5-109">Vn</span><span class="sxs-lookup"><span data-stu-id="09bd5-109">vₙ</span></span>        | <span data-ttu-id="09bd5-110">Cn</span><span class="sxs-lookup"><span data-stu-id="09bd5-110">cₙ</span></span>  | <span data-ttu-id="09bd5-111">Tn</span><span class="sxs-lookup"><span data-stu-id="09bd5-111">tₙ</span></span>  | <span data-ttu-id="09bd5-112">Rn</span><span class="sxs-lookup"><span data-stu-id="09bd5-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="09bd5-113">Dst</span><span class="sxs-lookup"><span data-stu-id="09bd5-113">dst</span></span>      | <span data-ttu-id="09bd5-114">Registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="09bd5-114">Destination register</span></span> |           |     |     | <span data-ttu-id="09bd5-115">x</span><span class="sxs-lookup"><span data-stu-id="09bd5-115">x</span></span>   | <span data-ttu-id="09bd5-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="09bd5-116">1\_4</span></span>         |
| <span data-ttu-id="09bd5-117">src</span><span class="sxs-lookup"><span data-stu-id="09bd5-117">src</span></span>      | <span data-ttu-id="09bd5-118">Registro di origine</span><span class="sxs-lookup"><span data-stu-id="09bd5-118">Source register</span></span>      |           |     | <span data-ttu-id="09bd5-119">x</span><span class="sxs-lookup"><span data-stu-id="09bd5-119">x</span></span>   |     | <span data-ttu-id="09bd5-120">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="09bd5-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="09bd5-121">x</span><span class="sxs-lookup"><span data-stu-id="09bd5-121">x</span></span>   | <span data-ttu-id="09bd5-122">x</span><span class="sxs-lookup"><span data-stu-id="09bd5-122">x</span></span>   | <span data-ttu-id="09bd5-123">1 \_ 4 fase</span><span class="sxs-lookup"><span data-stu-id="09bd5-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="09bd5-124">Quando si usa r(n) come registro di origine, i primi tre componenti (XYZ) devono essere stati inizializzati nella fase precedente dello shader.</span><span class="sxs-lookup"><span data-stu-id="09bd5-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="09bd5-125">Per altre informazioni sui registri, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="09bd5-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09bd5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="09bd5-126">Remarks</span></span>

<span data-ttu-id="09bd5-127">Questa istruzione campio la trama nella fase della trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09bd5-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="09bd5-128">La trama viene campionata usando i dati delle coordinate della trama del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="09bd5-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="09bd5-129">La sintassi per le istruzioni texld e texcrd espone il supporto per una divisione proiettativa con un modificatore del registro trame.</span><span class="sxs-lookup"><span data-stu-id="09bd5-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="09bd5-130">Per pixel shader versione 1.4, il flag di trasformazione della trama PROIETTATA D3DTTFF \_ viene sempre ignorato.</span><span class="sxs-lookup"><span data-stu-id="09bd5-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="09bd5-131">Regole per l'uso di texld:</span><span class="sxs-lookup"><span data-stu-id="09bd5-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="09bd5-132">Lo stesso modificatore .xyz o .xyw deve essere applicato a ogni lettura di un singolo registro t(n) all'interno di istruzioni texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="09bd5-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="09bd5-133">Se .xyw viene usato nelle operazioni di lettura del registro t(n), questa operazione può essere mista ad altre operazioni di lettura dello stesso registro t(n) usando .xyw \_ dw.</span><span class="sxs-lookup"><span data-stu-id="09bd5-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="09bd5-134">Il modificatore dz source è valido solo in texld con registro di origine \_ r(n) (solo fase 2).</span><span class="sxs-lookup"><span data-stu-id="09bd5-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="09bd5-135">Il \_ modificatore dz source può essere usato non più di due volte per ogni shader.</span><span class="sxs-lookup"><span data-stu-id="09bd5-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="09bd5-136">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="09bd5-136">Pixel shader versions</span></span> | <span data-ttu-id="09bd5-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="09bd5-137">1\_1</span></span> | <span data-ttu-id="09bd5-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="09bd5-138">1\_2</span></span> | <span data-ttu-id="09bd5-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="09bd5-139">1\_3</span></span> | <span data-ttu-id="09bd5-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="09bd5-140">1\_4</span></span> | <span data-ttu-id="09bd5-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09bd5-141">2\_0</span></span> | <span data-ttu-id="09bd5-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="09bd5-142">2\_x</span></span> | <span data-ttu-id="09bd5-143">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="09bd5-143">2\_sw</span></span> | <span data-ttu-id="09bd5-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09bd5-144">3\_0</span></span> | <span data-ttu-id="09bd5-145">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="09bd5-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="09bd5-146">texld</span><span class="sxs-lookup"><span data-stu-id="09bd5-146">texld</span></span>                 |      |      |      | <span data-ttu-id="09bd5-147">x</span><span class="sxs-lookup"><span data-stu-id="09bd5-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="09bd5-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="09bd5-148">Examples</span></span>

<span data-ttu-id="09bd5-149">L'istruzione texld offre un certo controllo sui componenti dei dati delle coordinate della trama di origine.</span><span class="sxs-lookup"><span data-stu-id="09bd5-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="09bd5-150">Il set completo di sintassi consentita per texld segue e include tutti i modificatori del registro di origine validi, i selettori e le combinazioni di maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="09bd5-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="09bd5-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09bd5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09bd5-152">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="09bd5-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




