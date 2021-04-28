---
description: 'Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h): compila una matrice con uno yaw, un passo e un lancio specificati.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118149"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="59a22-103">Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="59a22-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="59a22-104">Compila una matrice con uno yaw, un passo e un lancio specificati.</span><span class="sxs-lookup"><span data-stu-id="59a22-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a22-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59a22-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="59a22-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59a22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a22-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59a22-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59a22-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="59a22-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="59a22-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="59a22-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="59a22-110">*Yaw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="59a22-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a22-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59a22-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59a22-112">Yaw intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="59a22-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="59a22-113">*Tono* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="59a22-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a22-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59a22-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59a22-115">Passo intorno all'asse x, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="59a22-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="59a22-116">*Roll* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="59a22-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a22-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59a22-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59a22-118">Rullo intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="59a22-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a22-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59a22-119">Return value</span></span>

<span data-ttu-id="59a22-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="59a22-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="59a22-121">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) con yaw, pitch e roll specificati.</span><span class="sxs-lookup"><span data-stu-id="59a22-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a22-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="59a22-122">Remarks</span></span>

<span data-ttu-id="59a22-123">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="59a22-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="59a22-124">In questo modo, la **funzione D3DXMatrixRotationYawPitchRoll** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="59a22-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="59a22-125">L'ordine delle trasformazioni è roll first, quindi pitch, quindi yaw.</span><span class="sxs-lookup"><span data-stu-id="59a22-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="59a22-126">Rispetto all'asse delle coordinate locale dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="59a22-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Illustrazione di rollio, passo e yaw come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="59a22-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59a22-128">Requirements</span></span>



| <span data-ttu-id="59a22-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a22-129">Requirement</span></span> | <span data-ttu-id="59a22-130">Valore</span><span class="sxs-lookup"><span data-stu-id="59a22-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59a22-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59a22-131">Header</span></span><br/>  | <dl> <span data-ttu-id="59a22-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="59a22-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="59a22-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="59a22-133">Library</span></span><br/> | <dl> <span data-ttu-id="59a22-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="59a22-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59a22-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59a22-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a22-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="59a22-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="59a22-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="59a22-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="59a22-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="59a22-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="59a22-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="59a22-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="59a22-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="59a22-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="59a22-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="59a22-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
