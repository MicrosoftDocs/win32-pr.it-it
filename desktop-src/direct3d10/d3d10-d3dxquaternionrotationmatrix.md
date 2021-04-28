---
description: 'Funzione D3DXQuaternionRotationMatrix (D3DX10Math.h): compila un quaternione da una matrice di rotazione.'
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Funzione D3DXQuaternionRotationMatrix (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103149"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="0b3c4-103">Funzione D3DXQuaternionRotationMatrix (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="0b3c4-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="0b3c4-104">Compila un quaternione da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b3c4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0b3c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b3c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b3c4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0b3c4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3c4-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b3c4-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0b3c4-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0b3c4-110">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b3c4-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3c4-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b3c4-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b3c4-112">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b3c4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b3c4-113">Return value</span></span>

<span data-ttu-id="0b3c4-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b3c4-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0b3c4-115">Puntatore alla struttura D3DXQUATERNION compilata da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b3c4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b3c4-116">Remarks</span></span>

<span data-ttu-id="0b3c4-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0b3c4-118">In questo modo, la funzione D3DXQuaternionRotationMatrix può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0b3c4-119">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="0b3c4-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b3c4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b3c4-120">Requirements</span></span>



| <span data-ttu-id="0b3c4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b3c4-121">Requirement</span></span> | <span data-ttu-id="0b3c4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0b3c4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3c4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b3c4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0b3c4-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0b3c4-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0b3c4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b3c4-125">Library</span></span><br/> | <dl> <span data-ttu-id="0b3c4-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b3c4-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b3c4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b3c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3c4-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0b3c4-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
