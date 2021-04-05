---
description: Compila una matrice che ruota intorno a un asse arbitrario.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Funzione D3DXMatrixRotationAxis (D3DX10Math. h)
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
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058668"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="52c11-103">Funzione D3DXMatrixRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="52c11-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="52c11-104">Compila una matrice che ruota intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="52c11-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52c11-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="52c11-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c11-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="52c11-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52c11-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="52c11-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="52c11-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="52c11-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="52c11-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52c11-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c11-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="52c11-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="52c11-112">Puntatore all'asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="52c11-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="52c11-113">Vedere [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="52c11-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="52c11-114">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52c11-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c11-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52c11-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52c11-116">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="52c11-116">Angle of rotation in radians.</span></span> <span data-ttu-id="52c11-117">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="52c11-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c11-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52c11-118">Return value</span></span>

<span data-ttu-id="52c11-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="52c11-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="52c11-120">Puntatore a una struttura D3DXMATRIX ruotata intorno all'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="52c11-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c11-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c11-121">Remarks</span></span>

<span data-ttu-id="52c11-122">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="52c11-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="52c11-123">In questo modo, la funzione D3DXMatrixRotationAxis può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="52c11-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c11-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c11-124">Requirements</span></span>



| <span data-ttu-id="52c11-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c11-125">Requirement</span></span> | <span data-ttu-id="52c11-126">Valore</span><span class="sxs-lookup"><span data-stu-id="52c11-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52c11-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52c11-127">Header</span></span><br/>  | <dl> <span data-ttu-id="52c11-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c11-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="52c11-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="52c11-129">Library</span></span><br/> | <dl> <span data-ttu-id="52c11-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52c11-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52c11-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52c11-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c11-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="52c11-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
