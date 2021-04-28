---
description: "Funzione D3DXQuaternionExp (D3DX10Math.h): calcola l'esponenziale."
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Funzione D3DXQuaternionExp (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7c022b9df4302683a184b4fc8329561b22d341d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103219"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="d3dde-103">Funzione D3DXQuaternionExp (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d3dde-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="d3dde-104">Calcola l'esponenziale.</span><span class="sxs-lookup"><span data-stu-id="d3dde-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3dde-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3dde-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="d3dde-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3dde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3dde-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d3dde-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3dde-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3dde-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d3dde-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d3dde-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3dde-110">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d3dde-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3dde-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3dde-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d3dde-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="d3dde-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3dde-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3dde-113">Return value</span></span>

<span data-ttu-id="d3dde-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3dde-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d3dde-115">Puntatore a una struttura D3DXQUATERNION che rappresenta l'esponenziale.</span><span class="sxs-lookup"><span data-stu-id="d3dde-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3dde-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3dde-116">Remarks</span></span>

<span data-ttu-id="d3dde-117">Questo metodo converte un quaternione puro in un quaternione di unità.</span><span class="sxs-lookup"><span data-stu-id="d3dde-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="d3dde-118">D3DXQuaternionExp prevede un quaternione puro, dove w viene ignorato nel calcolo (w == 0).</span><span class="sxs-lookup"><span data-stu-id="d3dde-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="d3dde-119">dove v è la parte vettoriale di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="d3dde-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="d3dde-120">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="d3dde-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d3dde-121">In questo modo, la funzione D3DXQuaternionExp può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d3dde-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d3dde-122">Il [**metodo D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) può essere usato anche per impostare i punti di controllo di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="d3dde-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="d3dde-123">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="d3dde-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3dde-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3dde-124">Requirements</span></span>



| <span data-ttu-id="d3dde-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3dde-125">Requirement</span></span> | <span data-ttu-id="d3dde-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d3dde-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3dde-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3dde-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d3dde-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d3dde-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d3dde-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3dde-129">Library</span></span><br/> | <dl> <span data-ttu-id="d3dde-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3dde-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3dde-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3dde-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3dde-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d3dde-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
