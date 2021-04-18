---
title: Struttura CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura Desc del rasterizzatore D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Struttura CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322218"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="ccf20-104">\_Struttura Desc del rasterizzatore CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="ccf20-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="ccf20-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ Desc del rasterizzatore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="ccf20-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf20-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf20-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="ccf20-107">Members</span><span class="sxs-lookup"><span data-stu-id="ccf20-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ccf20-108">**\_Rasterizzatore CD3DX12 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="ccf20-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-109">Crea un'istanza nuova, non inizializzata, di un \_ rasterizzatore CD3DX12 \_ desc.</span><span class="sxs-lookup"><span data-stu-id="ccf20-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ccf20-110">**rasterizzatore esplicito CD3DX12 \_ \_ DESC (const D3D12 \_ rasterizzator \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="ccf20-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-111">Crea una nuova istanza di una \_ Descrizione del rasterizzatore CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ desc di rasterizzazione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="ccf20-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ccf20-112">**rasterizzatore CD3DX12 esplicito \_ \_ DESC ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="ccf20-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-113">Crea una nuova istanza di una \_ Descrizione di rasterizzazione CD3DX12 \_ , inizializzata con parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ccf20-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="ccf20-114">**rasterizzazione CD3DX12 esplicita \_ \_ DESC ( \_ \_ modalità di riempimento D3D12 FillMode, \_ modalità di abbattimento D3D12 \_ CullMode, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float slopeScaledDepthBias, bool DepthClipEnable, bool multisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ Conservation \_ mode di rasterizzazione conservativeRaster \_ )**</span><span class="sxs-lookup"><span data-stu-id="ccf20-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-115">Crea una nuova istanza di una \_ Descrizione del rasterizzatore CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccf20-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="ccf20-116">[**D3D12 \_ FillMode \_ modalità riempimento**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)</span><span class="sxs-lookup"><span data-stu-id="ccf20-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="ccf20-117">[**D3D12 \_ CullMode \_ modalità di eliminazione**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)</span><span class="sxs-lookup"><span data-stu-id="ccf20-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="ccf20-118">BOOL frontCounterClockwise</span><span class="sxs-lookup"><span data-stu-id="ccf20-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="ccf20-119">INT depthBias</span><span class="sxs-lookup"><span data-stu-id="ccf20-119">INT depthBias</span></span>

<span data-ttu-id="ccf20-120">FLOAT depthBiasClamp</span><span class="sxs-lookup"><span data-stu-id="ccf20-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="ccf20-121">FLOAT slopeScaledDepthBias</span><span class="sxs-lookup"><span data-stu-id="ccf20-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="ccf20-122">BOOL depthClipEnable</span><span class="sxs-lookup"><span data-stu-id="ccf20-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="ccf20-123">BOOL multisampleEnable</span><span class="sxs-lookup"><span data-stu-id="ccf20-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="ccf20-124">BOOL antialiasedLineEnable</span><span class="sxs-lookup"><span data-stu-id="ccf20-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="ccf20-125">ForcedSampleCount UINT</span><span class="sxs-lookup"><span data-stu-id="ccf20-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="ccf20-126">[**D3D12 \_ \_ \_ Modalità di RASTERIZZAzione conservativa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span><span class="sxs-lookup"><span data-stu-id="ccf20-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="ccf20-127">**~ CD3DX12 \_ rasterizzatore \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="ccf20-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-128">Elimina un'istanza di una descrizione del \_ rasterizzatore CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="ccf20-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ccf20-129">**operator const D3D12 \_ rasterizzatore \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="ccf20-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-130">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="ccf20-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccf20-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf20-131">Requirements</span></span>



| <span data-ttu-id="ccf20-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf20-132">Requirement</span></span> | <span data-ttu-id="ccf20-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf20-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf20-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccf20-134">Header</span></span><br/> | <dl> <span data-ttu-id="ccf20-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf20-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf20-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf20-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf20-137">**D3D12 \_ rasterizzatore \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="ccf20-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="ccf20-138">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="ccf20-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





