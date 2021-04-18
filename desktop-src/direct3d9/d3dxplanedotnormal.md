---
description: Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Funzione D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322101"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="26b56-104">D3DXPlaneDotNormal (funzione)</span><span class="sxs-lookup"><span data-stu-id="26b56-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="26b56-105">Calcola il prodotto a punti di un piano e di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="26b56-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="26b56-106">Si presuppone che il parametro w del vettore sia 0.</span><span class="sxs-lookup"><span data-stu-id="26b56-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b56-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26b56-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="26b56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="26b56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b56-109">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b56-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="26b56-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="26b56-111">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="26b56-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26b56-112">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b56-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="26b56-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="26b56-114">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="26b56-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b56-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26b56-115">Return value</span></span>

<span data-ttu-id="26b56-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b56-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b56-117">Prodotto a virgola del piano e del vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="26b56-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b56-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="26b56-118">Remarks</span></span>

<span data-ttu-id="26b56-119">Dato un piano (a, b, c, d) e un vettore 3D (x, y, z), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="26b56-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="26b56-120">La funzione **D3DXPlaneDotNormal** è utile per calcolare l'angolo tra la normale del piano e un altro normale.</span><span class="sxs-lookup"><span data-stu-id="26b56-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b56-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26b56-121">Requirements</span></span>



| <span data-ttu-id="26b56-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b56-122">Requirement</span></span> | <span data-ttu-id="26b56-123">Valore</span><span class="sxs-lookup"><span data-stu-id="26b56-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b56-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26b56-124">Header</span></span><br/>  | <dl> <span data-ttu-id="26b56-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b56-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="26b56-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="26b56-126">Library</span></span><br/> | <dl> <span data-ttu-id="26b56-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26b56-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26b56-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26b56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b56-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="26b56-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="26b56-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="26b56-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="26b56-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="26b56-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
