---
description: Compila una matrice che ruota intorno all'asse x.
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: Funzione D3DXMatrixRotationX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5eade695a3b410877665557bd42d61d1d89b18e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323339"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="87192-103">Funzione D3DXMatrixRotationX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="87192-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="87192-104">Compila una matrice che ruota intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="87192-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="87192-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87192-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="87192-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87192-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87192-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="87192-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87192-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87192-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87192-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87192-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87192-110">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87192-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87192-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87192-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87192-112">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="87192-112">Angle of rotation in radians.</span></span> <span data-ttu-id="87192-113">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="87192-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87192-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87192-114">Return value</span></span>

<span data-ttu-id="87192-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87192-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87192-116">Puntatore a una struttura D3DXMATRIX ruotata intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="87192-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="87192-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="87192-117">Remarks</span></span>

<span data-ttu-id="87192-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="87192-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="87192-119">In questo modo, la funzione D3DXMatrixRotationX può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="87192-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="87192-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87192-120">Requirements</span></span>



| <span data-ttu-id="87192-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87192-121">Requirement</span></span> | <span data-ttu-id="87192-122">Valore</span><span class="sxs-lookup"><span data-stu-id="87192-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87192-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87192-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87192-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87192-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="87192-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="87192-125">Library</span></span><br/> | <dl> <span data-ttu-id="87192-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87192-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87192-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87192-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87192-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="87192-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
