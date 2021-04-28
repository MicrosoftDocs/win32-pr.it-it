---
description: 'Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h): compila una matrice con un yaw, un passo e un rollio specificati.'
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)
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
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108949"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="2db6d-103">Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2db6d-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="2db6d-104">Compila una matrice con uno yaw, un passo e un rollio specificati.</span><span class="sxs-lookup"><span data-stu-id="2db6d-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db6d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2db6d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="2db6d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2db6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db6d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2db6d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2db6d-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2db6d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2db6d-110">*Yaw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2db6d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2db6d-112">Yaw intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="2db6d-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2db6d-113">*Pitch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2db6d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2db6d-115">Passo intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="2db6d-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2db6d-116">*Roll* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2db6d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2db6d-118">Eseguire il roll-around dell'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="2db6d-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db6d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2db6d-119">Return value</span></span>

<span data-ttu-id="2db6d-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2db6d-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2db6d-121">Puntatore a una struttura D3DXMATRIX con lo yaw, il passo e il rollio specificati.</span><span class="sxs-lookup"><span data-stu-id="2db6d-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db6d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2db6d-122">Remarks</span></span>

<span data-ttu-id="2db6d-123">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="2db6d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2db6d-124">In questo modo, la funzione D3DXMatrixRotationYawPitchRoll può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2db6d-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2db6d-125">L'ordine delle trasformazioni è roll first, quindi pitch e yaw.</span><span class="sxs-lookup"><span data-stu-id="2db6d-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="2db6d-126">Rispetto all'asse delle coordinate locale dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2db6d-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustrazione di lancio, passo e yaw come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="2db6d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2db6d-128">Requirements</span></span>



| <span data-ttu-id="2db6d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db6d-129">Requirement</span></span> | <span data-ttu-id="2db6d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2db6d-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db6d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2db6d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2db6d-132"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2db6d-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2db6d-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2db6d-133">Library</span></span><br/> | <dl> <span data-ttu-id="2db6d-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db6d-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2db6d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2db6d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db6d-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2db6d-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
