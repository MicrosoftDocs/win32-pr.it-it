---
description: Restituisce il quadrato della lunghezza di un quaternione.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Funzione D3DXQuaternionLengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323307"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="311c4-103">D3DXQuaternionLengthSq (funzione)</span><span class="sxs-lookup"><span data-stu-id="311c4-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="311c4-104">Restituisce il quadrato della lunghezza di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="311c4-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="311c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="311c4-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="311c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="311c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311c4-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="311c4-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311c4-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="311c4-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="311c4-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="311c4-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311c4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="311c4-110">Return value</span></span>

<span data-ttu-id="311c4-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="311c4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="311c4-112">Lunghezza quadrata del quaternione.</span><span class="sxs-lookup"><span data-stu-id="311c4-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="311c4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="311c4-113">Remarks</span></span>

<span data-ttu-id="311c4-114">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="311c4-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="311c4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="311c4-115">Requirements</span></span>



| <span data-ttu-id="311c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="311c4-116">Requirement</span></span> | <span data-ttu-id="311c4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="311c4-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="311c4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="311c4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="311c4-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="311c4-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="311c4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="311c4-120">Library</span></span><br/> | <dl> <span data-ttu-id="311c4-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="311c4-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="311c4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="311c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311c4-123">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="311c4-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="311c4-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="311c4-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
