---
description: 'Funzione D3DXVec4Transform (D3dx9math.h): trasforma un vettore 4D in base a una determinata matrice.'
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Funzione D3DXVec4Transform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115509"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="3e3b9-103">Funzione D3DXVec4Transform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3e3b9-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="3e3b9-104">Trasforma un vettore 4D in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e3b9-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="3e3b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e3b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e3b9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e3b9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3b9-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e3b9-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3e3b9-109">Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3e3b9-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3b9-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3b9-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e3b9-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3e3b9-112">Puntatore alla struttura [**D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e3b9-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3b9-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3b9-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e3b9-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3e3b9-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e3b9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e3b9-116">Return value</span></span>

<span data-ttu-id="3e3b9-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e3b9-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3e3b9-118">Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore 4D trasformato.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e3b9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e3b9-119">Remarks</span></span>

<span data-ttu-id="3e3b9-120">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="3e3b9-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3e3b9-121">In questo modo, la **funzione D3DXVec4Transform** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3b9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e3b9-122">Requirements</span></span>



| <span data-ttu-id="3e3b9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e3b9-123">Requirement</span></span> | <span data-ttu-id="3e3b9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3e3b9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3b9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e3b9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3e3b9-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e3b9-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3e3b9-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e3b9-127">Library</span></span><br/> | <dl> <span data-ttu-id="3e3b9-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e3b9-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3e3b9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e3b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3b9-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3e3b9-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




