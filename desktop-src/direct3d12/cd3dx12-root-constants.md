---
title: Struttura CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di costanti radice D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Struttura CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322212"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="e9051-104">\_Struttura delle \_ costanti radice CD3DX12</span><span class="sxs-lookup"><span data-stu-id="e9051-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="e9051-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="e9051-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9051-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9051-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="e9051-107">Members</span><span class="sxs-lookup"><span data-stu-id="e9051-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9051-108">**\_Costanti CD3DX12 radice \_ ()**</span><span class="sxs-lookup"><span data-stu-id="e9051-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="e9051-109">Crea una nuova istanza non inizializzata di una \_ costante CD3DX12 radice \_ .</span><span class="sxs-lookup"><span data-stu-id="e9051-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="e9051-110">**costanti radice CD3DX12 esplicite \_ \_ (costanti D3D12 \_ radice \_ costanti &o)**</span><span class="sxs-lookup"><span data-stu-id="e9051-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e9051-111">Crea una nuova istanza di una \_ costante CD3DX12 radice \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ costanti radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="e9051-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9051-112">**\_Costanti CD3DX12 radice \_ (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="e9051-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="e9051-113">Crea una nuova istanza di una \_ costante CD3DX12 radice \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9051-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="e9051-114">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-114">UINT num32BitValues</span></span>

<span data-ttu-id="e9051-115">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-115">UINT shaderRegister</span></span>

<span data-ttu-id="e9051-116">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e9051-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="e9051-117">**Init inline (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="e9051-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="e9051-118">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9051-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e9051-119">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-119">UINT num32BitValues</span></span>

<span data-ttu-id="e9051-120">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-120">UINT shaderRegister</span></span>

<span data-ttu-id="e9051-121">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e9051-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="e9051-122">**static inline init (D3D12 \_ radice \_ costanti &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="e9051-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="e9051-123">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9051-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e9051-124">[**D3D12 \_ \_Costanti radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span><span class="sxs-lookup"><span data-stu-id="e9051-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="e9051-125">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-125">UINT num32BitValues</span></span>

<span data-ttu-id="e9051-126">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="e9051-126">UINT shaderRegister</span></span>

<span data-ttu-id="e9051-127">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e9051-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9051-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9051-128">Requirements</span></span>



| <span data-ttu-id="e9051-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9051-129">Requirement</span></span> | <span data-ttu-id="e9051-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e9051-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9051-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9051-131">Header</span></span><br/> | <dl> <span data-ttu-id="e9051-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9051-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9051-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9051-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9051-134">**\_Costanti radice \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="e9051-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="e9051-135">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="e9051-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





