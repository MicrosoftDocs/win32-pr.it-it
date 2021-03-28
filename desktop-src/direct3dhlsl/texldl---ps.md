---
title: texldl-PS
description: Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981138"
---
# <a name="texldl---ps"></a><span data-ttu-id="5d418-105">texldl-PS</span><span class="sxs-lookup"><span data-stu-id="5d418-105">texldl - ps</span></span>

<span data-ttu-id="5d418-106">Campionare una trama con un campionatore specifico.</span><span class="sxs-lookup"><span data-stu-id="5d418-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="5d418-107">Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="5d418-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d418-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d418-108">Syntax</span></span>



| <span data-ttu-id="5d418-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5d418-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="5d418-110">Dove:</span><span class="sxs-lookup"><span data-stu-id="5d418-110">Where:</span></span>

-   <span data-ttu-id="5d418-111">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d418-111">dst is a destination register.</span></span>
-   <span data-ttu-id="5d418-112">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="5d418-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="5d418-113">Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="5d418-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="5d418-114">src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="5d418-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="5d418-115">Il campionatore è associato a una trama e a uno stato di controllo definiti dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (ad esempio, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="5d418-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d418-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d418-116">Remarks</span></span>



| <span data-ttu-id="5d418-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="5d418-117">Pixel shader versions</span></span> | <span data-ttu-id="5d418-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="5d418-118">1\_1</span></span> | <span data-ttu-id="5d418-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="5d418-119">1\_2</span></span> | <span data-ttu-id="5d418-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5d418-120">1\_3</span></span> | <span data-ttu-id="5d418-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="5d418-121">1\_4</span></span> | <span data-ttu-id="5d418-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5d418-122">2\_0</span></span> | <span data-ttu-id="5d418-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5d418-123">2\_x</span></span> | <span data-ttu-id="5d418-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5d418-124">2\_sw</span></span> | <span data-ttu-id="5d418-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5d418-125">3\_0</span></span> | <span data-ttu-id="5d418-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5d418-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5d418-127">texldl</span><span class="sxs-lookup"><span data-stu-id="5d418-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="5d418-128">x</span><span class="sxs-lookup"><span data-stu-id="5d418-128">x</span></span>    | <span data-ttu-id="5d418-129">x</span><span class="sxs-lookup"><span data-stu-id="5d418-129">x</span></span>     |



 

<span data-ttu-id="5d418-130">texldl Cerca il set di trame nella fase del campionatore a cui fa riferimento src1.</span><span class="sxs-lookup"><span data-stu-id="5d418-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="5d418-131">Il livello di dettaglio è selezionato da src0. w.</span><span class="sxs-lookup"><span data-stu-id="5d418-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="5d418-132">Questo valore può essere negativo, nel qual caso il livello di dettaglio selezionato è zero One (mapping più grande) con il MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="5d418-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="5d418-133">Poiché src0. w è un valore a virgola mobile, il valore frazionario viene usato per interpolare (se MIPFILTER è lineare) tra due livelli MIP.</span><span class="sxs-lookup"><span data-stu-id="5d418-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="5d418-134">Gli Stati del campionatore MIPMAPLODBIAS e MAXMIPLEVEL vengono rispettati.</span><span class="sxs-lookup"><span data-stu-id="5d418-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="5d418-135">Per ulteriori informazioni sugli Stati del campionatore, vedere [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="5d418-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="5d418-136">Se uno shader esegue un campionamento di un campionatore che non dispone di un set di trame, viene ottenuto il valore 0001 nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d418-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="5d418-137">Di seguito è riportato un algoritmo approssimativo che il dispositivo di riferimento segue:</span><span class="sxs-lookup"><span data-stu-id="5d418-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="5d418-138">Restrizioni:</span><span class="sxs-lookup"><span data-stu-id="5d418-138">Restrictions:</span></span>

-   <span data-ttu-id="5d418-139">Le coordinate di trama non devono essere ridimensionate in base alle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="5d418-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="5d418-140">DST deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="5d418-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="5d418-141">DST può accettare un writemask.</span><span class="sxs-lookup"><span data-stu-id="5d418-141">dst can accept a writemask.</span></span> <span data-ttu-id="5d418-142">Vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="5d418-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="5d418-143">Le impostazioni predefinite per i componenti mancanti sono 0 o 1 e dipendono dal formato di trama.</span><span class="sxs-lookup"><span data-stu-id="5d418-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="5d418-144">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="5d418-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="5d418-145">src1 non può usare un modificatore negazioni (vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="5d418-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="5d418-146">src1 può usare swizzle (vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), che viene applicato dopo il campionamento, ma prima che venga rispettata la maschera di scrittura (vedere la maschera di scrittura del registro di destinazione).</span><span class="sxs-lookup"><span data-stu-id="5d418-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="5d418-147">Il campionatore deve essere stato dichiarato (usando [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) all'inizio dello shader.</span><span class="sxs-lookup"><span data-stu-id="5d418-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="5d418-148">Il numero di coordinate necessarie per eseguire l'esempio di trama dipende dalla modalità di dichiarazione del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5d418-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="5d418-149">Se è stata dichiarata come cubo, è richiesta una coordinata di trama a tre componenti (. RGB).</span><span class="sxs-lookup"><span data-stu-id="5d418-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="5d418-150">La convalida impone che le coordinate fornite a Tex \_ LDL siano sufficienti per la dimensione di trama dichiarata per il campionatore.</span><span class="sxs-lookup"><span data-stu-id="5d418-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="5d418-151">Tuttavia, non è garantito che l'applicazione imposti effettivamente una trama (tramite l'API) con dimensioni uguali alla dimensione dichiarata per il campionatore.</span><span class="sxs-lookup"><span data-stu-id="5d418-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="5d418-152">In tal caso, il runtime tenterà di rilevare le mancate corrispondenze (probabilmente solo in fase di debug).</span><span class="sxs-lookup"><span data-stu-id="5d418-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="5d418-153">Il campionamento di una trama con un minor numero di dimensioni rispetto a quelli presenti nella coordinata di trama sarà consentito e dovrebbe ignorare i componenti della coordinata trama aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="5d418-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="5d418-154">Viceversa, il campionamento di una trama con più dimensioni rispetto a quelle presenti nella coordinata di trama non è valido.</span><span class="sxs-lookup"><span data-stu-id="5d418-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="5d418-155">Se il src0 (coordinata di trama) è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md), è necessario che i componenti necessari per la ricerca (descritti in precedenza) siano stati precedentemente scritti.</span><span class="sxs-lookup"><span data-stu-id="5d418-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="5d418-156">Il campionamento di trame RGB senza segno comporterà valori float compresi tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="5d418-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="5d418-157">Il campionamento delle trame con segno comporterà valori float compresi tra-1,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="5d418-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="5d418-158">Quando si campionano trame a virgola mobile, Float16 significa che i dati variano entro il numero massimo di \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="5d418-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="5d418-159">Float32 indica che verrà utilizzato l'intervallo massimo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d418-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="5d418-160">Il campionamento esterno a uno dei due intervalli non è definito.</span><span class="sxs-lookup"><span data-stu-id="5d418-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="5d418-161">Nessun limite di lettura dipendente.</span><span class="sxs-lookup"><span data-stu-id="5d418-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d418-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d418-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d418-163">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="5d418-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
