---
description: 'Funzione D3DXMatrixRotationAxis (D3DX10Math.h): compila una matrice che ruota intorno a un asse arbitrario.'
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Funzione D3DXMatrixRotationAxis (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ea5b8b0a40e876af454daa8915c0e455d691d08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108999"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="f16a2-103">Funzione D3DXMatrixRotationAxis (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f16a2-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="f16a2-104">Compila una matrice che ruota intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f16a2-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f16a2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="f16a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f16a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16a2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f16a2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16a2-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f16a2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f16a2-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f16a2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f16a2-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f16a2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16a2-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f16a2-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f16a2-112">Puntatore all'asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f16a2-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="f16a2-113">Vedere [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="f16a2-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="f16a2-114">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f16a2-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16a2-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f16a2-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f16a2-116">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="f16a2-116">Angle of rotation in radians.</span></span> <span data-ttu-id="f16a2-117">Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="f16a2-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16a2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f16a2-118">Return value</span></span>

<span data-ttu-id="f16a2-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f16a2-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f16a2-120">Puntatore a una struttura D3DXMATRIX ruotata intorno all'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="f16a2-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="f16a2-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f16a2-121">Remarks</span></span>

<span data-ttu-id="f16a2-122">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="f16a2-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f16a2-123">In questo modo, la funzione D3DXMatrixRotationAxis può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f16a2-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16a2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f16a2-124">Requirements</span></span>



| <span data-ttu-id="f16a2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16a2-125">Requirement</span></span> | <span data-ttu-id="f16a2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f16a2-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16a2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f16a2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f16a2-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f16a2-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f16a2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="f16a2-129">Library</span></span><br/> | <dl> <span data-ttu-id="f16a2-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f16a2-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f16a2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f16a2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16a2-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f16a2-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
