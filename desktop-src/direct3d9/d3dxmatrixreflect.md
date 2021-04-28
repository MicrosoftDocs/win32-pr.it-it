---
description: 'Funzione D3DXMatrixReflect (D3dx9math.h): compila una matrice che riflette il sistema di coordinate su un piano.'
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: Funzione D3DXMatrixReflect (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4118a5f0a1cd997d5fab5fecebae449d4c30b09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118219"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="4c9bd-103">Funzione D3DXMatrixReflect (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="4c9bd-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="4c9bd-104">Compila una matrice che riflette il sistema di coordinate di un piano.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c9bd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="4c9bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c9bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9bd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c9bd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c9bd-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c9bd-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c9bd-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c9bd-110">*pPlane* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4c9bd-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c9bd-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c9bd-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="4c9bd-112">Puntatore alla struttura [**D3DXPLANE di**](d3dxplane.md) origine.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c9bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c9bd-113">Return value</span></span>

<span data-ttu-id="4c9bd-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c9bd-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c9bd-115">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che riflette il sistema di coordinate sul piano di origine.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9bd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c9bd-116">Remarks</span></span>

<span data-ttu-id="4c9bd-117">Questa funzione normalizza l'equazione del piano prima di creare la matrice riflessa.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="4c9bd-118">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="4c9bd-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4c9bd-119">In questo modo, la **funzione D3DXMatrixReflect** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4c9bd-120">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="4c9bd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c9bd-121">Requirements</span></span>



| <span data-ttu-id="4c9bd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c9bd-122">Requirement</span></span> | <span data-ttu-id="4c9bd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4c9bd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9bd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c9bd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4c9bd-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9bd-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c9bd-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c9bd-126">Library</span></span><br/> | <dl> <span data-ttu-id="4c9bd-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c9bd-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c9bd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c9bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9bd-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4c9bd-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




