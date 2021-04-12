---
description: Proietta un vettore 3D dallo spazio oggetto nello spazio dello schermo.
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Funzione D3DXVec3Project (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c8198987b970fd6d79db3c73f715df4f0ac6981
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354699"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="5f73c-103">Funzione D3DXVec3Project (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5f73c-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="5f73c-104">Proietta un vettore 3D dallo spazio oggetto nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5f73c-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f73c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f73c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="5f73c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f73c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f73c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f73c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f73c-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5f73c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f73c-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f73c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f73c-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="5f73c-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f73c-113">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-114">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f73c-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="5f73c-115">Puntatore a una struttura [**D3DVIEWPORT9**](d3dviewport9.md) che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="5f73c-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="5f73c-116">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f73c-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5f73c-118">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="5f73c-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="5f73c-119">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f73c-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5f73c-121">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5f73c-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="5f73c-122">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f73c-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f73c-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f73c-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5f73c-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="5f73c-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f73c-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f73c-125">Return value</span></span>

<span data-ttu-id="5f73c-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f73c-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f73c-127">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore proiettato dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5f73c-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f73c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f73c-128">Remarks</span></span>

<span data-ttu-id="5f73c-129">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="5f73c-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5f73c-130">In questo modo, la funzione **D3DXVec3Project** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5f73c-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f73c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f73c-131">Requirements</span></span>



| <span data-ttu-id="5f73c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f73c-132">Requirement</span></span> | <span data-ttu-id="5f73c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5f73c-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f73c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f73c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5f73c-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f73c-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5f73c-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f73c-136">Library</span></span><br/> | <dl> <span data-ttu-id="5f73c-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f73c-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f73c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f73c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f73c-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5f73c-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5f73c-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="5f73c-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




