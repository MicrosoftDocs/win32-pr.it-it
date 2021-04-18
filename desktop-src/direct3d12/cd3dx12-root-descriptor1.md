---
title: Struttura CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura DESCRIPTOR1 radice D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323558"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="c6542-104">\_ \_ Struttura DESCRIPTOR1 radice CD3DX12</span><span class="sxs-lookup"><span data-stu-id="c6542-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="c6542-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ DESCRIPTOR1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="c6542-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6542-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6542-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="c6542-107">Members</span><span class="sxs-lookup"><span data-stu-id="c6542-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6542-108">**CD3DX12 \_ radice \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="c6542-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="c6542-109">Crea una nuova istanza non inizializzata di un \_ DESCRIPTOR1 radice CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c6542-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="c6542-110">**Explicit CD3DX12 \_ root \_ DESCRIPTOR1 (const D3D12 \_ root \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="c6542-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c6542-111">Crea una nuova istanza di un \_ DESCRIPTOR1 radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ DESCRIPTOR1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="c6542-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c6542-112">**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="c6542-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="c6542-113">Crea una nuova istanza di un \_ DESCRIPTOR1 radice CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6542-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="c6542-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="c6542-114">UINT shaderRegister</span></span>

<span data-ttu-id="c6542-115">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c6542-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="c6542-116">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="c6542-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="c6542-117">**inline init (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ Descriptor \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="c6542-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="c6542-118">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6542-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c6542-119">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="c6542-119">UINT shaderRegister</span></span>

<span data-ttu-id="c6542-120">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c6542-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="c6542-121">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="c6542-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="c6542-122">**static inline init (D3D12 \_ radice \_ DESCRIPTOR1 &Table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ radice \_ descrittore Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="c6542-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="c6542-123">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6542-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c6542-124">[**D3D12 \_ \_DESCRIPTOR1 radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &tabella</span><span class="sxs-lookup"><span data-stu-id="c6542-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="c6542-125">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="c6542-125">UINT shaderRegister</span></span>

<span data-ttu-id="c6542-126">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c6542-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="c6542-127">[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="c6542-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6542-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6542-128">Requirements</span></span>



| <span data-ttu-id="c6542-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6542-129">Requirement</span></span> | <span data-ttu-id="c6542-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c6542-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6542-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6542-131">Header</span></span><br/> | <dl> <span data-ttu-id="c6542-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6542-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6542-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6542-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6542-134">**\_DESCRIPTOR1 radice \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="c6542-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="c6542-135">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="c6542-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





