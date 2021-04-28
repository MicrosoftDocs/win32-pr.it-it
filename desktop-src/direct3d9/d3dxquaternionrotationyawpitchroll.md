---
description: "Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h): compila un quaternione con l'yaw, il passo e il lancio dati."
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117999"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="8268e-103">Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8268e-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="8268e-104">Compila un quaternione con l'yaw, il passo e il lancio dati.</span><span class="sxs-lookup"><span data-stu-id="8268e-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="8268e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8268e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="8268e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8268e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8268e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8268e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8268e-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8268e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8268e-109">Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8268e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8268e-110">*Yaw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8268e-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8268e-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8268e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8268e-112">Yaw intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="8268e-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8268e-113">*Tono* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8268e-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8268e-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8268e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8268e-115">Passo intorno all'asse x, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="8268e-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8268e-116">*Roll* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8268e-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8268e-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8268e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8268e-118">Rullo intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="8268e-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8268e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8268e-119">Return value</span></span>

<span data-ttu-id="8268e-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8268e-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8268e-121">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) con yaw, pitch e roll specificati.</span><span class="sxs-lookup"><span data-stu-id="8268e-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="8268e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8268e-122">Remarks</span></span>

<span data-ttu-id="8268e-123">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="8268e-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8268e-124">In questo modo, la **funzione D3DXQuaternionRotationYawPitchRoll** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8268e-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8268e-125">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="8268e-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8268e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8268e-126">Requirements</span></span>



| <span data-ttu-id="8268e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8268e-127">Requirement</span></span> | <span data-ttu-id="8268e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8268e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8268e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8268e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8268e-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8268e-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8268e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8268e-131">Library</span></span><br/> | <dl> <span data-ttu-id="8268e-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8268e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8268e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8268e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8268e-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8268e-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8268e-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="8268e-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="8268e-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="8268e-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
