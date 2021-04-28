---
description: 'Funzione D3DXMatrixRotationAxis (D3dx9math.h): compila una matrice che ruota intorno a un asse arbitrario.'
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: Funzione D3DXMatrixRotationAxis (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118189"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="1e65a-103">Funzione D3DXMatrixRotationAxis (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1e65a-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="1e65a-104">Compila una matrice che ruota intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="1e65a-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e65a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e65a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="1e65a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e65a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e65a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e65a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e65a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e65a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1e65a-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1e65a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e65a-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1e65a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e65a-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e65a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1e65a-112">Puntatore all'asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="1e65a-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="1e65a-113">Vedere [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="1e65a-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e65a-114">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1e65a-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e65a-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e65a-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e65a-116">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="1e65a-116">Angle of rotation in radians.</span></span> <span data-ttu-id="1e65a-117">Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="1e65a-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e65a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e65a-118">Return value</span></span>

<span data-ttu-id="1e65a-119">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e65a-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1e65a-120">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) ruotata intorno all'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="1e65a-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e65a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e65a-121">Remarks</span></span>

<span data-ttu-id="1e65a-122">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1e65a-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1e65a-123">In questo modo, la **funzione D3DXMatrixRotationAxis** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1e65a-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e65a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e65a-124">Requirements</span></span>



| <span data-ttu-id="1e65a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e65a-125">Requirement</span></span> | <span data-ttu-id="1e65a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1e65a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e65a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e65a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1e65a-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e65a-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1e65a-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="1e65a-129">Library</span></span><br/> | <dl> <span data-ttu-id="1e65a-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e65a-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e65a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e65a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e65a-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1e65a-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1e65a-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="1e65a-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="1e65a-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="1e65a-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="1e65a-135">**D3DXMatrixRotationy**</span><span class="sxs-lookup"><span data-stu-id="1e65a-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="1e65a-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="1e65a-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="1e65a-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="1e65a-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
