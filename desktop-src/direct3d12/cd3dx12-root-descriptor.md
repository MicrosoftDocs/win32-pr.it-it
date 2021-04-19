---
title: Struttura CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura del descrittore radice D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323562"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="fa02d-104">\_Struttura del \_ descrittore radice CD3DX12</span><span class="sxs-lookup"><span data-stu-id="fa02d-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="fa02d-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="fa02d-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa02d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa02d-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="fa02d-107">Members</span><span class="sxs-lookup"><span data-stu-id="fa02d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa02d-108">**\_Descrittore radice CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="fa02d-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="fa02d-109">Crea una nuova istanza non inizializzata di un \_ \_ descrittore radice CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="fa02d-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="fa02d-110">**descrittore radice CD3DX12 esplicito \_ \_ ( \_ descrittore radice D3D12 const \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="fa02d-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="fa02d-111">Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12, inizializzato con il contenuto di un'altra struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="fa02d-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fa02d-112">**\_Descrittore radice CD3DX12 \_ (uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="fa02d-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="fa02d-113">Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa02d-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="fa02d-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="fa02d-114">UINT shaderRegister</span></span>

<span data-ttu-id="fa02d-115">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="fa02d-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="fa02d-116">**Init inline (UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="fa02d-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="fa02d-117">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa02d-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="fa02d-118">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="fa02d-118">UINT shaderRegister</span></span>

<span data-ttu-id="fa02d-119">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="fa02d-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="fa02d-120">**static inline init (D3D12 \_ radice \_ descrittore &tabella, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="fa02d-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="fa02d-121">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa02d-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="fa02d-122">[**D3D12 \_ \_Descrittore radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &tabella</span><span class="sxs-lookup"><span data-stu-id="fa02d-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="fa02d-123">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="fa02d-123">UINT shaderRegister</span></span>

<span data-ttu-id="fa02d-124">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="fa02d-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa02d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa02d-125">Requirements</span></span>



| <span data-ttu-id="fa02d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa02d-126">Requirement</span></span> | <span data-ttu-id="fa02d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fa02d-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fa02d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa02d-128">Header</span></span><br/> | <dl> <span data-ttu-id="fa02d-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa02d-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa02d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa02d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa02d-131">**\_Descrittore radice D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="fa02d-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="fa02d-132">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="fa02d-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





