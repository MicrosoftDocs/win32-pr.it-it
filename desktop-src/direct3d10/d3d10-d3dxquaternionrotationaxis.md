---
description: Ruota un quaternione su un asse arbitrario.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: Funzione D3DXQuaternionRotationAxis (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 739f128ca1a56eed15ebc2528036875eaf2bb9b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323337"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="4cfa3-103">Funzione D3DXQuaternionRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4cfa3-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="4cfa3-104">Ruota un quaternione su un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfa3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cfa3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="4cfa3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cfa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfa3-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4cfa3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa3-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfa3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4cfa3-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4cfa3-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfa3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa3-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfa3-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfa3-112">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che identifica l'asse attorno al quale ruotare il quaternione.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="4cfa3-113">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfa3-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa3-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfa3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cfa3-115">Angolo di rotazione, in radianti.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="4cfa3-116">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfa3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cfa3-117">Return value</span></span>

<span data-ttu-id="4cfa3-118">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfa3-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4cfa3-119">Puntatore a una struttura D3DXQUATERNION ruotata intorno all'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfa3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cfa3-120">Remarks</span></span>

<span data-ttu-id="4cfa3-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4cfa3-122">In questo modo, la funzione D3DXQuaternionRotationAxis può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4cfa3-123">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfa3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cfa3-124">Requirements</span></span>



| <span data-ttu-id="4cfa3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfa3-125">Requirement</span></span> | <span data-ttu-id="4cfa3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4cfa3-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfa3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cfa3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfa3-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfa3-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4cfa3-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cfa3-129">Library</span></span><br/> | <dl> <span data-ttu-id="4cfa3-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cfa3-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4cfa3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cfa3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfa3-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4cfa3-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
