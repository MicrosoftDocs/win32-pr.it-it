---
description: 'Funzione D3DXMatrixTranspose (D3DX10Math.h): restituisce il trasposto di matrice di una matrice.'
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: Funzione D3DXMatrixTranspose (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108859"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="dab1e-103">Funzione D3DXMatrixTranspose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="dab1e-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="dab1e-104">Restituisce la trasposizione della matrice di una matrice.</span><span class="sxs-lookup"><span data-stu-id="dab1e-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dab1e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="dab1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dab1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab1e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dab1e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dab1e-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dab1e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dab1e-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dab1e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dab1e-110">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dab1e-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab1e-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="dab1e-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dab1e-112">Puntatore alla struttura D3DXMATRIX di origine.</span><span class="sxs-lookup"><span data-stu-id="dab1e-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab1e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dab1e-113">Return value</span></span>

<span data-ttu-id="dab1e-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dab1e-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dab1e-115">Puntatore alla struttura D3DXMATRIX che rappresenta la trasposizione della matrice.</span><span class="sxs-lookup"><span data-stu-id="dab1e-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab1e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dab1e-116">Remarks</span></span>

<span data-ttu-id="dab1e-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="dab1e-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="dab1e-118">In questo modo, la funzione D3DXMatrixTranspose può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="dab1e-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab1e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dab1e-119">Requirements</span></span>



| <span data-ttu-id="dab1e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dab1e-120">Requirement</span></span> | <span data-ttu-id="dab1e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dab1e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dab1e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dab1e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dab1e-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="dab1e-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="dab1e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="dab1e-124">Library</span></span><br/> | <dl> <span data-ttu-id="dab1e-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dab1e-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dab1e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dab1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab1e-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="dab1e-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
