---
title: Struttura CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di parametri radice D3D12.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Struttura CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322204"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="43af7-104">\_Struttura di \_ parametri radice CD3DX12</span><span class="sxs-lookup"><span data-stu-id="43af7-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="43af7-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ parametri radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="43af7-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="43af7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43af7-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="43af7-107">Members</span><span class="sxs-lookup"><span data-stu-id="43af7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="43af7-108">**\_Parametro radice CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="43af7-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-109">Crea una nuova istanza non inizializzata di un \_ parametro radice CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="43af7-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="43af7-110">**parametro radice CD3DX12 esplicito \_ \_ (parametro radice D3D12 const \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="43af7-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-111">Crea una nuova istanza di un \_ parametro radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ parametri radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="43af7-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="43af7-112">**static inline InitAsDescriptorTable ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descrittore \_ Range \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-113">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-114">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="43af7-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="43af7-115">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="43af7-116">[**D3D12 \_ \_Intervallo DEscrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="43af7-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="43af7-117">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-118">**static inline InitAsConstants ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-119">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-120">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="43af7-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="43af7-121">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-121">UINT num32BitValues</span></span>

<span data-ttu-id="43af7-122">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-122">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-123">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-124">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-125">**static inline InitAsConstantBufferView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-126">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-127">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="43af7-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="43af7-128">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-128">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-129">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-130">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-131">**static inline InitAsShaderResourceView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-132">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-133">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="43af7-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="43af7-134">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-134">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-135">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-136">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-137">**static inline InitAsUnorderedAccessView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-138">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-139">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="43af7-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="43af7-140">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-140">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-141">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-142">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-143">**inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-144">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-145">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="43af7-146">[**D3D12 \_ \_Intervallo DEscrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="43af7-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="43af7-147">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-148">**inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-149">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-150">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-150">UINT num32BitValues</span></span>

<span data-ttu-id="43af7-151">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-151">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-152">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-153">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-154">**inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-155">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-156">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-156">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-157">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-158">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-159">**inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-160">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-161">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-161">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-162">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-163">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="43af7-164">**inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="43af7-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="43af7-165">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="43af7-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="43af7-166">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="43af7-166">UINT shaderRegister</span></span>

<span data-ttu-id="43af7-167">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="43af7-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="43af7-168">consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="43af7-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43af7-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43af7-169">Requirements</span></span>



| <span data-ttu-id="43af7-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="43af7-170">Requirement</span></span> | <span data-ttu-id="43af7-171">Valore</span><span class="sxs-lookup"><span data-stu-id="43af7-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43af7-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43af7-172">Header</span></span><br/> | <dl> <span data-ttu-id="43af7-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="43af7-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43af7-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43af7-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43af7-175">**\_Parametro radice \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="43af7-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="43af7-176">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="43af7-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





