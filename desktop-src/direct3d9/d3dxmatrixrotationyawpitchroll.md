---
description: Compila una matrice con l'imbardata, il pitch e il rullo specificati.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math. h)
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
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234943"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="235ce-103">Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="235ce-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="235ce-104">Compila una matrice con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="235ce-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="235ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="235ce-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="235ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="235ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235ce-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="235ce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="235ce-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="235ce-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="235ce-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="235ce-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="235ce-110">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="235ce-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235ce-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235ce-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="235ce-112">Imbardata intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="235ce-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="235ce-113">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="235ce-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235ce-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235ce-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="235ce-115">Pitch intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="235ce-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="235ce-116">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="235ce-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235ce-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235ce-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="235ce-118">Ruotare intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="235ce-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235ce-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="235ce-119">Return value</span></span>

<span data-ttu-id="235ce-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="235ce-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="235ce-121">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="235ce-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="235ce-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="235ce-122">Remarks</span></span>

<span data-ttu-id="235ce-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="235ce-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="235ce-124">In questo modo, la funzione **D3DXMatrixRotationYawPitchRoll** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="235ce-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="235ce-125">L'ordine delle trasformazioni è prima di tutto roll, quindi pitch, then imbardata.</span><span class="sxs-lookup"><span data-stu-id="235ce-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="235ce-126">Rispetto all'asse delle coordinate locali dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="235ce-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustrazione di roll, pitch e imbardata come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="235ce-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="235ce-128">Requirements</span></span>



| <span data-ttu-id="235ce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="235ce-129">Requirement</span></span> | <span data-ttu-id="235ce-130">Valore</span><span class="sxs-lookup"><span data-stu-id="235ce-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="235ce-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="235ce-131">Header</span></span><br/>  | <dl> <span data-ttu-id="235ce-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="235ce-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="235ce-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="235ce-133">Library</span></span><br/> | <dl> <span data-ttu-id="235ce-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="235ce-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="235ce-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="235ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235ce-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="235ce-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="235ce-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="235ce-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="235ce-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="235ce-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="235ce-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="235ce-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="235ce-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="235ce-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="235ce-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="235ce-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
