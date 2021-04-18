---
description: Restituisce la lunghezza di un vettore 3D.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: Funzione D3DXVec3Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322446"
---
# <a name="d3dxvec3length-function"></a><span data-ttu-id="28583-103">D3DXVec3Length (funzione)</span><span class="sxs-lookup"><span data-stu-id="28583-103">D3DXVec3Length function</span></span>

<span data-ttu-id="28583-104">Restituisce la lunghezza di un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="28583-104">Returns the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="28583-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28583-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="28583-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28583-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28583-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28583-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="28583-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="28583-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="28583-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28583-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28583-110">Return value</span></span>

<span data-ttu-id="28583-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28583-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28583-112">Lunghezza del vettore.</span><span class="sxs-lookup"><span data-stu-id="28583-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="28583-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28583-113">Requirements</span></span>



| <span data-ttu-id="28583-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28583-114">Requirement</span></span> | <span data-ttu-id="28583-115">Valore</span><span class="sxs-lookup"><span data-stu-id="28583-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28583-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28583-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28583-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28583-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28583-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="28583-118">Library</span></span><br/> | <dl> <span data-ttu-id="28583-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28583-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28583-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28583-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28583-121">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="28583-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="28583-122">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="28583-122">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
