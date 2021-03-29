---
title: texld-ps_1_4
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati utilizzando il contenuto del registro di origine come coordinate di trama. La trama campionata è la trama associata al numero di registro di destinazione.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993144"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="30eed-104">texld-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="30eed-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="30eed-105">Carica il registro di destinazione con i dati di colore (RGBA) campionati utilizzando il contenuto del registro di origine come coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="30eed-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="30eed-106">La trama campionata è la trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="30eed-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="30eed-107">texld DST, src</span><span class="sxs-lookup"><span data-stu-id="30eed-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="30eed-108">Registri</span><span class="sxs-lookup"><span data-stu-id="30eed-108">Registers</span></span>



| <span data-ttu-id="30eed-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="30eed-109">Argument</span></span> | <span data-ttu-id="30eed-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30eed-110">Description</span></span>          | <span data-ttu-id="30eed-111">Registri</span><span class="sxs-lookup"><span data-stu-id="30eed-111">Registers</span></span> |     |     |     | <span data-ttu-id="30eed-112">Versione</span><span class="sxs-lookup"><span data-stu-id="30eed-112">Version</span></span>      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | <span data-ttu-id="30eed-113">VN</span><span class="sxs-lookup"><span data-stu-id="30eed-113">vₙ</span></span>        | <span data-ttu-id="30eed-114">CN</span><span class="sxs-lookup"><span data-stu-id="30eed-114">cₙ</span></span>  | <span data-ttu-id="30eed-115">TN</span><span class="sxs-lookup"><span data-stu-id="30eed-115">tₙ</span></span>  | <span data-ttu-id="30eed-116">RN</span><span class="sxs-lookup"><span data-stu-id="30eed-116">rₙ</span></span>  |              |
| <span data-ttu-id="30eed-117">DST</span><span class="sxs-lookup"><span data-stu-id="30eed-117">dst</span></span>      | <span data-ttu-id="30eed-118">Registro destinazione</span><span class="sxs-lookup"><span data-stu-id="30eed-118">Destination register</span></span> |           |     |     | <span data-ttu-id="30eed-119">x</span><span class="sxs-lookup"><span data-stu-id="30eed-119">x</span></span>   | <span data-ttu-id="30eed-120">1\_4</span><span class="sxs-lookup"><span data-stu-id="30eed-120">1\_4</span></span>         |
| <span data-ttu-id="30eed-121">src</span><span class="sxs-lookup"><span data-stu-id="30eed-121">src</span></span>      | <span data-ttu-id="30eed-122">Registro di origine</span><span class="sxs-lookup"><span data-stu-id="30eed-122">Source register</span></span>      |           |     | <span data-ttu-id="30eed-123">x</span><span class="sxs-lookup"><span data-stu-id="30eed-123">x</span></span>   |     | <span data-ttu-id="30eed-124">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="30eed-124">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="30eed-125">x</span><span class="sxs-lookup"><span data-stu-id="30eed-125">x</span></span>   | <span data-ttu-id="30eed-126">x</span><span class="sxs-lookup"><span data-stu-id="30eed-126">x</span></span>   | <span data-ttu-id="30eed-127">1 \_ fase 4</span><span class="sxs-lookup"><span data-stu-id="30eed-127">1\_4 phase</span></span>   |



 

<span data-ttu-id="30eed-128">Quando si usa r (n) come registro di origine, è necessario inizializzare i primi tre componenti (XYZ) nella fase precedente dello shader.</span><span class="sxs-lookup"><span data-stu-id="30eed-128">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="30eed-129">Per ulteriori informazioni sui registri, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="30eed-129">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30eed-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="30eed-130">Remarks</span></span>

<span data-ttu-id="30eed-131">Questa istruzione esegue il campionamento della trama nella fase della trama associata al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="30eed-131">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="30eed-132">La trama viene campionata usando i dati delle coordinate di trama del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="30eed-132">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="30eed-133">La sintassi per le istruzioni texld e texcrd espone il supporto per una divisione proiettiva con un modificatore di registro di trama.</span><span class="sxs-lookup"><span data-stu-id="30eed-133">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="30eed-134">Per pixel shader versione 1,4, il \_ flag di trasformazione trama D3DTTFF proiettato viene sempre ignorato.</span><span class="sxs-lookup"><span data-stu-id="30eed-134">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="30eed-135">Regole per l'uso di texld:</span><span class="sxs-lookup"><span data-stu-id="30eed-135">Rules for using texld:</span></span>

1.  <span data-ttu-id="30eed-136">Lo stesso modificatore. xyz o. XYW deve essere applicato a ogni lettura di un singolo registro t (n) nelle istruzioni texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="30eed-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="30eed-137">Se viene usato. XYW nelle letture del registro t (n), questo può essere misto con altre letture dello stesso registro t (n) con. XYW \_ DW.</span><span class="sxs-lookup"><span data-stu-id="30eed-137">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="30eed-138">Il \_ modificatore di origine DZ è valido solo in texld con il registro di origine r (n) (solo in questo caso la fase 2).</span><span class="sxs-lookup"><span data-stu-id="30eed-138">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="30eed-139">Il \_ modificatore di origine DZ può essere usato non più di due volte per shader.</span><span class="sxs-lookup"><span data-stu-id="30eed-139">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="30eed-140">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="30eed-140">Pixel shader versions</span></span> | <span data-ttu-id="30eed-141">1\_1</span><span class="sxs-lookup"><span data-stu-id="30eed-141">1\_1</span></span> | <span data-ttu-id="30eed-142">1\_2</span><span class="sxs-lookup"><span data-stu-id="30eed-142">1\_2</span></span> | <span data-ttu-id="30eed-143">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="30eed-143">1\_3</span></span> | <span data-ttu-id="30eed-144">1\_4</span><span class="sxs-lookup"><span data-stu-id="30eed-144">1\_4</span></span> | <span data-ttu-id="30eed-145">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30eed-145">2\_0</span></span> | <span data-ttu-id="30eed-146">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="30eed-146">2\_x</span></span> | <span data-ttu-id="30eed-147">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30eed-147">2\_sw</span></span> | <span data-ttu-id="30eed-148">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30eed-148">3\_0</span></span> | <span data-ttu-id="30eed-149">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30eed-149">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="30eed-150">texld</span><span class="sxs-lookup"><span data-stu-id="30eed-150">texld</span></span>                 |      |      |      | <span data-ttu-id="30eed-151">x</span><span class="sxs-lookup"><span data-stu-id="30eed-151">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="30eed-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="30eed-152">Examples</span></span>

<span data-ttu-id="30eed-153">L'istruzione texld offre un certo controllo sui componenti utilizzati per i dati delle coordinate di trama di origine.</span><span class="sxs-lookup"><span data-stu-id="30eed-153">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="30eed-154">Segue il set completo di sintassi consentita per texld e include tutti i modificatori del registro di origine, i selettori e le combinazioni di maschere di scrittura validi.</span><span class="sxs-lookup"><span data-stu-id="30eed-154">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="30eed-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30eed-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30eed-156">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="30eed-156">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




