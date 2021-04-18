---
description: Trasforma un vettore 4D in base a una matrice specificata.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Funzione D3DXVec4Transform (D3dx9math. h)
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
ms.openlocfilehash: 20192cf51a6096bbbce1f009d91d96551aec12d8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323191"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="f7a10-103">Funzione D3DXVec4Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f7a10-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="f7a10-104">Trasforma un vettore 4D in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="f7a10-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a10-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7a10-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f7a10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a10-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f7a10-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a10-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a10-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f7a10-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f7a10-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f7a10-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a10-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a10-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a10-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f7a10-112">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="f7a10-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f7a10-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a10-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a10-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a10-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f7a10-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="f7a10-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a10-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7a10-116">Return value</span></span>

<span data-ttu-id="f7a10-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a10-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f7a10-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore 4D trasformato.</span><span class="sxs-lookup"><span data-stu-id="f7a10-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a10-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7a10-119">Remarks</span></span>

<span data-ttu-id="f7a10-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="f7a10-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f7a10-121">In questo modo, la funzione **D3DXVec4Transform** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f7a10-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a10-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7a10-122">Requirements</span></span>



| <span data-ttu-id="f7a10-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7a10-123">Requirement</span></span> | <span data-ttu-id="f7a10-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f7a10-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a10-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7a10-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f7a10-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a10-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f7a10-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7a10-127">Library</span></span><br/> | <dl> <span data-ttu-id="f7a10-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7a10-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7a10-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7a10-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a10-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f7a10-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




