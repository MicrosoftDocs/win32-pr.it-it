---
description: Proietta una matrice (x, y, z,0) dallo spazio dello schermo nello spazio degli oggetti.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Funzione D3DXVec3UnprojectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3af4cc05b5f8ee30c624f904df7e2ae5cd4b844a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969474"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="b5ec4-103">Funzione D3DXVec3UnprojectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b5ec4-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="b5ec4-104">Proietta una matrice (x, y, z,0) dallo spazio dello schermo nello spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ec4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5ec4-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="b5ec4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5ec4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ec4-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5ec4-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5ec4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5ec4-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5ec4-115">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5ec4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5ec4-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-119">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="b5ec4-121">Puntatore a una struttura [**D3DVIEWPORT9**](d3dviewport9.md) che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-122">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5ec4-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-125">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5ec4-127">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-128">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5ec4-130">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec4-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ec4-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec4-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5ec4-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5ec4-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ec4-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5ec4-134">Return value</span></span>

<span data-ttu-id="b5ec4-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5ec4-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5ec4-136">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice proiettata dallo spazio dello schermo allo spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ec4-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5ec4-137">Remarks</span></span>

<span data-ttu-id="b5ec4-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="b5ec4-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b5ec4-139">In questo modo, la funzione [**D3DXVec3Unproject**](d3dxvec3unproject.md) può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ec4-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5ec4-140">Requirements</span></span>



| <span data-ttu-id="b5ec4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ec4-141">Requirement</span></span> | <span data-ttu-id="b5ec4-142">Valore</span><span class="sxs-lookup"><span data-stu-id="b5ec4-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ec4-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5ec4-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b5ec4-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ec4-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5ec4-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5ec4-145">Library</span></span><br/> | <dl> <span data-ttu-id="b5ec4-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5ec4-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5ec4-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5ec4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ec4-148">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b5ec4-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b5ec4-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="b5ec4-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
