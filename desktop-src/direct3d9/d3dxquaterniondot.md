---
description: Restituisce il prodotto scalare di due quaternioni.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Funzione D3DXQuaternionDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355519"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="8a8ae-103">D3DXQuaternionDot (funzione)</span><span class="sxs-lookup"><span data-stu-id="8a8ae-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="8a8ae-104">Restituisce il prodotto scalare di due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="8a8ae-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a8ae-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="8a8ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8ae-107">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a8ae-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8ae-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a8ae-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8a8ae-109">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="8a8ae-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a8ae-110">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a8ae-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8ae-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a8ae-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8a8ae-112">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="8a8ae-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8ae-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a8ae-113">Return value</span></span>

<span data-ttu-id="8a8ae-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a8ae-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a8ae-115">Prodotto scalare di due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="8a8ae-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8ae-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a8ae-116">Remarks</span></span>

<span data-ttu-id="8a8ae-117">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="8a8ae-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8ae-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a8ae-118">Requirements</span></span>



| <span data-ttu-id="8a8ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8ae-119">Requirement</span></span> | <span data-ttu-id="8a8ae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8a8ae-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8ae-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a8ae-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a8ae-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a8ae-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8a8ae-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a8ae-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a8ae-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a8ae-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a8ae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a8ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8ae-126">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8a8ae-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
