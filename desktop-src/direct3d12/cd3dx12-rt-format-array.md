---
title: Struttura CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di matrici di formato D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Struttura CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323553"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="e017f-104">\_Struttura della \_ matrice di formato CD3DX12 RT \_</span><span class="sxs-lookup"><span data-stu-id="e017f-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="e017f-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="e017f-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e017f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e017f-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="e017f-107">Members</span><span class="sxs-lookup"><span data-stu-id="e017f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e017f-108">**CD3DX12 \_ RT \_ Format \_ Array ()**</span><span class="sxs-lookup"><span data-stu-id="e017f-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="e017f-109">Crea una nuova istanza non inizializzata di una \_ matrice di formato CD3DX12 \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="e017f-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="e017f-110">**matrice di \_ formato CD3DX12 RT esplicita \_ \_ (const D3D12 \_ RT \_ Format \_ Array& o)**</span><span class="sxs-lookup"><span data-stu-id="e017f-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="e017f-111">Crea una nuova istanza di una \_ matrice di formato CD3DX12 RT \_ \_ , inizializzata con i valori copiati da una struttura di [**\_ \_ \_ matrice di formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="e017f-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e017f-112">**matrice di \_ formato CD3DX12 RT esplicita \_ \_ (const DXGI \_ Format \* pFormats, uint NumFormats)**</span><span class="sxs-lookup"><span data-stu-id="e017f-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="e017f-113">Crea una nuova istanza di una \_ matrice di formato CD3DX12 RT \_ \_ , inizializzata con i valori passati nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="e017f-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="e017f-114">Il contenuto della matrice specificata dal parametro *pFormats* viene copiato nella matrice membro **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="e017f-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="e017f-115">Si presuppone che la matrice specificata da *pFormats* abbia le stesse dimensioni di **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="e017f-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="e017f-116">**operatore const D3D12 \_ RT \_ FORMAT \_ Array& () const**</span><span class="sxs-lookup"><span data-stu-id="e017f-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e017f-117">Conversione implicita in una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="e017f-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="e017f-118">Poiché D3D12 \_ RT \_ Format \_ Array è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, l'oggetto viene semplicemente restituito come \_ \_ riferimento alla matrice di formato const D3D12 RT \_ a se stesso.</span><span class="sxs-lookup"><span data-stu-id="e017f-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e017f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e017f-119">Requirements</span></span>



| <span data-ttu-id="e017f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e017f-120">Requirement</span></span> | <span data-ttu-id="e017f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e017f-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e017f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e017f-122">Header</span></span><br/> | <dl> <span data-ttu-id="e017f-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e017f-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e017f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e017f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e017f-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="e017f-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e017f-126">**\_Matrice di \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="e017f-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





