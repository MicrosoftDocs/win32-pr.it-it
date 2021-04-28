---
description: 'Funzione D3DXMatrixTranspose (D3dx9math.h): restituisce la trasposizione di matrice di una matrice.'
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: Funzione D3DXMatrixTranspose (D3dx9math.h)
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
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098109"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="026e5-103">Funzione D3DXMatrixTranspose (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="026e5-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="026e5-104">Restituisce la trasposizione della matrice di una matrice.</span><span class="sxs-lookup"><span data-stu-id="026e5-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="026e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="026e5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="026e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="026e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="026e5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="026e5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="026e5-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="026e5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="026e5-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="026e5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="026e5-110">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="026e5-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026e5-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="026e5-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="026e5-112">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="026e5-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="026e5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="026e5-113">Return value</span></span>

<span data-ttu-id="026e5-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="026e5-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="026e5-115">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la trasposizione della matrice.</span><span class="sxs-lookup"><span data-stu-id="026e5-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="026e5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="026e5-116">Remarks</span></span>

<span data-ttu-id="026e5-117">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="026e5-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="026e5-118">In questo modo, la **funzione D3DXMatrixTranspose** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="026e5-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="026e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="026e5-119">Requirements</span></span>



| <span data-ttu-id="026e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="026e5-120">Requirement</span></span> | <span data-ttu-id="026e5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="026e5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="026e5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="026e5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="026e5-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="026e5-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="026e5-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="026e5-124">Library</span></span><br/> | <dl> <span data-ttu-id="026e5-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="026e5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="026e5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="026e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026e5-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="026e5-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




