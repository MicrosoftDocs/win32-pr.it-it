---
title: Struttura CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura DESC1 di D3D12 Depth \_ stencil \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Struttura CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322274"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="8ea5e-104">\_ \_ Struttura DESC1 dello stencil CD3DX12 Depth \_</span><span class="sxs-lookup"><span data-stu-id="8ea5e-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="8ea5e-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**DESC1 di D3D12 \_ Depth \_ stencil \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="8ea5e-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea5e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ea5e-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="8ea5e-107">Members</span><span class="sxs-lookup"><span data-stu-id="8ea5e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ea5e-108">**\_Stencil Depth \_ CD3DX12 \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-109">Crea una nuova istanza non inizializzata di uno \_ stencil di profondità CD3DX12 \_ \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-110">**Explicit CD3DX12 \_ Depth \_ stencil \_ DESC1 (const D3D12 \_ Depth \_ stencil \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-111">Crea una nuova istanza di uno \_ stencil Depth \_ CD3DX12 \_ DESC1, inizializzato con i valori copiati da una struttura [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="8ea5e-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-112">**Explicit CD3DX12 \_ Depth \_ stencil \_ DESC1 (const D3D12 \_ Depth \_ stencil \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-113">Crea una nuova istanza di uno \_ stencil Depth \_ CD3DX12 \_ DESC1, inizializzato con i valori copiati da una struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="8ea5e-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="8ea5e-114">e il membro **DepthBoundsTestEnable** aggiuntivo impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-115">**DESC1 esplicito CD3DX12 \_ Depth \_ stencil \_ (CD3DX12 \_ predefinito)**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-116">Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzato con lo stato predefinito prescritto da D3DX12:</span><span class="sxs-lookup"><span data-stu-id="8ea5e-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="8ea5e-117">**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC1 (bool depthEnable, D3D12 \_ Depth \_ Write \_ mask depthWriteMask, D3D12 \_ Comparison \_ Func depthFunc, bool STENCILENABLE, Uint8 StencilReadMask, Uint8 stencilWriteMask, D3D12 \_ stencil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op FRONTSTENCILDEPTHFAILOP, D3D12 \_ stencil \_ op frontStencilPassOp, D3D12 \_ Comparison \_ Func frontStencilFunc, D3D12 \_ stencil \_ op BackStencilFailOp, D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 \_ stencil \_ op backStencilPassOp, D3D12 \_ Comparison \_ Func backStencilFunc, bool depthBoundsTestEnable)**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-118">Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-119">**~ CD3DX12 \_ Depth \_ stencil \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-120">Elimina un'istanza di uno stencil di \_ profondità \_ D3DX12 \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-121">**operatore const D3D12 \_ Depth \_ STENCIL \_ DESC1& () const**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-122">Conversione implicita in una \_ struttura DESC1 di D3D12 Depth \_ stencil \_ .</span><span class="sxs-lookup"><span data-stu-id="8ea5e-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="8ea5e-123">Poiché D3D12 \_ Depth \_ stencil \_ DESC1 è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, l'oggetto viene semplicemente restituito come un riferimento a un D3D12 di profondità const DESC1 \_ \_ \_ a se stesso.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5e-124">**operator const D3D12 \_ Depth \_ stencil \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-125">Conversione implicita in un \_ valore della struttura desc di D3D12 Depth \_ stencil \_ .</span><span class="sxs-lookup"><span data-stu-id="8ea5e-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="8ea5e-126">Poiché D3D12 \_ Depth \_ stencil \_ DESC non è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, viene creata una nuova istanza di D3D12 \_ Depth \_ stencil \_ DESC, che viene restituita per valore.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="8ea5e-127">Si noti che D3D12 \_ Depth \_ stencil DESC non \_ include il membro **DepthBoundsTestEnable** , quindi questo valore viene perso nella conversione.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ea5e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ea5e-128">Requirements</span></span>



| <span data-ttu-id="8ea5e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea5e-129">Requirement</span></span> | <span data-ttu-id="8ea5e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8ea5e-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea5e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ea5e-131">Header</span></span><br/> | <dl> <span data-ttu-id="8ea5e-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea5e-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea5e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ea5e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea5e-134">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="8ea5e-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8ea5e-135">**\_Stencil profondità \_ D3D12 \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="8ea5e-136">**D3D12 \_ Depth \_ stencil \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





