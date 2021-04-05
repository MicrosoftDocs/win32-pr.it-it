---
description: Compila una matrice con l'imbardata, il pitch e il rullo specificati.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969482"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="f4ff1-103">Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f4ff1-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="f4ff1-104">Compila una matrice con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ff1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4ff1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="f4ff1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4ff1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ff1-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f4ff1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff1-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4ff1-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f4ff1-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f4ff1-110">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4ff1-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4ff1-112">Imbardata intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f4ff1-113">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4ff1-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff1-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4ff1-115">Pitch intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f4ff1-116">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4ff1-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff1-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4ff1-118">Ruotare intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ff1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4ff1-119">Return value</span></span>

<span data-ttu-id="f4ff1-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4ff1-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f4ff1-121">Puntatore a una struttura D3DXMATRIX con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ff1-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4ff1-122">Remarks</span></span>

<span data-ttu-id="f4ff1-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f4ff1-124">In questo modo, la funzione D3DXMatrixRotationYawPitchRoll può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f4ff1-125">L'ordine delle trasformazioni è prima di tutto roll, quindi pitch, then imbardata.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="f4ff1-126">Rispetto all'asse delle coordinate locali dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="f4ff1-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustrazione di roll, pitch e imbardata come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="f4ff1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4ff1-128">Requirements</span></span>



| <span data-ttu-id="f4ff1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ff1-129">Requirement</span></span> | <span data-ttu-id="f4ff1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f4ff1-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ff1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4ff1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f4ff1-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff1-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f4ff1-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4ff1-133">Library</span></span><br/> | <dl> <span data-ttu-id="f4ff1-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff1-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4ff1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4ff1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ff1-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f4ff1-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
