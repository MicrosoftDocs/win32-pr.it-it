---
description: Proietta un vettore dallo spazio dello schermo nello spazio degli oggetti.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Funzione D3DXVec3Unproject (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322958"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="0491b-103">Funzione D3DXVec3Unproject (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0491b-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="0491b-104">Proietta un vettore dallo spazio dello schermo nello spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="0491b-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="0491b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0491b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="0491b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0491b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0491b-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0491b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0491b-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0491b-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0491b-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0491b-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0491b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0491b-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0491b-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="0491b-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="0491b-113">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0491b-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-114">Tipo: **const [**D3D10 \_ viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="0491b-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="0491b-115">Puntatore a un [**\_ viewport D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="0491b-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="0491b-116">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0491b-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0491b-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0491b-118">Puntatore a una struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="0491b-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0491b-119">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0491b-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0491b-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0491b-121">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0491b-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0491b-122">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0491b-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0491b-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0491b-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0491b-124">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="0491b-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0491b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0491b-125">Return value</span></span>

<span data-ttu-id="0491b-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0491b-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0491b-127">Puntatore a una struttura D3DXVECTOR3 che rappresenta il vettore proiettato dallo spazio dello schermo allo spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="0491b-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="0491b-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="0491b-128">Remarks</span></span>

<span data-ttu-id="0491b-129">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="0491b-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0491b-130">In questo modo, la funzione D3DXVec3Unproject può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0491b-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0491b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0491b-131">Requirements</span></span>



| <span data-ttu-id="0491b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0491b-132">Requirement</span></span> | <span data-ttu-id="0491b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0491b-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0491b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0491b-134">Header</span></span><br/> | <dl> <span data-ttu-id="0491b-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0491b-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0491b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0491b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0491b-137">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0491b-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
