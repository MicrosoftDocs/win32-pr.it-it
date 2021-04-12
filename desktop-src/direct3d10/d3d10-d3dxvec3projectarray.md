---
description: Proietta una matrice (x, y, z,0) dallo spazio dell'oggetto nello spazio dello schermo.
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: Funzione D3DXVec3ProjectArray (D3DX10Math. h)
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
ms.openlocfilehash: bdbda9201d23a6c525dc054c53874c71d548e65e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355384"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a><span data-ttu-id="1b271-103">Funzione D3DXVec3ProjectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1b271-103">D3DXVec3ProjectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="1b271-104">Proietta una matrice (x, y, z,0) dallo spazio dell'oggetto nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1b271-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b271-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b271-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1b271-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b271-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1b271-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b271-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b271-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1b271-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b271-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b271-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="1b271-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b271-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b271-115">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="1b271-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b271-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b271-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="1b271-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-119">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-120">Tipo: **const [**D3D10 \_ viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="1b271-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="1b271-121">Puntatore a un [**\_ viewport D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="1b271-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-122">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b271-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1b271-124">Puntatore a una struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="1b271-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-125">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b271-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1b271-127">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b271-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-128">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b271-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1b271-130">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="1b271-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1b271-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b271-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b271-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b271-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b271-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1b271-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b271-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b271-134">Return value</span></span>

<span data-ttu-id="1b271-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b271-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b271-136">Puntatore a una struttura D3DXVECTOR3 che rappresenta la matrice proiettata dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1b271-136">Pointer to a D3DXVECTOR3 structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b271-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b271-137">Remarks</span></span>

<span data-ttu-id="1b271-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="1b271-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1b271-139">In questo modo, la funzione D3DXVec3ProjectArray può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1b271-139">In this way, the D3DXVec3ProjectArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b271-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b271-140">Requirements</span></span>



| <span data-ttu-id="1b271-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b271-141">Requirement</span></span> | <span data-ttu-id="1b271-142">Valore</span><span class="sxs-lookup"><span data-stu-id="1b271-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b271-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b271-143">Header</span></span><br/> | <dl> <span data-ttu-id="1b271-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b271-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b271-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b271-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b271-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1b271-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
