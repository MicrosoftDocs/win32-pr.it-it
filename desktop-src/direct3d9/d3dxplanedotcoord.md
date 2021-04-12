---
description: Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia pari a 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Funzione D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234938"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="e57da-104">D3DXPlaneDotCoord (funzione)</span><span class="sxs-lookup"><span data-stu-id="e57da-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="e57da-105">Calcola il prodotto a punti di un piano e di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="e57da-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="e57da-106">Si presuppone che il parametro w del vettore sia pari a 1.</span><span class="sxs-lookup"><span data-stu-id="e57da-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="e57da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e57da-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e57da-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e57da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e57da-109">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e57da-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57da-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="e57da-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e57da-111">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e57da-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e57da-112">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e57da-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57da-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e57da-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e57da-114">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e57da-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e57da-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e57da-115">Return value</span></span>

<span data-ttu-id="e57da-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e57da-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e57da-117">Prodotto a virgola del piano e del vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="e57da-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e57da-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e57da-118">Remarks</span></span>

<span data-ttu-id="e57da-119">Dato un piano (a, b, c, d) e un vettore 3D (x, y, z), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="e57da-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="e57da-120">La funzione **D3DXPlaneDotCoord** è utile per determinare la relazione del piano con una coordinata nello spazio 3D.</span><span class="sxs-lookup"><span data-stu-id="e57da-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57da-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e57da-121">Requirements</span></span>



| <span data-ttu-id="e57da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e57da-122">Requirement</span></span> | <span data-ttu-id="e57da-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e57da-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e57da-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e57da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e57da-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e57da-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e57da-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e57da-126">Library</span></span><br/> | <dl> <span data-ttu-id="e57da-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e57da-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e57da-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e57da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57da-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e57da-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e57da-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="e57da-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="e57da-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="e57da-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
