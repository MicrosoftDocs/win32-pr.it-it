---
title: texld - ps_1_4
description: Carica il registro di destinazione con dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate di trama. La trama campionata è la trama associata al numero di registro di destinazione.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118826"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="b0bde-104">texld - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b0bde-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="b0bde-105">Carica il registro di destinazione con dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="b0bde-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="b0bde-106">La trama campionata è la trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b0bde-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="b0bde-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="b0bde-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="b0bde-108">Registri</span><span class="sxs-lookup"><span data-stu-id="b0bde-108">Registers</span></span>



| <span data-ttu-id="b0bde-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b0bde-109">Value</span></span>         | <span data-ttu-id="b0bde-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0bde-110">Description</span></span>                     | <span data-ttu-id="b0bde-111">Vn</span><span class="sxs-lookup"><span data-stu-id="b0bde-111">vₙ</span></span>        | <span data-ttu-id="b0bde-112">Cn</span><span class="sxs-lookup"><span data-stu-id="b0bde-112">cₙ</span></span>  | <span data-ttu-id="b0bde-113">Tn</span><span class="sxs-lookup"><span data-stu-id="b0bde-113">tₙ</span></span>  | <span data-ttu-id="b0bde-114">Rn</span><span class="sxs-lookup"><span data-stu-id="b0bde-114">rₙ</span></span>  | <span data-ttu-id="b0bde-115">Versione pixel shader</span><span class="sxs-lookup"><span data-stu-id="b0bde-115">Pixel shader version</span></span>              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="b0bde-116">Dst</span><span class="sxs-lookup"><span data-stu-id="b0bde-116">dst</span></span>      | <span data-ttu-id="b0bde-117">Registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="b0bde-117">Destination register</span></span> |           |     |     | <span data-ttu-id="b0bde-118">x</span><span class="sxs-lookup"><span data-stu-id="b0bde-118">x</span></span>   | <span data-ttu-id="b0bde-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0bde-119">1\_4</span></span>         |
| <span data-ttu-id="b0bde-120">src</span><span class="sxs-lookup"><span data-stu-id="b0bde-120">src</span></span>      | <span data-ttu-id="b0bde-121">Registro di origine</span><span class="sxs-lookup"><span data-stu-id="b0bde-121">Source register</span></span>      |           |     | <span data-ttu-id="b0bde-122">x</span><span class="sxs-lookup"><span data-stu-id="b0bde-122">x</span></span>   |     | <span data-ttu-id="b0bde-123">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="b0bde-123">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="b0bde-124">x</span><span class="sxs-lookup"><span data-stu-id="b0bde-124">x</span></span>   | <span data-ttu-id="b0bde-125">x</span><span class="sxs-lookup"><span data-stu-id="b0bde-125">x</span></span>   | <span data-ttu-id="b0bde-126">1 \_ 4 fase</span><span class="sxs-lookup"><span data-stu-id="b0bde-126">1\_4 phase</span></span>   |



 

<span data-ttu-id="b0bde-127">Quando si usa r(n) come registro di origine, i primi tre componenti (XYZ) devono essere stati inizializzati nella fase precedente dello shader.</span><span class="sxs-lookup"><span data-stu-id="b0bde-127">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="b0bde-128">Per altre informazioni sui registri, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="b0bde-128">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0bde-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0bde-129">Remarks</span></span>

<span data-ttu-id="b0bde-130">Questa istruzione consente di eseguire il campionamento della trama nella fase di trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b0bde-130">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="b0bde-131">La trama viene campionata usando i dati delle coordinate della trama del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b0bde-131">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="b0bde-132">La sintassi per le istruzioni texld e texcrd espone il supporto per una divisione proiettativa con un modificatore del registro trame.</span><span class="sxs-lookup"><span data-stu-id="b0bde-132">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="b0bde-133">Per pixel shader versione 1.4, il flag di trasformazione della trama PROIETTATA D3DTTFF \_ viene sempre ignorato.</span><span class="sxs-lookup"><span data-stu-id="b0bde-133">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="b0bde-134">Regole per l'uso di texld:</span><span class="sxs-lookup"><span data-stu-id="b0bde-134">Rules for using texld:</span></span>

1.  <span data-ttu-id="b0bde-135">Lo stesso modificatore .xyz o .xyw deve essere applicato a ogni lettura di un singolo registro t(n) all'interno di istruzioni texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="b0bde-135">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="b0bde-136">Se .xyw viene usato nelle operazioni di lettura del registro t(n), questa operazione può essere mista ad altre operazioni di lettura dello stesso registro t(n) usando .xyw \_ dw.</span><span class="sxs-lookup"><span data-stu-id="b0bde-136">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="b0bde-137">Il modificatore dz source è valido solo in texld con registro di origine \_ r(n) (solo fase 2).</span><span class="sxs-lookup"><span data-stu-id="b0bde-137">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="b0bde-138">Il \_ modificatore dz source può essere usato non più di due volte per ogni shader.</span><span class="sxs-lookup"><span data-stu-id="b0bde-138">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="b0bde-139">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="b0bde-139">Pixel shader versions</span></span> | <span data-ttu-id="b0bde-140">1\_1</span><span class="sxs-lookup"><span data-stu-id="b0bde-140">1\_1</span></span> | <span data-ttu-id="b0bde-141">1\_2</span><span class="sxs-lookup"><span data-stu-id="b0bde-141">1\_2</span></span> | <span data-ttu-id="b0bde-142">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0bde-142">1\_3</span></span> | <span data-ttu-id="b0bde-143">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0bde-143">1\_4</span></span> | <span data-ttu-id="b0bde-144">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0bde-144">2\_0</span></span> | <span data-ttu-id="b0bde-145">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b0bde-145">2\_x</span></span> | <span data-ttu-id="b0bde-146">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b0bde-146">2\_sw</span></span> | <span data-ttu-id="b0bde-147">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0bde-147">3\_0</span></span> | <span data-ttu-id="b0bde-148">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b0bde-148">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b0bde-149">texld</span><span class="sxs-lookup"><span data-stu-id="b0bde-149">texld</span></span>                 |      |      |      | <span data-ttu-id="b0bde-150">x</span><span class="sxs-lookup"><span data-stu-id="b0bde-150">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="b0bde-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="b0bde-151">Examples</span></span>

<span data-ttu-id="b0bde-152">L'istruzione texld offre un certo controllo sui componenti dei dati delle coordinate della trama di origine.</span><span class="sxs-lookup"><span data-stu-id="b0bde-152">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="b0bde-153">Il set completo di sintassi consentita per texld segue e include tutti i modificatori del registro di origine validi, i selettori e le combinazioni di maschere di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b0bde-153">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b0bde-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0bde-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0bde-155">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="b0bde-155">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




