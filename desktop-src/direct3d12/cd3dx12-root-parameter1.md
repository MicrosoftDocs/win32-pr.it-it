---
title: Struttura CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura PARAMETRO1 radice D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Struttura CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323556"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="b3866-104">\_ \_ Struttura PARAMETRO1 radice CD3DX12</span><span class="sxs-lookup"><span data-stu-id="b3866-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="b3866-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ parametro1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="b3866-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3866-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3866-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="b3866-107">Members</span><span class="sxs-lookup"><span data-stu-id="b3866-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3866-108">**CD3DX12 \_ radice \_ parametro1 ()**</span><span class="sxs-lookup"><span data-stu-id="b3866-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-109">Crea una nuova istanza non inizializzata di un \_ parametro1 radice CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b3866-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="b3866-110">**Explicit CD3DX12 \_ root \_ parametro1 (const D3D12 \_ root \_ parametro1 &o)**</span><span class="sxs-lookup"><span data-stu-id="b3866-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-111">Crea una nuova istanza di un \_ parametro1 radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ parametro1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="b3866-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3866-112">**static inline InitAsDescriptorTable (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-113">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-114">[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b3866-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b3866-115">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b3866-116">[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b3866-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="b3866-117">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-118">**static inline InitAsConstants (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-119">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-120">[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b3866-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b3866-121">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-121">UINT num32BitValues</span></span>

<span data-ttu-id="b3866-122">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-122">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-123">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-124">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-125">**static inline InitAsConstantBufferView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-126">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-127">[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b3866-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b3866-128">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-128">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-129">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-130">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-131">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-132">**static inline InitAsShaderResourceView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-133">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-134">[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b3866-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b3866-135">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-135">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-136">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-137">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-138">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-139">**static inline InitAsUnorderedAccessView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-140">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-141">[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b3866-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b3866-142">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-142">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-143">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-144">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-145">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-146">**inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-147">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-148">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b3866-149">[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b3866-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="b3866-150">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-151">**inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-152">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-153">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-153">UINT num32BitValues</span></span>

<span data-ttu-id="b3866-154">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-154">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-155">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-156">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-157">**inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-158">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-159">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-159">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-160">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-161">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-162">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-163">**inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-164">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-165">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-165">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-166">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-167">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-168">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b3866-169">**inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="b3866-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b3866-170">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3866-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3866-171">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="b3866-171">UINT shaderRegister</span></span>

<span data-ttu-id="b3866-172">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b3866-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="b3866-173">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b3866-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b3866-174">[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="b3866-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3866-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3866-175">Requirements</span></span>



| <span data-ttu-id="b3866-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3866-176">Requirement</span></span> | <span data-ttu-id="b3866-177">Valore</span><span class="sxs-lookup"><span data-stu-id="b3866-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3866-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3866-178">Header</span></span><br/> | <dl> <span data-ttu-id="b3866-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3866-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3866-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3866-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3866-181">**\_Parametro1 radice \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="b3866-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="b3866-182">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="b3866-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





