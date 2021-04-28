---
description: 'Funzione D3DXVec3Normalize (D3dx9math.h): restituisce la versione normalizzata di un vettore 3D.'
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: Funzione D3DXVec3Normalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f39890a92bbff9d27a1150e76092d865dc36c089
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097829"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="be54a-103">Funzione D3DXVec3Normalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="be54a-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="be54a-104">Restituisce la versione normalizzata di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="be54a-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="be54a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be54a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="be54a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be54a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be54a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be54a-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="be54a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="be54a-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="be54a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be54a-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="be54a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be54a-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="be54a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="be54a-112">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="be54a-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be54a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be54a-113">Return value</span></span>

<span data-ttu-id="be54a-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="be54a-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="be54a-115">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la versione normalizzata del vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="be54a-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="be54a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="be54a-116">Remarks</span></span>

<span data-ttu-id="be54a-117">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="be54a-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="be54a-118">In questo modo, la **funzione D3DXVec3Normalize** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="be54a-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be54a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be54a-119">Requirements</span></span>



| <span data-ttu-id="be54a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="be54a-120">Requirement</span></span> | <span data-ttu-id="be54a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="be54a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be54a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be54a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="be54a-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="be54a-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="be54a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="be54a-124">Library</span></span><br/> | <dl> <span data-ttu-id="be54a-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="be54a-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be54a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be54a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be54a-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="be54a-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




