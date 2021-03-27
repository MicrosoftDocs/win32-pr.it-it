---
title: Interfaccia ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Un'interfaccia di variabile shader accede a una variabile shader.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995924"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="6434f-105">Interfaccia ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="6434f-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="6434f-106">Un'interfaccia di variabile shader accede a una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="6434f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6434f-107">Members</span></span>

<span data-ttu-id="6434f-108">L'interfaccia **ID3DX11EffectShaderVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6434f-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6434f-109">**ID3DX11EffectShaderVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6434f-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6434f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6434f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6434f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6434f-111">Methods</span></span>

<span data-ttu-id="6434f-112">L'interfaccia **ID3DX11EffectShaderVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6434f-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="6434f-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="6434f-113">Method</span></span>                                                                                                           | <span data-ttu-id="6434f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6434f-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="6434f-115">**GetComputeShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="6434f-116">Ottenere un compute shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="6434f-117">**GetDomainShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="6434f-118">Ottenere un Domain shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="6434f-119">**GetGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="6434f-120">Ottenere un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="6434f-121">**GetHullShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="6434f-122">Ottenere un Hull shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="6434f-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="6434f-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="6434f-124">Ottenere una descrizione della firma di input.</span><span class="sxs-lookup"><span data-stu-id="6434f-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="6434f-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="6434f-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="6434f-126">Ottenere una descrizione della firma di output.</span><span class="sxs-lookup"><span data-stu-id="6434f-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="6434f-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="6434f-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="6434f-128">Ottenere una descrizione della firma costante della patch.</span><span class="sxs-lookup"><span data-stu-id="6434f-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="6434f-129">**GetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="6434f-130">Ottenere un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="6434f-131">**GetShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6434f-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="6434f-132">Ottenere una descrizione dello shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="6434f-133">**GetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="6434f-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="6434f-134">Ottenere un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="6434f-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="6434f-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="6434f-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6434f-136">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6434f-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6434f-137">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6434f-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6434f-138">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6434f-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6434f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6434f-139">Requirements</span></span>



| <span data-ttu-id="6434f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6434f-140">Requirement</span></span> | <span data-ttu-id="6434f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="6434f-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6434f-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6434f-142">Header</span></span><br/>  | <dl> <span data-ttu-id="6434f-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6434f-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6434f-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="6434f-144">Library</span></span><br/> | <dl> <span data-ttu-id="6434f-145"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6434f-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6434f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6434f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6434f-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6434f-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6434f-148">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="6434f-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6434f-149">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6434f-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





