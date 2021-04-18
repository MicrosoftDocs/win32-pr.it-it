---
description: Proietta una matrice (x, y, z,0) dallo spazio dello schermo nello spazio degli oggetti.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Funzione D3DXVec3UnprojectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c7293339145253f817e8ed8b6812906b49792193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322389"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="e4985-103">Funzione D3DXVec3UnprojectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e4985-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="e4985-104">Proietta una matrice (x, y, z,0) dallo spazio dello schermo nello spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="e4985-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4985-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4985-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="e4985-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4985-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e4985-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4985-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4985-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e4985-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4985-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4985-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="e4985-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4985-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4985-115">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="e4985-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4985-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4985-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="e4985-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-119">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-120">Tipo: **const [**D3D10 \_ viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="e4985-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="e4985-121">Puntatore a un [**\_ viewport D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="e4985-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-122">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4985-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4985-124">Puntatore a una struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="e4985-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-125">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4985-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4985-127">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e4985-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-128">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4985-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4985-130">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="e4985-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4985-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4985-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4985-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4985-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4985-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="e4985-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4985-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4985-134">Return value</span></span>

<span data-ttu-id="e4985-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4985-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4985-136">Puntatore a una struttura D3DXVECTOR3 che rappresenta la matrice proiettata dallo spazio dello schermo allo spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="e4985-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4985-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4985-137">Remarks</span></span>

<span data-ttu-id="e4985-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="e4985-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e4985-139">In questo modo, la funzione [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e4985-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4985-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4985-140">Requirements</span></span>



| <span data-ttu-id="e4985-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4985-141">Requirement</span></span> | <span data-ttu-id="e4985-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e4985-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4985-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4985-143">Header</span></span><br/> | <dl> <span data-ttu-id="e4985-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4985-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4985-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4985-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4985-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e4985-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
