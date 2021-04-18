---
title: Struttura CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura D3D12 depth stencil \_ desc.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Struttura CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322278"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="23fe6-104">\_Struttura CD3DX12 Depth \_ stencil \_ DESC</span><span class="sxs-lookup"><span data-stu-id="23fe6-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="23fe6-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="23fe6-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fe6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23fe6-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="23fe6-107">Members</span><span class="sxs-lookup"><span data-stu-id="23fe6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23fe6-108">**CD3DX12 \_ Depth \_ stencil \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="23fe6-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-109">Crea una nuova istanza non inizializzata di una \_ Descrizione di stencil Depth \_ D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="23fe6-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="23fe6-110">**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC (const D3D12 \_ Depth \_ stencil \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="23fe6-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-111">Crea una nuova istanza di D3DX12 \_ Depth \_ stencil \_ DESC, inizializzata con il contenuto di un'altra struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="23fe6-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="23fe6-112">**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="23fe6-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-113">Crea una nuova istanza di D3DX12 \_ Depth \_ stencil \_ DESC, inizializzata con parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="23fe6-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="23fe6-114">**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC (bool depthEnable, D3D12 \_ Depth \_ Write \_ mask depthWriteMask, D3D12 \_ Comparison \_ Func depthFunc, bool STENCILENABLE, Uint8 StencilReadMask, Uint8 stencilWriteMask, D3D12 \_ stencil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op FRONTSTENCILDEPTHFAILOP, D3D12 \_ stencil \_ op frontStencilPassOp, D3D12 \_ Comparison \_ Func frontStencilFunc, D3D12 \_ stencil \_ op backStencilFailOp, D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 \_ stencil \_ op backStencilPassOp, D3D12 \_ Comparison \_ Func backStencilFunc)**</span><span class="sxs-lookup"><span data-stu-id="23fe6-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-115">Crea una nuova istanza di una \_ desc D3DX12 Depth \_ stencil \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="23fe6-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="23fe6-116">BOOL depthEnable</span><span class="sxs-lookup"><span data-stu-id="23fe6-116">BOOL depthEnable</span></span>

<span data-ttu-id="23fe6-117">[**D3D12 \_ \_ \_ Maschera di scrittura profondità**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span><span class="sxs-lookup"><span data-stu-id="23fe6-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="23fe6-118">[**D3D12 \_ DepthFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)</span><span class="sxs-lookup"><span data-stu-id="23fe6-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="23fe6-119">BOOL stencilEnable</span><span class="sxs-lookup"><span data-stu-id="23fe6-119">BOOL stencilEnable</span></span>

<span data-ttu-id="23fe6-120">StencilReadMask UINT8</span><span class="sxs-lookup"><span data-stu-id="23fe6-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="23fe6-121">StencilWriteMask UINT8</span><span class="sxs-lookup"><span data-stu-id="23fe6-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="23fe6-122">[**D3D12 \_ FrontStencilFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="23fe6-123">[**D3D12 \_ FrontStencilDepthFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="23fe6-124">[**D3D12 \_ FrontStencilPassOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="23fe6-125">[**D3D12 \_ FrontStencilFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)</span><span class="sxs-lookup"><span data-stu-id="23fe6-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="23fe6-126">[**D3D12 \_ BackStencilFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="23fe6-127">[**D3D12 \_ BackStencilDepthFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="23fe6-128">[**D3D12 \_ BackStencilPassOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="23fe6-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="23fe6-129">[**D3D12 \_ BackStencilFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)</span><span class="sxs-lookup"><span data-stu-id="23fe6-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="23fe6-130">**~ CD3DX12 \_ Depth \_ stencil \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="23fe6-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-131">Elimina un'istanza di una desc CD3DX12 \_ Depth \_ stencil \_ .</span><span class="sxs-lookup"><span data-stu-id="23fe6-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="23fe6-132">**operator const D3D12 \_ Depth \_ STENCIL \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="23fe6-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="23fe6-133">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="23fe6-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23fe6-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23fe6-134">Requirements</span></span>



| <span data-ttu-id="23fe6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fe6-135">Requirement</span></span> | <span data-ttu-id="23fe6-136">Valore</span><span class="sxs-lookup"><span data-stu-id="23fe6-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23fe6-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23fe6-137">Header</span></span><br/> | <dl> <span data-ttu-id="23fe6-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fe6-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23fe6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23fe6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fe6-140">**D3D12 \_ Depth \_ stencil \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="23fe6-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="23fe6-141">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="23fe6-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





