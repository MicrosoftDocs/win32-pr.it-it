---
description: Compila una matrice che ruota intorno all'asse x.
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: Funzione D3DXMatrixRotationX (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1d3dd85a4cd0e5f9e668856a4d6d2f87bbdf108
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401924"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a><span data-ttu-id="93f38-103">Funzione D3DXMatrixRotationX (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="93f38-103">D3DXMatrixRotationX function (D3dx9math.h)</span></span>

<span data-ttu-id="93f38-104">Compila una matrice che ruota intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="93f38-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93f38-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="93f38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f38-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="93f38-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93f38-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="93f38-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93f38-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="93f38-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93f38-110">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93f38-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f38-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93f38-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93f38-112">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="93f38-112">Angle of rotation in radians.</span></span> <span data-ttu-id="93f38-113">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="93f38-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f38-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93f38-114">Return value</span></span>

<span data-ttu-id="93f38-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="93f38-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93f38-116">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) ruotata intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="93f38-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f38-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="93f38-117">Remarks</span></span>

<span data-ttu-id="93f38-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="93f38-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="93f38-119">In questo modo, la funzione **D3DXMatrixRotationX** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="93f38-119">In this way, the **D3DXMatrixRotationX** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f38-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93f38-120">Requirements</span></span>



| <span data-ttu-id="93f38-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f38-121">Requirement</span></span> | <span data-ttu-id="93f38-122">Valore</span><span class="sxs-lookup"><span data-stu-id="93f38-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f38-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93f38-123">Header</span></span><br/>  | <dl> <span data-ttu-id="93f38-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f38-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="93f38-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="93f38-125">Library</span></span><br/> | <dl> <span data-ttu-id="93f38-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93f38-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93f38-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93f38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f38-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="93f38-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="93f38-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="93f38-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="93f38-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="93f38-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="93f38-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="93f38-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="93f38-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="93f38-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="93f38-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="93f38-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
