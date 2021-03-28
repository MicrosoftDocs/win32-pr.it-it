---
title: texldl-vs
description: Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058520"
---
# <a name="texldl---vs"></a><span data-ttu-id="471a4-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="471a4-105">texldl - vs</span></span>

<span data-ttu-id="471a4-106">Campionare una trama con un campionatore specifico.</span><span class="sxs-lookup"><span data-stu-id="471a4-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="471a4-107">Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="471a4-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="471a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="471a4-108">Syntax</span></span>



| <span data-ttu-id="471a4-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="471a4-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="471a4-110">Dove:</span><span class="sxs-lookup"><span data-stu-id="471a4-110">Where:</span></span>

-   <span data-ttu-id="471a4-111">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="471a4-111">dst is a destination register.</span></span>
-   <span data-ttu-id="471a4-112">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="471a4-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="471a4-113">src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="471a4-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="471a4-114">Il campionatore è associato a una trama e a uno stato di controllo definiti dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (ad esempio, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="471a4-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="471a4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="471a4-115">Remarks</span></span>



| <span data-ttu-id="471a4-116">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="471a4-116">Vertex shader versions</span></span> | <span data-ttu-id="471a4-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="471a4-117">1\_1</span></span> | <span data-ttu-id="471a4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a4-118">2\_0</span></span> | <span data-ttu-id="471a4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="471a4-119">2\_x</span></span> | <span data-ttu-id="471a4-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="471a4-120">2\_sw</span></span> | <span data-ttu-id="471a4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a4-121">3\_0</span></span> | <span data-ttu-id="471a4-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="471a4-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="471a4-123">texldl</span><span class="sxs-lookup"><span data-stu-id="471a4-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="471a4-124">x</span><span class="sxs-lookup"><span data-stu-id="471a4-124">x</span></span>    | <span data-ttu-id="471a4-125">x</span><span class="sxs-lookup"><span data-stu-id="471a4-125">x</span></span>     |



 

<span data-ttu-id="471a4-126">texldl Cerca il set di trame nella fase del campionatore a cui fa riferimento src1.</span><span class="sxs-lookup"><span data-stu-id="471a4-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="471a4-127">Il livello di dettaglio è selezionato da src0. w.</span><span class="sxs-lookup"><span data-stu-id="471a4-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="471a4-128">Questo valore può essere negativo, nel qual caso il livello di dettaglio selezionato è "Zero One" (mapping più grande) con il MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="471a4-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="471a4-129">Poiché src0. w è un valore a virgola mobile, il valore frazionario viene usato per interpolare (se MIPFILTER è lineare) tra due livelli MIP.</span><span class="sxs-lookup"><span data-stu-id="471a4-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="471a4-130">Gli Stati del campionatore MIPMAPLODBIAS e MAXMIPLEVEL vengono rispettati.</span><span class="sxs-lookup"><span data-stu-id="471a4-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="471a4-131">Per ulteriori informazioni sugli Stati del campionatore, vedere [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="471a4-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="471a4-132">Se uno shader esegue un campionamento di un campionatore che non dispone di un set di trame, 0001 viene ottenuto nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="471a4-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="471a4-133">Si tratta di un'approssimazione all'algoritmo del dispositivo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="471a4-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="471a4-134">Restrizioni:</span><span class="sxs-lookup"><span data-stu-id="471a4-134">Restrictions:</span></span>

-   <span data-ttu-id="471a4-135">Le coordinate di trama non devono essere ridimensionate in base alle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="471a4-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="471a4-136">DST deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="471a4-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="471a4-137">DST può accettare una maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="471a4-137">dst can accept a write mask.</span></span> <span data-ttu-id="471a4-138">Vedere [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="471a4-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="471a4-139">Le impostazioni predefinite per i componenti mancanti sono 0 o 1 e dipendono dal formato di trama.</span><span class="sxs-lookup"><span data-stu-id="471a4-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="471a4-140">src1 deve essere un [campionatore (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# ).</span><span class="sxs-lookup"><span data-stu-id="471a4-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="471a4-141">src1 non può usare un modificatore negazioni.</span><span class="sxs-lookup"><span data-stu-id="471a4-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="471a4-142">src1 può usare Swizzle, che viene applicato dopo il campionamento prima che venga rispettata la maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="471a4-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="471a4-143">Il campionatore deve essere stato dichiarato (usando [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)) all'inizio dello shader.</span><span class="sxs-lookup"><span data-stu-id="471a4-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="471a4-144">Il numero di coordinate necessarie per eseguire l'esempio di trama dipende dalla modalità di dichiarazione del campionatore.</span><span class="sxs-lookup"><span data-stu-id="471a4-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="471a4-145">Se è stata dichiarata come cubo, è richiesta una coordinata di trama a tre componenti (. RGB).</span><span class="sxs-lookup"><span data-stu-id="471a4-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="471a4-146">La convalida impone che le coordinate fornite a texldl siano sufficienti per la dimensione di trama dichiarata per il campionatore.</span><span class="sxs-lookup"><span data-stu-id="471a4-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="471a4-147">Tuttavia, non è garantito che l'applicazione imposti effettivamente una trama (tramite l'API) con dimensioni uguali alla dimensione dichiarata per il campionatore.</span><span class="sxs-lookup"><span data-stu-id="471a4-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="471a4-148">In tal caso, il runtime tenterà di rilevare le mancate corrispondenze (probabilmente solo in fase di debug).</span><span class="sxs-lookup"><span data-stu-id="471a4-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="471a4-149">Il campionamento di una trama con meno dimensioni rispetto a quelli presenti nella coordinata di trama sarà consentito e si presuppone che ignori i componenti aggiuntivi delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="471a4-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="471a4-150">Viceversa, il campionamento di una trama con più dimensioni rispetto a quelle presenti nella coordinata di trama non è consentito.</span><span class="sxs-lookup"><span data-stu-id="471a4-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="471a4-151">Se il src0 (coordinata di trama) è un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), i componenti necessari per la ricerca (descritta in precedenza) devono essere stati scritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="471a4-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="471a4-152">Il campionamento di trame RGB senza segno comporterà valori float compresi tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="471a4-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="471a4-153">Il campionamento delle trame con segno comporterà valori float compresi tra-1,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="471a4-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="471a4-154">Quando si campionano trame a virgola mobile, il valore di Float16 indica che i dati variano entro il numero massimo di \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="471a4-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="471a4-155">Float32 indica che verrà utilizzato l'intervallo massimo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="471a4-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="471a4-156">Il campionamento esterno a uno dei due intervalli non è definito.</span><span class="sxs-lookup"><span data-stu-id="471a4-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="471a4-157">Nessun limite di lettura dipendente.</span><span class="sxs-lookup"><span data-stu-id="471a4-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="471a4-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="471a4-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="471a4-159">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="471a4-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
