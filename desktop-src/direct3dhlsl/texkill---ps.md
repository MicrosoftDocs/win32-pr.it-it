---
title: texkill-PS
description: Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate di trama è minore di zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335447"
---
# <a name="texkill---ps"></a><span data-ttu-id="be920-103">texkill-PS</span><span class="sxs-lookup"><span data-stu-id="be920-103">texkill - ps</span></span>

<span data-ttu-id="be920-104">Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate di trama è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="be920-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="be920-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be920-105">Syntax</span></span>



| <span data-ttu-id="be920-106">texkill DST</span><span class="sxs-lookup"><span data-stu-id="be920-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="be920-107">dove</span><span class="sxs-lookup"><span data-stu-id="be920-107">where</span></span>

-   <span data-ttu-id="be920-108">DST è un registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="be920-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="be920-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="be920-109">Remarks</span></span>



| <span data-ttu-id="be920-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="be920-110">Pixel shader versions</span></span> | <span data-ttu-id="be920-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="be920-111">1\_1</span></span> | <span data-ttu-id="be920-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="be920-112">1\_2</span></span> | <span data-ttu-id="be920-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="be920-113">1\_3</span></span> | <span data-ttu-id="be920-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="be920-114">1\_4</span></span> | <span data-ttu-id="be920-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="be920-115">2\_0</span></span> | <span data-ttu-id="be920-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="be920-116">2\_x</span></span> | <span data-ttu-id="be920-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="be920-117">2\_sw</span></span> | <span data-ttu-id="be920-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="be920-118">3\_0</span></span> | <span data-ttu-id="be920-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="be920-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="be920-120">texkill</span><span class="sxs-lookup"><span data-stu-id="be920-120">texkill</span></span>               | <span data-ttu-id="be920-121">x</span><span class="sxs-lookup"><span data-stu-id="be920-121">x</span></span>    | <span data-ttu-id="be920-122">x</span><span class="sxs-lookup"><span data-stu-id="be920-122">x</span></span>    | <span data-ttu-id="be920-123">x</span><span class="sxs-lookup"><span data-stu-id="be920-123">x</span></span>    | <span data-ttu-id="be920-124">x</span><span class="sxs-lookup"><span data-stu-id="be920-124">x</span></span>    | <span data-ttu-id="be920-125">x</span><span class="sxs-lookup"><span data-stu-id="be920-125">x</span></span>    | <span data-ttu-id="be920-126">x</span><span class="sxs-lookup"><span data-stu-id="be920-126">x</span></span>    | <span data-ttu-id="be920-127">x</span><span class="sxs-lookup"><span data-stu-id="be920-127">x</span></span>     | <span data-ttu-id="be920-128">x</span><span class="sxs-lookup"><span data-stu-id="be920-128">x</span></span>    | <span data-ttu-id="be920-129">x</span><span class="sxs-lookup"><span data-stu-id="be920-129">x</span></span>     |



 

<span data-ttu-id="be920-130">Questa istruzione corrisponde alla funzione di [**ritaglio**](dx-graphics-hlsl-clip.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="be920-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="be920-131">texkill non campiona alcuna trama.</span><span class="sxs-lookup"><span data-stu-id="be920-131">texkill does not sample any texture.</span></span> <span data-ttu-id="be920-132">Opera sui primi tre componenti delle coordinate di trama fornite dal numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be920-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="be920-133">Per PS \_ 1 \_ 4, texkill opera sui dati nei primi tre componenti del registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be920-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="be920-134">È possibile utilizzare questa istruzione per implementare piani di ritaglio arbitrari nel rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="be920-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="be920-135">Quando si usano vertex shader, l'applicazione è responsabile dell'applicazione della trasformazione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="be920-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="be920-136">Questo può causare problemi per i piani di ritaglio arbitrari perché se contiene fattori di scala anisomorphic, è necessario trasformare anche i piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="be920-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="be920-137">Pertanto, è preferibile fornire una posizione di vertice non proiettata da usare nel Clipper arbitrario, ovvero il set di coordinate di trama identificato dall'operatore texkill.</span><span class="sxs-lookup"><span data-stu-id="be920-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="be920-138">Questa istruzione viene utilizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="be920-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="be920-139">texkill TN</span><span class="sxs-lookup"><span data-stu-id="be920-139">texkill tn</span></span>  
<span data-ttu-id="be920-140">Il mascheramento dei pixel viene eseguito come segue:</span><span class="sxs-lookup"><span data-stu-id="be920-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="be920-141">if (i componenti x, y, z di TextureCoordinates (fase n)<sub>UVWQ</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="be920-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="be920-142">Annulla rendering pixel</span><span class="sxs-lookup"><span data-stu-id="be920-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="be920-143">Per pixel shader 1 \_ 1, 1 \_ 2 e 1 \_ 3, texkill opera sul set di coordinate di trama fornito dal numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be920-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="be920-144">Nella versione 1 \_ 4, tuttavia, texkill opera sui dati contenuti nel registro delle [coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) o nel registro temporaneo (RN) specificato come destinazione.</span><span class="sxs-lookup"><span data-stu-id="be920-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="be920-145">Quando è abilitato il campionamento multiplo, qualsiasi effetto di anti-aliasing raggiunto sui bordi del poligono a causa del campionamento multiplo non verrà raggiunto lungo i bordi generati da texkill.</span><span class="sxs-lookup"><span data-stu-id="be920-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="be920-146">Il pixel shader viene eseguito una volta per pixel.</span><span class="sxs-lookup"><span data-stu-id="be920-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="be920-147">Questo esempio viene utilizzato solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="be920-147">This example is for illustration only.</span></span>

<span data-ttu-id="be920-148">Questo esempio Mostra come mascherare i pixel con coordinate di trama negative.</span><span class="sxs-lookup"><span data-stu-id="be920-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="be920-149">I colori dei pixel vengono interpolati dai colori dei vertici forniti nei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="be920-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="be920-150">Le coordinate di trama variano da-0,5 a 0,5 in u e da 0,0 a 1,0 in v.</span><span class="sxs-lookup"><span data-stu-id="be920-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="be920-151">Con questa istruzione i valori u negativi vengono mascherati. La prima figura seguente mostra il colore del vertice applicato al quad senza l'istruzione texkill applicata.</span><span class="sxs-lookup"><span data-stu-id="be920-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="be920-152">La seconda illustrazione seguente mostra il risultato dell'istruzione texkill.</span><span class="sxs-lookup"><span data-stu-id="be920-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="be920-153">I colori dei pixel dalle coordinate di trama inferiori a 0 (dove x passa da-0,5 a 0,0) sono mascherati. Il colore di sfondo (bianco) viene usato quando il colore del pixel è mascherato.</span><span class="sxs-lookup"><span data-stu-id="be920-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![illustrazione dell'output con il colore del vertice applicato al quad senza l'istruzione texkill](images/pstexkill-in.jpg)![illustrazione dell'output con l'istruzione texkill applicata](images/pstexkill-out.jpg)

<span data-ttu-id="be920-156">I dati delle coordinate di trama sono dichiarati nella dichiarazione dei dati dei vertici in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="be920-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="be920-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be920-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be920-158">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="be920-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




