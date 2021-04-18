---
title: Struttura CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di valori non crittografati D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Struttura CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322281"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="5809a-104">\_Struttura del valore Clear di CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="5809a-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="5809a-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ valori non crittografati D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="5809a-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5809a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5809a-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="5809a-107">Members</span><span class="sxs-lookup"><span data-stu-id="5809a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5809a-108">**\_Valore CD3DX12 Clear \_ ()**</span><span class="sxs-lookup"><span data-stu-id="5809a-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="5809a-109">Crea una nuova istanza non inizializzata di un \_ valore CD3DX12 Clear \_ .</span><span class="sxs-lookup"><span data-stu-id="5809a-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="5809a-110">**valore esplicito CD3DX12 \_ Clear \_ (const D3D12 \_ Clear \_ value &o)**</span><span class="sxs-lookup"><span data-stu-id="5809a-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5809a-111">Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ valori non crittografati D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="5809a-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5809a-112">**CD3DX12 \_ Clear \_ value ( \_ formato DXGI, const Float color \[ 4 \] )**</span><span class="sxs-lookup"><span data-stu-id="5809a-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="5809a-113">Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5809a-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="5809a-114">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="5809a-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="5809a-115">Colore FLOAT \[ 4 \]</span><span class="sxs-lookup"><span data-stu-id="5809a-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="5809a-116">**\_Valore CD3DX12 Clear \_ (formato DXGI \_ , profondità float, stencil Uint8)**</span><span class="sxs-lookup"><span data-stu-id="5809a-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="5809a-117">Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5809a-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="5809a-118">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="5809a-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="5809a-119">Profondità FLOAT</span><span class="sxs-lookup"><span data-stu-id="5809a-119">FLOAT depth</span></span>

<span data-ttu-id="5809a-120">Stencil UINT8</span><span class="sxs-lookup"><span data-stu-id="5809a-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="5809a-121">**operator const D3D12 \_ Clear \_ value& () const**</span><span class="sxs-lookup"><span data-stu-id="5809a-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5809a-122">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="5809a-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5809a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5809a-123">Requirements</span></span>



| <span data-ttu-id="5809a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5809a-124">Requirement</span></span> | <span data-ttu-id="5809a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5809a-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5809a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5809a-126">Header</span></span><br/> | <dl> <span data-ttu-id="5809a-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5809a-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5809a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5809a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5809a-129">**\_Valore D3D12 Clear \_**</span><span class="sxs-lookup"><span data-stu-id="5809a-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="5809a-130">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="5809a-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

