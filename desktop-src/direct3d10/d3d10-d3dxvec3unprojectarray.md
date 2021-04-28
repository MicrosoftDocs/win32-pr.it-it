---
description: 'Funzione D3DXVec3UnprojectArray (D3DX10Math.h): proietta una matrice (x, y, z, 0) dallo spazio dello schermo allo spazio oggetto.'
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Funzione D3DXVec3UnprojectArray (D3DX10Math.h)
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
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103009"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="fe7ac-103">Funzione D3DXVec3UnprojectArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="fe7ac-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="fe7ac-104">Proietta una matrice (x, y, z, 0) dallo spazio dello schermo allo spazio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe7ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe7ac-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fe7ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe7ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe7ac-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe7ac-109">Puntatore [**all'oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe7ac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe7ac-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe7ac-115">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe7ac-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe7ac-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-119">*pViewport* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-120">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="fe7ac-121">Puntatore a [**un \_ VIEWPORT D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-122">*pProjection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe7ac-124">Puntatore a [**una struttura D3DXMATRIX,**](d3d10-d3dxmatrix.md) che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-125">*pView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe7ac-127">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-128">*pWorld* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe7ac-130">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice globale.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ac-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe7ac-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7ac-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe7ac-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe7ac-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe7ac-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe7ac-134">Return value</span></span>

<span data-ttu-id="fe7ac-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe7ac-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe7ac-136">Puntatore a una struttura D3DXVECTOR3 che rappresenta la matrice proiettata dallo spazio dello schermo allo spazio oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe7ac-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe7ac-137">Remarks</span></span>

<span data-ttu-id="fe7ac-138">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fe7ac-139">In questo modo, la [**funzione D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="fe7ac-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7ac-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe7ac-140">Requirements</span></span>



| <span data-ttu-id="fe7ac-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe7ac-141">Requirement</span></span> | <span data-ttu-id="fe7ac-142">Valore</span><span class="sxs-lookup"><span data-stu-id="fe7ac-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7ac-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe7ac-143">Header</span></span><br/> | <dl> <span data-ttu-id="fe7ac-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ac-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe7ac-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe7ac-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7ac-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fe7ac-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
