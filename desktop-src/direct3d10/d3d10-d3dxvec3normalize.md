---
description: 'Funzione D3DXVec3Normalize (D3DX10Math.h): restituisce la versione normalizzata di un vettore 3D.'
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Funzione D3DXVec3Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108179"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="8f80f-103">Funzione D3DXVec3Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8f80f-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="8f80f-104">Restituisce la versione normalizzata di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="8f80f-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f80f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f80f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="8f80f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f80f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f80f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8f80f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f80f-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f80f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8f80f-109">Puntatore [**all'oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8f80f-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f80f-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8f80f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f80f-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f80f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8f80f-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="8f80f-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f80f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f80f-113">Return value</span></span>

<span data-ttu-id="8f80f-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f80f-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8f80f-115">Puntatore a una struttura D3DXVECTOR3 che rappresenta la versione normalizzata del vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="8f80f-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f80f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f80f-116">Remarks</span></span>

<span data-ttu-id="8f80f-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="8f80f-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8f80f-118">In questo modo, la funzione D3DXVec3Normalize può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8f80f-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f80f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f80f-119">Requirements</span></span>



| <span data-ttu-id="8f80f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f80f-120">Requirement</span></span> | <span data-ttu-id="8f80f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8f80f-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f80f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f80f-122">Header</span></span><br/> | <dl> <span data-ttu-id="8f80f-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8f80f-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f80f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f80f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f80f-125">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8f80f-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
