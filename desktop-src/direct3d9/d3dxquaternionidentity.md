---
description: Restituisce il quaternione di identità.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: Funzione D3DXQuaternionIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354644"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="ea245-103">D3DXQuaternionIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="ea245-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="ea245-104">Restituisce il quaternione di identità.</span><span class="sxs-lookup"><span data-stu-id="ea245-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea245-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea245-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="ea245-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea245-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ea245-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea245-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea245-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ea245-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea245-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea245-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea245-110">Return value</span></span>

<span data-ttu-id="ea245-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea245-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ea245-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il quaternione di identità.</span><span class="sxs-lookup"><span data-stu-id="ea245-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea245-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea245-113">Remarks</span></span>

<span data-ttu-id="ea245-114">Dato un quaternione (x, y, z, w), la funzione **D3DXQuaternionIdentity** restituirà il quaternione (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="ea245-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="ea245-115">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="ea245-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ea245-116">In questo modo, la funzione **D3DXQuaternionIdentity** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ea245-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ea245-117">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ea245-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea245-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea245-118">Requirements</span></span>



| <span data-ttu-id="ea245-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea245-119">Requirement</span></span> | <span data-ttu-id="ea245-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ea245-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea245-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea245-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ea245-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea245-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ea245-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea245-123">Library</span></span><br/> | <dl> <span data-ttu-id="ea245-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea245-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea245-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea245-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea245-126">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ea245-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ea245-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="ea245-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




