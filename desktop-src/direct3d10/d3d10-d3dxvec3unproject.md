---
description: "Funzione D3DXVec3Unproject (D3DX10Math.h): proietta un vettore dallo spazio dello schermo allo spazio dell'oggetto."
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Funzione D3DXVec3Unproject (D3DX10Math.h)
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
ms.openlocfilehash: 08d38691d0e780e49293149bdb7a08b1ea0ef1fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103029"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="276c5-103">Funzione D3DXVec3Unproject (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="276c5-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="276c5-104">Proietta un vettore dallo spazio dello schermo nello spazio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="276c5-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="276c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="276c5-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="276c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="276c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276c5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="276c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="276c5-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="276c5-109">Puntatore [**all'oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="276c5-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="276c5-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="276c5-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="276c5-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="276c5-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="276c5-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="276c5-113">*pViewport* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="276c5-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-114">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="276c5-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="276c5-115">Puntatore a [**un \_ VIEWPORT D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="276c5-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="276c5-116">*pProjection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="276c5-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="276c5-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="276c5-118">Puntatore a una [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="276c5-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="276c5-119">*pView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="276c5-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="276c5-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="276c5-121">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="276c5-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="276c5-122">*pWorld* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="276c5-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276c5-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="276c5-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="276c5-124">Puntatore a una struttura D3DXMATRIX, che rappresenta la matrice globale.</span><span class="sxs-lookup"><span data-stu-id="276c5-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276c5-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="276c5-125">Return value</span></span>

<span data-ttu-id="276c5-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="276c5-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="276c5-127">Puntatore a una struttura D3DXVECTOR3 che rappresenta il vettore proiettato dallo spazio dello schermo allo spazio oggetto.</span><span class="sxs-lookup"><span data-stu-id="276c5-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="276c5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="276c5-128">Remarks</span></span>

<span data-ttu-id="276c5-129">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="276c5-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="276c5-130">In questo modo, la funzione D3DXVec3Unproject può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="276c5-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="276c5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="276c5-131">Requirements</span></span>



| <span data-ttu-id="276c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="276c5-132">Requirement</span></span> | <span data-ttu-id="276c5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="276c5-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="276c5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="276c5-134">Header</span></span><br/> | <dl> <span data-ttu-id="276c5-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="276c5-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="276c5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="276c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276c5-137">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="276c5-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
