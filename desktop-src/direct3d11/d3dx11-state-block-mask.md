---
title: Struttura D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indica lo stato del dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Struttura D3DX11_STATE_BLOCK_MASK Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355359"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="0ebf3-104">\_Struttura della \_ maschera di blocco dello stato D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="0ebf3-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="0ebf3-105">Indica lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebf3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ebf3-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="0ebf3-107">Members</span><span class="sxs-lookup"><span data-stu-id="0ebf3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ebf3-108">**VS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-109">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-110">Valore booleano che indica se salvare lo stato del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-111">**VSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-112">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-113">Matrice di Sampler vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="0ebf3-114">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-115">**VSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-116">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-117">Matrice di risorse vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="0ebf3-118">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-119">**VSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-120">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-121">Matrice di buffer costanti del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-122">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-123">**VSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-124">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-125">Matrice di interfacce vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="0ebf3-126">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-127">**HS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-128">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-129">Valore booleano che indica se salvare lo stato di Hull shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-130">**HSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-131">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-132">Matrice di Sampler di Hull shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="0ebf3-133">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-134">**HSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-135">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-136">Matrice di risorse dello shader Hull.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-136">Array of hull-shader resources.</span></span> <span data-ttu-id="0ebf3-137">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-138">**HSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-139">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-140">Matrice di buffer costanti dello shader Hull.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-141">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-142">**HSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-143">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-144">Matrice di interfacce dello shader Hull.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="0ebf3-145">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-147">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-148">Valore booleano che indica se salvare lo stato del Domain shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-149">**DSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-150">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-151">Matrice di Sampler di Domain shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="0ebf3-152">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-153">**DSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-154">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-155">Matrice di risorse dello shader di dominio.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-155">Array of domain-shader resources.</span></span> <span data-ttu-id="0ebf3-156">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-157">**DSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-158">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-159">Matrice di buffer di costanti dello shader di dominio.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-160">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-161">**DSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-162">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-163">Matrice di interfacce dello shader di dominio.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="0ebf3-164">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-166">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-167">Valore booleano che indica se salvare lo stato di Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-168">**GSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-169">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-170">Matrice di Sampler geometry shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="0ebf3-171">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-172">**GSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-173">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-174">Matrice di risorse dello shader di geometria.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="0ebf3-175">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-176">**GSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-177">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-178">Matrice di buffer costanti dello shader di geometria.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-179">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-180">**GSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-181">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-182">Matrice di interfacce di shader Geometry.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="0ebf3-183">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-184">**PS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-185">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-186">Valore booleano che indica se salvare lo stato del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-187">**PSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-188">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-189">Matrice di Sampler pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="0ebf3-190">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-191">**PSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-192">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-193">Matrice di risorse pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="0ebf3-194">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-195">**PSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-196">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-197">Matrice di buffer costanti pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-198">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-199">**PSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-200">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-201">Matrice di interfacce pixel shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="0ebf3-202">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-203">**PSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-204">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-205">Valore booleano che indica se salvare il pixel shader le visualizzazioni di accesso non ordinate.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-207">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-208">Valore booleano che indica se salvare lo stato di compute shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-209">**CSSamplers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-210">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-211">Matrice di Sampler di compute shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="0ebf3-212">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-213">**CSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-214">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-215">Matrice di risorse di calcolo shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-215">Array of compute-shader resources.</span></span> <span data-ttu-id="0ebf3-216">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-217">**CSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-218">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-219">Matrice di buffer costanti compute shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="0ebf3-220">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-221">**CSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-222">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-223">Matrice di interfacce di calcolo shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="0ebf3-224">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-225">**CSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-226">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-227">Valore booleano che indica se salvare le visualizzazioni di accesso non ordinato del compute shader.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-228">**IAVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-229">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-230">Matrice di buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-230">Array of vertex buffers.</span></span> <span data-ttu-id="0ebf3-231">La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-232">**IAIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-233">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-234">Valore booleano che indica se salvare lo stato del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-235">**IAInputLayout**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-236">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-237">Valore booleano che indica se salvare lo stato del layout di input.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-238">**IAPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-239">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-240">Valore booleano che indica se salvare lo stato della topologia primitiva.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-241">**OMRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-242">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-243">Valore booleano che indica se salvare gli Stati delle destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-244">**OMDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-245">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-246">Valore booleano che indica se salvare lo stato dello stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-247">**OMBlendState**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-248">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-249">Valore booleano che indica se salvare lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-250">**RSViewports**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-251">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-252">Valore booleano che indica se salvare gli Stati dei viewport.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-253">**RSScissorRects**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-254">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-255">Valore booleano che indica se salvare gli Stati dei rettangoli a forbice.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-256">**RSRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-257">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-258">Valore booleano che indica se salvare lo stato del rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-259">**SOBuffers**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-260">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-261">Valore booleano che indica se salvare gli Stati dei buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf3-262">**Predicazione**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="0ebf3-263">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0ebf3-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0ebf3-264">Valore booleano che indica se salvare lo stato predicazione.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ebf3-265">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ebf3-265">Remarks</span></span>

<span data-ttu-id="0ebf3-266">Una maschera di blocco di stato indica che il dispositivo è stato modificato da un passaggio o da una tecnica.</span><span class="sxs-lookup"><span data-stu-id="0ebf3-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebf3-267">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ebf3-267">Requirements</span></span>



| <span data-ttu-id="0ebf3-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebf3-268">Requirement</span></span> | <span data-ttu-id="0ebf3-269">Valore</span><span class="sxs-lookup"><span data-stu-id="0ebf3-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebf3-270">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ebf3-270">Header</span></span><br/> | <dl> <span data-ttu-id="0ebf3-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf3-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebf3-272">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ebf3-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebf3-273">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="0ebf3-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

