---
description: 'Funzione D3DXMatrixRotationQuaternion (D3dx9math.h): compila una matrice di rotazione da un quaternione.'
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Funzione D3DXMatrixRotationQuaternion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118199"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="7511f-103">Funzione D3DXMatrixRotationQuaternion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="7511f-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="7511f-104">Compila una matrice di rotazione da un quaternione.</span><span class="sxs-lookup"><span data-stu-id="7511f-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7511f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7511f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="7511f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7511f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7511f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7511f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7511f-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7511f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7511f-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7511f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7511f-110">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7511f-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7511f-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7511f-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7511f-112">Puntatore alla struttura [**D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="7511f-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7511f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7511f-113">Return value</span></span>

<span data-ttu-id="7511f-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7511f-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7511f-115">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) compilata dal quaternione di origine.</span><span class="sxs-lookup"><span data-stu-id="7511f-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="7511f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7511f-116">Remarks</span></span>

<span data-ttu-id="7511f-117">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="7511f-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7511f-118">In questo modo, la **funzione D3DXMatrixRotationQuaternion** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7511f-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7511f-119">Per informazioni su come calcolare i valori del quaternione da un vettore di direzione ( x, y, z ) e un angolo di rotazione, vedere [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="7511f-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7511f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7511f-120">Requirements</span></span>



| <span data-ttu-id="7511f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7511f-121">Requirement</span></span> | <span data-ttu-id="7511f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7511f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7511f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7511f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7511f-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7511f-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7511f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7511f-125">Library</span></span><br/> | <dl> <span data-ttu-id="7511f-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7511f-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7511f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7511f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7511f-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7511f-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7511f-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7511f-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="7511f-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="7511f-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="7511f-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="7511f-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="7511f-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7511f-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="7511f-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="7511f-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




