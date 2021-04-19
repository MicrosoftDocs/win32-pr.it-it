---
description: Restituisce la matrice di trasponente di una matrice.
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: Funzione D3DXMatrixTranspose (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322121"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="9f53f-103">Funzione D3DXMatrixTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9f53f-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="9f53f-104">Restituisce la matrice di trasponente di una matrice.</span><span class="sxs-lookup"><span data-stu-id="9f53f-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f53f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f53f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="9f53f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f53f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f53f-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9f53f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f53f-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f53f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9f53f-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9f53f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9f53f-110">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f53f-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f53f-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f53f-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9f53f-112">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="9f53f-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f53f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f53f-113">Return value</span></span>

<span data-ttu-id="9f53f-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f53f-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9f53f-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di trasporre la matrice.</span><span class="sxs-lookup"><span data-stu-id="9f53f-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f53f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f53f-116">Remarks</span></span>

<span data-ttu-id="9f53f-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="9f53f-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9f53f-118">In questo modo, la funzione **D3DXMatrixTranspose** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="9f53f-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f53f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f53f-119">Requirements</span></span>



| <span data-ttu-id="9f53f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f53f-120">Requirement</span></span> | <span data-ttu-id="9f53f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9f53f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f53f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f53f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9f53f-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f53f-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9f53f-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f53f-124">Library</span></span><br/> | <dl> <span data-ttu-id="9f53f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f53f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f53f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f53f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f53f-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9f53f-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




