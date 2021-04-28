---
description: "Funzione D3DXVec3ProjectArray (D3DX10Math.h): proietta una matrice (x, y, z, 0) dallo spazio dell'oggetto allo spazio dello schermo."
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: Funzione D3DXVec3ProjectArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1f69eb14cf2cf5fd77092ed6881e16524d8428c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108149"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a><span data-ttu-id="7190a-103">Funzione D3DXVec3ProjectArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7190a-103">D3DXVec3ProjectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="7190a-104">Proietta una matrice (x, y, z, 0) dallo spazio dell'oggetto nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7190a-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="7190a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7190a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
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



## <a name="parameters"></a><span data-ttu-id="7190a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7190a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7190a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7190a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7190a-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7190a-109">Puntatore [**all'oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7190a-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7190a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7190a-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="7190a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7190a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7190a-115">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="7190a-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7190a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7190a-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="7190a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-119">*pViewport* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-120">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="7190a-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="7190a-121">Puntatore a [**un \_ VIEWPORT D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="7190a-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-122">*pProjection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7190a-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7190a-124">Puntatore a una [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="7190a-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-125">*pView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7190a-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7190a-127">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7190a-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-128">*pWorld* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7190a-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7190a-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7190a-130">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice globale.</span><span class="sxs-lookup"><span data-stu-id="7190a-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="7190a-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7190a-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190a-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7190a-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7190a-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7190a-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7190a-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7190a-134">Return value</span></span>

<span data-ttu-id="7190a-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7190a-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7190a-136">Puntatore a una struttura D3DXVECTOR3 che rappresenta la matrice proiettata dallo spazio dell'oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7190a-136">Pointer to a D3DXVECTOR3 structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="7190a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="7190a-137">Remarks</span></span>

<span data-ttu-id="7190a-138">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="7190a-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7190a-139">In questo modo, la funzione D3DXVec3ProjectArray può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7190a-139">In this way, the D3DXVec3ProjectArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7190a-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7190a-140">Requirements</span></span>



| <span data-ttu-id="7190a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7190a-141">Requirement</span></span> | <span data-ttu-id="7190a-142">Valore</span><span class="sxs-lookup"><span data-stu-id="7190a-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7190a-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7190a-143">Header</span></span><br/> | <dl> <span data-ttu-id="7190a-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7190a-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7190a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7190a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7190a-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7190a-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
