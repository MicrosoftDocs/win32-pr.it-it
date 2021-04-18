---
title: Struttura CD3DX12_BLEND_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura desc di D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Struttura CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322284"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="6ebb5-104">\_ \_ Struttura desc di CD3DX12 Blend</span><span class="sxs-lookup"><span data-stu-id="6ebb5-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="6ebb5-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc di D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="6ebb5-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebb5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ebb5-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="6ebb5-107">Members</span><span class="sxs-lookup"><span data-stu-id="6ebb5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ebb5-108">**CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6ebb5-109">Crea una nuova istanza non inizializzata di una \_ Descrizione di Blend CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6ebb5-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6ebb5-110">**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="6ebb5-111">Crea una nuova istanza di CD3DX12 \_ Blend \_ DESC, inizializzata con il contenuto di un'altra struttura di [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="6ebb5-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ebb5-112">**Explicit CD3DX12 \_ Blend \_ DESC ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="6ebb5-113">Crea una nuova istanza di CD3DX12 \_ Blend \_ DESC, inizializzata con parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6ebb5-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="6ebb5-114">State</span><span class="sxs-lookup"><span data-stu-id="6ebb5-114">State</span></span>                                   | <span data-ttu-id="6ebb5-115">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="6ebb5-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="6ebb5-116">AlphaToCoverageEnable</span><span class="sxs-lookup"><span data-stu-id="6ebb5-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="6ebb5-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-117">**FALSE**</span></span>                        |
| <span data-ttu-id="6ebb5-118">IndependentBlendEnable</span><span class="sxs-lookup"><span data-stu-id="6ebb5-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="6ebb5-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-119">**FALSE**</span></span>                        |
| <span data-ttu-id="6ebb5-120">RenderTarget \[ 0 \] . BlendEnable</span><span class="sxs-lookup"><span data-stu-id="6ebb5-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="6ebb5-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-121">**FALSE**</span></span>                        |
| <span data-ttu-id="6ebb5-122">RenderTarget \[ 0 \] . LogicOpEnable</span><span class="sxs-lookup"><span data-stu-id="6ebb5-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="6ebb5-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-123">**FALSE**</span></span>                        |
| <span data-ttu-id="6ebb5-124">RenderTarget \[ 0 \] . SrcBlend</span><span class="sxs-lookup"><span data-stu-id="6ebb5-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="6ebb5-125">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="6ebb5-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="6ebb5-126">RenderTarget \[ 0 \] . DestBlend</span><span class="sxs-lookup"><span data-stu-id="6ebb5-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="6ebb5-127">D3D12 \_ Blend \_ zero</span><span class="sxs-lookup"><span data-stu-id="6ebb5-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="6ebb5-128">RenderTarget \[ 0 \] . BlendOp</span><span class="sxs-lookup"><span data-stu-id="6ebb5-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="6ebb5-129">D3D12 \_ Blend \_ op \_ Add</span><span class="sxs-lookup"><span data-stu-id="6ebb5-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="6ebb5-130">RenderTarget \[ 0 \] . SrcBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="6ebb5-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="6ebb5-131">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="6ebb5-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="6ebb5-132">RenderTarget \[ 0 \] . DestBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="6ebb5-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="6ebb5-133">D3D12 \_ Blend \_ zero</span><span class="sxs-lookup"><span data-stu-id="6ebb5-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="6ebb5-134">RenderTarget \[ 0 \] . BlendOpAlpha</span><span class="sxs-lookup"><span data-stu-id="6ebb5-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="6ebb5-135">D3D12 \_ Blend \_ op \_ Add</span><span class="sxs-lookup"><span data-stu-id="6ebb5-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="6ebb5-136">RenderTarget \[ 0 \] . LogicOp</span><span class="sxs-lookup"><span data-stu-id="6ebb5-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="6ebb5-137">\_ \_ NoOp op per la logica D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="6ebb5-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="6ebb5-138">RenderTarget \[ 0 \] . RenderTargetWriteMask</span><span class="sxs-lookup"><span data-stu-id="6ebb5-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="6ebb5-139">D3D12 \_ Color \_ Write \_ Abilita \_ tutto</span><span class="sxs-lookup"><span data-stu-id="6ebb5-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="6ebb5-140">**~ CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6ebb5-141">Elimina un'istanza di una descrizione di \_ Blend CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6ebb5-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6ebb5-142">**operator const D3D12 \_ Blend \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6ebb5-143">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="6ebb5-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ebb5-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ebb5-144">Requirements</span></span>



| <span data-ttu-id="6ebb5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebb5-145">Requirement</span></span> | <span data-ttu-id="6ebb5-146">Valore</span><span class="sxs-lookup"><span data-stu-id="6ebb5-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebb5-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ebb5-147">Header</span></span><br/> | <dl> <span data-ttu-id="6ebb5-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebb5-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebb5-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ebb5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebb5-150">**D3D12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6ebb5-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="6ebb5-151">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="6ebb5-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





