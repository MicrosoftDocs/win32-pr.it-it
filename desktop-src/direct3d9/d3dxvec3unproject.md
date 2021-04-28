---
description: 'Funzione D3DXVec3Unproject (D3dx9math.h): proietta un vettore dallo spazio dello schermo allo spazio oggetto.'
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: Funzione D3DXVec3Unproject (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c3ea6ec1aa60f48589b10575e279bed81b2c94f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115559"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="1a640-103">Funzione D3DXVec3Unproject (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1a640-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="1a640-104">Proietta un vettore dallo spazio dello schermo allo spazio oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a640-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a640-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a640-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="1a640-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a640-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a640-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a640-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a640-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1a640-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a640-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a640-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a640-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a640-112">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1a640-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1a640-113">*pViewport* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a640-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-114">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a640-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="1a640-115">Puntatore a [**una struttura D3DVIEWPORT9,**](d3dviewport9.md) che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="1a640-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="1a640-116">*pProjection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a640-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a640-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a640-118">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="1a640-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1a640-119">*pView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a640-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a640-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a640-121">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1a640-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1a640-122">*pWorld* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a640-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a640-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a640-124">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice globale.</span><span class="sxs-lookup"><span data-stu-id="1a640-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a640-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a640-125">Return value</span></span>

<span data-ttu-id="1a640-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a640-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a640-127">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore proiettato dallo spazio dello schermo allo spazio oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a640-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a640-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a640-128">Remarks</span></span>

<span data-ttu-id="1a640-129">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1a640-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1a640-130">In questo modo, la **funzione D3DXVec3Unproject** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1a640-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a640-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a640-131">Requirements</span></span>



| <span data-ttu-id="1a640-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a640-132">Requirement</span></span> | <span data-ttu-id="1a640-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1a640-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a640-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a640-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1a640-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a640-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a640-136">Library</span></span><br/> | <dl> <span data-ttu-id="1a640-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a640-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a640-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a640-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1a640-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1a640-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="1a640-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




