---
description: Compila un quaternione da una matrice di rotazione.
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Funzione D3DXQuaternionRotationMatrix (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a9513c9aededdd06080db97aac78278986244b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354639"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="7a5f4-103">Funzione D3DXQuaternionRotationMatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7a5f4-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="7a5f4-104">Compila un quaternione da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5f4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a5f4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7a5f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a5f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5f4-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7a5f4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5f4-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a5f4-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7a5f4-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7a5f4-110">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a5f4-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5f4-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a5f4-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a5f4-112">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5f4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a5f4-113">Return value</span></span>

<span data-ttu-id="7a5f4-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a5f4-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7a5f4-115">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) compilata da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5f4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a5f4-116">Remarks</span></span>

<span data-ttu-id="7a5f4-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="7a5f4-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7a5f4-118">In questo modo, la funzione **D3DXQuaternionRotationMatrix** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7a5f4-119">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="7a5f4-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5f4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a5f4-120">Requirements</span></span>



| <span data-ttu-id="7a5f4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5f4-121">Requirement</span></span> | <span data-ttu-id="7a5f4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7a5f4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5f4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a5f4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7a5f4-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f4-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7a5f4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a5f4-125">Library</span></span><br/> | <dl> <span data-ttu-id="7a5f4-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f4-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a5f4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a5f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5f4-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7a5f4-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7a5f4-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7a5f4-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="7a5f4-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7a5f4-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




