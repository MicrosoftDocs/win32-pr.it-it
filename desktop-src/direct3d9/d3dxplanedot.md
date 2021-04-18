---
description: Calcola il prodotto a punti di un piano e di un vettore 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Funzione D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322110"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="9776b-103">D3DXPlaneDot (funzione)</span><span class="sxs-lookup"><span data-stu-id="9776b-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="9776b-104">Calcola il prodotto a punti di un piano e di un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="9776b-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9776b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9776b-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="9776b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9776b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9776b-107">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9776b-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9776b-108">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="9776b-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="9776b-109">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="9776b-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9776b-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9776b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9776b-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="9776b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="9776b-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="9776b-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9776b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9776b-113">Return value</span></span>

<span data-ttu-id="9776b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9776b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9776b-115">Prodotto a virgola del piano e del vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="9776b-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9776b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9776b-116">Remarks</span></span>

<span data-ttu-id="9776b-117">Dato un piano (a, b, c, d) e un vettore 4D (x, y, z, w), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* .</span><span class="sxs-lookup"><span data-stu-id="9776b-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="9776b-118">La funzione **D3DXPlaneDot** è utile per determinare la relazione del piano con una coordinata omogenea.</span><span class="sxs-lookup"><span data-stu-id="9776b-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="9776b-119">Questa funzione, ad esempio, può essere utilizzata per determinare se una coordinata specifica si trova su un particolare piano o su quale lato di un particolare piano si trova una coordinata particolare.</span><span class="sxs-lookup"><span data-stu-id="9776b-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="9776b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9776b-120">Requirements</span></span>



| <span data-ttu-id="9776b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9776b-121">Requirement</span></span> | <span data-ttu-id="9776b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9776b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9776b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9776b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9776b-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9776b-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9776b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9776b-125">Library</span></span><br/> | <dl> <span data-ttu-id="9776b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9776b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9776b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9776b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9776b-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9776b-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9776b-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="9776b-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="9776b-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="9776b-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
