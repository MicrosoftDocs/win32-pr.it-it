---
description: Determina il prodotto scalare di due vettori 3D.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: Funzione D3DXVec3Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322624"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="4a163-103">D3DXVec3Dot (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a163-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="4a163-104">Determina il prodotto scalare di due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="4a163-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a163-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a163-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="4a163-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a163-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a163-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a163-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a163-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4a163-109">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4a163-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a163-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a163-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a163-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a163-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4a163-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4a163-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a163-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a163-113">Return value</span></span>

<span data-ttu-id="4a163-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a163-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a163-115">Prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="4a163-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a163-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a163-116">Requirements</span></span>



| <span data-ttu-id="4a163-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a163-117">Requirement</span></span> | <span data-ttu-id="4a163-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4a163-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a163-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a163-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4a163-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a163-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4a163-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a163-121">Library</span></span><br/> | <dl> <span data-ttu-id="4a163-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a163-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a163-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a163-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a163-124">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4a163-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4a163-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="4a163-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
