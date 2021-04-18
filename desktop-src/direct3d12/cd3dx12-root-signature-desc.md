---
title: Struttura CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura desc della firma radice D3D12 \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Struttura CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323554"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="12a09-104">\_ \_ Struttura desc della firma radice CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="12a09-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="12a09-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="12a09-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a09-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12a09-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="12a09-107">Members</span><span class="sxs-lookup"><span data-stu-id="12a09-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="12a09-108">**CD3DX12 \_ della \_ firma radice \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="12a09-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-109">Crea una nuova istanza non inizializzata di una \_ firma radice CD3DX12 \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="12a09-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="12a09-110">**Descrizione della \_ firma radice CD3DX12 esplicita \_ \_ (const D3D12 \_ root \_ Signature \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="12a09-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-111">Crea una nuova istanza di una \_ firma radice \_ CD3DX12 \_ DESC, inizializzata con il contenuto di un'altra struttura [**\_ \_ \_ desc della firma radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="12a09-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="12a09-112">**CD3DX12 \_ root \_ Signature \_ DESC (uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 root Signature Flags Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="12a09-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-113">Crea una nuova istanza di una \_ Descrizione della \_ firma radice CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a09-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="12a09-114">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="12a09-114">UINT numParameters</span></span>

<span data-ttu-id="12a09-115">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="12a09-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="12a09-116">consenso esplicito UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="12a09-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="12a09-117">consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="12a09-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="12a09-118">consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="12a09-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="12a09-119">**\_Firma radice \_ CD3DX12 \_ DESC ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="12a09-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-120">Crea una nuova istanza di una \_ firma radice \_ CD3DX12 \_ DESC, inizializzata con parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="12a09-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="12a09-121">**inline init (UINT numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ root Signature Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="12a09-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-122">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a09-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="12a09-123">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="12a09-123">UINT numParameters</span></span>

<span data-ttu-id="12a09-124">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="12a09-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="12a09-125">consenso esplicito UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="12a09-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="12a09-126">consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="12a09-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="12a09-127">consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="12a09-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="12a09-128">**static inline init (D3D12 \_ root \_ signature \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ flag firma radice Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="12a09-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="12a09-129">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a09-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="12a09-130">[**D3D12 \_ Descrizione \_ della \_ firma radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="12a09-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="12a09-131">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="12a09-131">UINT numParameters</span></span>

<span data-ttu-id="12a09-132">[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="12a09-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="12a09-133">consenso esplicito UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="12a09-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="12a09-134">consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="12a09-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="12a09-135">consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="12a09-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12a09-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12a09-136">Requirements</span></span>



| <span data-ttu-id="12a09-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="12a09-137">Requirement</span></span> | <span data-ttu-id="12a09-138">Valore</span><span class="sxs-lookup"><span data-stu-id="12a09-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="12a09-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12a09-139">Header</span></span><br/> | <dl> <span data-ttu-id="12a09-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a09-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a09-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12a09-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a09-142">**\_Descrizione della \_ firma \_ radice D3D12**</span><span class="sxs-lookup"><span data-stu-id="12a09-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="12a09-143">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="12a09-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





