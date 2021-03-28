---
title: Tex-PS
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama. La trama deve essere associata a una fase di trama particolare (n) utilizzando la texture. Il campionamento della trama è controllato da SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963238"
---
# <a name="tex---ps"></a><span data-ttu-id="48098-105">Tex-PS</span><span class="sxs-lookup"><span data-stu-id="48098-105">tex - ps</span></span>

<span data-ttu-id="48098-106">Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama.</span><span class="sxs-lookup"><span data-stu-id="48098-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="48098-107">La trama deve essere associata a una fase di trama particolare (n) [**utilizzando la texture.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)</span><span class="sxs-lookup"><span data-stu-id="48098-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="48098-108">Il campionamento della trama è controllato da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="48098-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="48098-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48098-109">Syntax</span></span>



| <span data-ttu-id="48098-110">ora di Tex</span><span class="sxs-lookup"><span data-stu-id="48098-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="48098-111">dove</span><span class="sxs-lookup"><span data-stu-id="48098-111">where</span></span>

-   <span data-ttu-id="48098-112">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="48098-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="48098-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="48098-113">Remarks</span></span>



| <span data-ttu-id="48098-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="48098-114">Pixel shader versions</span></span> | <span data-ttu-id="48098-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="48098-115">1\_1</span></span> | <span data-ttu-id="48098-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="48098-116">1\_2</span></span> | <span data-ttu-id="48098-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="48098-117">1\_3</span></span> | <span data-ttu-id="48098-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="48098-118">1\_4</span></span> | <span data-ttu-id="48098-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48098-119">2\_0</span></span> | <span data-ttu-id="48098-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48098-120">2\_x</span></span> | <span data-ttu-id="48098-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48098-121">2\_sw</span></span> | <span data-ttu-id="48098-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48098-122">3\_0</span></span> | <span data-ttu-id="48098-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48098-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="48098-124">Tex</span><span class="sxs-lookup"><span data-stu-id="48098-124">tex</span></span>                   | <span data-ttu-id="48098-125">x</span><span class="sxs-lookup"><span data-stu-id="48098-125">x</span></span>    | <span data-ttu-id="48098-126">x</span><span class="sxs-lookup"><span data-stu-id="48098-126">x</span></span>    | <span data-ttu-id="48098-127">x</span><span class="sxs-lookup"><span data-stu-id="48098-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="48098-128">Il numero del registro di destinazione specifica il numero della fase della trama.</span><span class="sxs-lookup"><span data-stu-id="48098-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="48098-129">Il campionamento di trama usa coordinate di trama per cercare o campionare un valore di colore in corrispondenza delle coordinate specificate (u, v, w, q) tenendo conto degli attributi dello stato della fase della trama.</span><span class="sxs-lookup"><span data-stu-id="48098-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="48098-130">I dati delle coordinate di trama vengono interpolati dai dati delle coordinate di trama dei vertici ed è associato a una fase di trama specifica.</span><span class="sxs-lookup"><span data-stu-id="48098-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="48098-131">L'associazione predefinita è un mapping uno-a-uno tra il numero di fase della trama e l'ordine di dichiarazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="48098-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="48098-132">Ciò significa che per impostazione predefinita, il primo set di coordinate di trama definito nel formato Vertex è associato alla fase 0 della trama.</span><span class="sxs-lookup"><span data-stu-id="48098-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="48098-133">Le coordinate di trama possono essere associate a qualsiasi fase usando due tecniche.</span><span class="sxs-lookup"><span data-stu-id="48098-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="48098-134">Quando si usa un vertex shader della funzione fissa o la pipeline della funzione fissa, il flag di stato della fase \_ di trama TEXCOORDINDEX può essere usato in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per associare le coordinate a una fase.</span><span class="sxs-lookup"><span data-stu-id="48098-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="48098-135">In caso contrario, le coordinate di trama vengono restituite dai registri vertex shader oTn quando si usa un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="48098-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48098-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48098-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48098-137">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="48098-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 