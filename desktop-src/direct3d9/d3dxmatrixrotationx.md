---
description: "Funzione D3DXMatrixRotationX (D3dx9math.h): compila una matrice che ruota intorno all'asse x."
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: Funzione D3DXMatrixRotationX (D3dx9math.h)
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
ms.openlocfilehash: a4f51f8acab7caddd4571d60f7deae795440f02a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118179"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a><span data-ttu-id="8c54a-103">Funzione D3DXMatrixRotationX (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8c54a-103">D3DXMatrixRotationX function (D3dx9math.h)</span></span>

<span data-ttu-id="8c54a-104">Compila una matrice che ruota intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="8c54a-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c54a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c54a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="8c54a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c54a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8c54a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c54a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c54a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c54a-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8c54a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c54a-110">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8c54a-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c54a-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c54a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c54a-112">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="8c54a-112">Angle of rotation in radians.</span></span> <span data-ttu-id="8c54a-113">Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="8c54a-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c54a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c54a-114">Return value</span></span>

<span data-ttu-id="8c54a-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c54a-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c54a-116">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) ruotata intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="8c54a-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c54a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c54a-117">Remarks</span></span>

<span data-ttu-id="8c54a-118">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="8c54a-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c54a-119">In questo modo, la **funzione D3DXMatrixRotationX** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8c54a-119">In this way, the **D3DXMatrixRotationX** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c54a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c54a-120">Requirements</span></span>



| <span data-ttu-id="8c54a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c54a-121">Requirement</span></span> | <span data-ttu-id="8c54a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8c54a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c54a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c54a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8c54a-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c54a-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c54a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c54a-125">Library</span></span><br/> | <dl> <span data-ttu-id="8c54a-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c54a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c54a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c54a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c54a-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8c54a-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c54a-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="8c54a-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="8c54a-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="8c54a-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="8c54a-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="8c54a-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="8c54a-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="8c54a-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="8c54a-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="8c54a-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
