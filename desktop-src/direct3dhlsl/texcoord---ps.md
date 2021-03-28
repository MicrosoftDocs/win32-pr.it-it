---
title: TEXCOORD-PS
description: Interpreta i dati delle coordinate di trama (UVW1) come dati di colore (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728058"
---
# <a name="texcoord---ps"></a><span data-ttu-id="15a94-103">TEXCOORD-PS</span><span class="sxs-lookup"><span data-stu-id="15a94-103">texcoord - ps</span></span>

<span data-ttu-id="15a94-104">Interpreta i dati delle coordinate di trama (UVW1) come dati di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="15a94-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="15a94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15a94-105">Syntax</span></span>



| <span data-ttu-id="15a94-106">TEXCOORD DST</span><span class="sxs-lookup"><span data-stu-id="15a94-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="15a94-107">dove</span><span class="sxs-lookup"><span data-stu-id="15a94-107">where</span></span>

-   <span data-ttu-id="15a94-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="15a94-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a94-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="15a94-109">Remarks</span></span>



| <span data-ttu-id="15a94-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="15a94-110">Pixel shader versions</span></span> | <span data-ttu-id="15a94-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="15a94-111">1\_1</span></span> | <span data-ttu-id="15a94-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="15a94-112">1\_2</span></span> | <span data-ttu-id="15a94-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="15a94-113">1\_3</span></span> | <span data-ttu-id="15a94-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="15a94-114">1\_4</span></span> | <span data-ttu-id="15a94-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15a94-115">2\_0</span></span> | <span data-ttu-id="15a94-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="15a94-116">2\_x</span></span> | <span data-ttu-id="15a94-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15a94-117">2\_sw</span></span> | <span data-ttu-id="15a94-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15a94-118">3\_0</span></span> | <span data-ttu-id="15a94-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15a94-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="15a94-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="15a94-120">texcoord</span></span>              | <span data-ttu-id="15a94-121">x</span><span class="sxs-lookup"><span data-stu-id="15a94-121">x</span></span>    | <span data-ttu-id="15a94-122">x</span><span class="sxs-lookup"><span data-stu-id="15a94-122">x</span></span>    | <span data-ttu-id="15a94-123">x</span><span class="sxs-lookup"><span data-stu-id="15a94-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="15a94-124">Questa istruzione interpreta il set di coordinate di trama (UVW1) corrispondente al numero di registro di destinazione come dati colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="15a94-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="15a94-125">Se il set di coordinate di trama contiene meno di tre componenti, i componenti mancanti vengono impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="15a94-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="15a94-126">Il quarto componente viene sempre impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="15a94-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="15a94-127">Tutti i valori vengono fissati tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="15a94-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="15a94-128">Il vantaggio di TEXCOORD è che fornisce un modo per passare i dati dei vertici interpolati a precisione elevata direttamente nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="15a94-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="15a94-129">Tuttavia, quando i dati vengono scritti nel registro di destinazione, una certa precisione andrà persa, a seconda del numero di bit utilizzati dall'hardware per i registri.</span><span class="sxs-lookup"><span data-stu-id="15a94-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="15a94-130">Questa istruzione non consente di campionare alcuna trama.</span><span class="sxs-lookup"><span data-stu-id="15a94-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="15a94-131">Sono rilevanti solo le coordinate di trama impostate in questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="15a94-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="15a94-132">È possibile eseguire il mapping di qualsiasi dato di trama, ad esempio posizione, normale e direzione di origine, tramite un vertex shader in una coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="15a94-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="15a94-133">Questa operazione viene eseguita associando una trama a un registro di trama usando la trama e specificando il modo in cui viene eseguito il campionamento della [**trama usando**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="15a94-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="15a94-134">Se viene utilizzata la pipeline della funzione fissa, assicurarsi di specificare il \_ flag TEXCOORDINDEX di TSS.</span><span class="sxs-lookup"><span data-stu-id="15a94-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="15a94-135">Questa istruzione viene utilizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="15a94-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="15a94-136">Un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contiene quattro valori di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="15a94-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="15a94-137">I dati possono essere considerati anche come dati vettoriali (xyzw).</span><span class="sxs-lookup"><span data-stu-id="15a94-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="15a94-138">TEXCOORD recupererà tre di questi valori (XYZ) dal set di coordinate di trama x e il quarto componente (w) verrà impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="15a94-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="15a94-139">L'indirizzo di trama viene copiato dal set di coordinate di trama n.</span><span class="sxs-lookup"><span data-stu-id="15a94-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="15a94-140">Il risultato viene fissato tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="15a94-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="15a94-141">Questo esempio viene utilizzato solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="15a94-141">This example is for illustration only.</span></span> <span data-ttu-id="15a94-142">Il codice C associato allo shader non è stato ottimizzato per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="15a94-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="15a94-143">Di seguito è riportato un esempio di shader che usa TEXCOORD.</span><span class="sxs-lookup"><span data-stu-id="15a94-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="15a94-144">L'output di cui è stato eseguito il rendering dal pixel shader è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="15a94-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="15a94-145">I valori delle coordinate (u, v, w, 1) vengono mappati ai canali (RGB).</span><span class="sxs-lookup"><span data-stu-id="15a94-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="15a94-146">Il canale alfa è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="15a94-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="15a94-147">Negli angoli dell'illustrazione, la coordinata (0, 0, 0, 1) viene interpretata come nera; (1, 0, 0, 1) è rosso; (0, 1, 0, 1) è verde; e (1, 1, 0, 1) contiene verde e rosso, producendo un colore giallo.</span><span class="sxs-lookup"><span data-stu-id="15a94-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![illustrazione dell'output sottoposto a rendering dell'esempio pixel shader](images/pstexcoord.jpg)

<span data-ttu-id="15a94-149">Il codice aggiuntivo è necessario per usare questo shader e uno scenario di esempio è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="15a94-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="15a94-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15a94-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a94-151">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="15a94-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 