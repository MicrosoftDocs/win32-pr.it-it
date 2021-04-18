---
description: Compila un quaternione con l'imbardata, il pitch e il rullo specificati.
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Funzione D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d894be61f5f22322f83c4e4a6c6a724de4b9da4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323201"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="80fd5-103">Funzione D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="80fd5-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="80fd5-104">Compila un quaternione con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="80fd5-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80fd5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="80fd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80fd5-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="80fd5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="80fd5-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="80fd5-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="80fd5-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="80fd5-110">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80fd5-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80fd5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80fd5-112">Imbardata intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="80fd5-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="80fd5-113">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80fd5-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80fd5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80fd5-115">Pitch intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="80fd5-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="80fd5-116">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80fd5-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80fd5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80fd5-118">Ruotare intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="80fd5-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80fd5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80fd5-119">Return value</span></span>

<span data-ttu-id="80fd5-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="80fd5-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="80fd5-121">Puntatore a una struttura D3DXQUATERNION con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="80fd5-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="80fd5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="80fd5-122">Remarks</span></span>

<span data-ttu-id="80fd5-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="80fd5-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="80fd5-124">In questo modo, la funzione D3DXQuaternionRotationYawPitchRoll può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="80fd5-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="80fd5-125">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="80fd5-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="80fd5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80fd5-126">Requirements</span></span>



| <span data-ttu-id="80fd5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80fd5-127">Requirement</span></span> | <span data-ttu-id="80fd5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="80fd5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80fd5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80fd5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="80fd5-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="80fd5-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="80fd5-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="80fd5-131">Library</span></span><br/> | <dl> <span data-ttu-id="80fd5-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80fd5-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80fd5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80fd5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fd5-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="80fd5-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
