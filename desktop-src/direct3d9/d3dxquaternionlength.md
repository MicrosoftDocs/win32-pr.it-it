---
description: Restituisce la lunghezza di un quaternione.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: Funzione D3DXQuaternionLength (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402005"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="66d09-103">D3DXQuaternionLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="66d09-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="66d09-104">Restituisce la lunghezza di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="66d09-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66d09-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="66d09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66d09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d09-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66d09-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d09-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66d09-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66d09-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="66d09-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d09-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66d09-110">Return value</span></span>

<span data-ttu-id="66d09-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66d09-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66d09-112">Lunghezza del quaternione.</span><span class="sxs-lookup"><span data-stu-id="66d09-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d09-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="66d09-113">Remarks</span></span>

<span data-ttu-id="66d09-114">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="66d09-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d09-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66d09-115">Requirements</span></span>



| <span data-ttu-id="66d09-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d09-116">Requirement</span></span> | <span data-ttu-id="66d09-117">Valore</span><span class="sxs-lookup"><span data-stu-id="66d09-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d09-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66d09-118">Header</span></span><br/>  | <dl> <span data-ttu-id="66d09-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d09-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="66d09-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="66d09-120">Library</span></span><br/> | <dl> <span data-ttu-id="66d09-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66d09-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66d09-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66d09-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d09-123">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="66d09-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="66d09-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="66d09-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
