---
description: "Funzione D3DXMatrixRotationY (D3dx9math.h): compila una matrice che ruota intorno all'asse y."
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: Funzione D3DXMatrixRotationY (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 902325890b02416e796940388bca7a6548773be5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118129"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="fe3cb-103">Funzione D3DXMatrixRotationY (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fe3cb-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="fe3cb-104">Compila una matrice che ruota intorno all'asse y.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe3cb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="fe3cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe3cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3cb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe3cb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3cb-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe3cb-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe3cb-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe3cb-110">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe3cb-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3cb-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe3cb-112">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-112">Angle of rotation in radians.</span></span> <span data-ttu-id="fe3cb-113">Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3cb-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe3cb-114">Return value</span></span>

<span data-ttu-id="fe3cb-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe3cb-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe3cb-116">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) ruotata intorno all'asse y.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3cb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe3cb-117">Remarks</span></span>

<span data-ttu-id="fe3cb-118">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="fe3cb-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fe3cb-119">In questo modo, la **funzione D3DXMatrixRotationY** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="fe3cb-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3cb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe3cb-120">Requirements</span></span>



| <span data-ttu-id="fe3cb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe3cb-121">Requirement</span></span> | <span data-ttu-id="fe3cb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fe3cb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3cb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe3cb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fe3cb-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3cb-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe3cb-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe3cb-125">Library</span></span><br/> | <dl> <span data-ttu-id="fe3cb-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe3cb-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe3cb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe3cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3cb-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fe3cb-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fe3cb-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="fe3cb-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="fe3cb-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="fe3cb-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="fe3cb-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="fe3cb-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
