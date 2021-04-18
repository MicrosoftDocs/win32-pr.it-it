---
title: Struttura CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura BYTECODE dello shader D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Struttura CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322203"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="34b8a-104">\_ \_ Struttura BYTECODE shader CD3DX12</span><span class="sxs-lookup"><span data-stu-id="34b8a-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="34b8a-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ BYTECODE dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="34b8a-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b8a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34b8a-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="34b8a-107">Members</span><span class="sxs-lookup"><span data-stu-id="34b8a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34b8a-108">**\_BYTECODE shader CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="34b8a-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="34b8a-109">Crea una nuova istanza non inizializzata di un \_ BYTECODE dello shader CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="34b8a-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="34b8a-110">**bytecode CD3DX12 \_ shader esplicito \_ (const D3D12 \_ shader \_ bytecode &o)**</span><span class="sxs-lookup"><span data-stu-id="34b8a-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="34b8a-111">Crea una nuova istanza di un \_ bytecode dello shader CD3DX12 \_ , inizializzato con il contenuto di un'altra struttura [**\_ \_ bytecode dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="34b8a-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34b8a-112">**\_BYTECODE shader CD3DX12 \_ (ID3DBlob \* pShaderBlob)**</span><span class="sxs-lookup"><span data-stu-id="34b8a-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="34b8a-113">Crea una nuova istanza di un \_ BYTECODE dello shader CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="34b8a-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="34b8a-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob</span><span class="sxs-lookup"><span data-stu-id="34b8a-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="34b8a-115">**\_BYTECODE shader CD3DX12 \_ (const void \* \_ PShaderBytecode, Size \_ T bytecodeLength)**</span><span class="sxs-lookup"><span data-stu-id="34b8a-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="34b8a-116">Crea una nuova istanza di un \_ BYTECODE dello shader CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="34b8a-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="34b8a-117">void \* \_ pShaderBytecode</span><span class="sxs-lookup"><span data-stu-id="34b8a-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="34b8a-118">DIMENSIONI \_ T bytecodeLength</span><span class="sxs-lookup"><span data-stu-id="34b8a-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="34b8a-119">**operator const D3D12 \_ BYTECODE dello shader \_& () const**</span><span class="sxs-lookup"><span data-stu-id="34b8a-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="34b8a-120">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="34b8a-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34b8a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34b8a-121">Requirements</span></span>



| <span data-ttu-id="34b8a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b8a-122">Requirement</span></span> | <span data-ttu-id="34b8a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="34b8a-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34b8a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34b8a-124">Header</span></span><br/> | <dl> <span data-ttu-id="34b8a-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b8a-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b8a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34b8a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b8a-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="34b8a-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="34b8a-128">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="34b8a-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

