---
description: Compila un quaternione con l'imbardata, il pitch e il rullo specificati.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)
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
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322607"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="5781f-103">Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5781f-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="5781f-104">Compila un quaternione con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="5781f-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="5781f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5781f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="5781f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5781f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5781f-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5781f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5781f-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5781f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5781f-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5781f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5781f-110">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5781f-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5781f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5781f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5781f-112">Imbardata intorno all'asse y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5781f-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5781f-113">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5781f-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5781f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5781f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5781f-115">Pitch intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5781f-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5781f-116">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5781f-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5781f-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5781f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5781f-118">Ruotare intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5781f-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5781f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5781f-119">Return value</span></span>

<span data-ttu-id="5781f-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5781f-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5781f-121">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) con l'imbardata, il pitch e il rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="5781f-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="5781f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5781f-122">Remarks</span></span>

<span data-ttu-id="5781f-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="5781f-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5781f-124">In questo modo, la funzione **D3DXQuaternionRotationYawPitchRoll** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5781f-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5781f-125">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="5781f-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="5781f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5781f-126">Requirements</span></span>



| <span data-ttu-id="5781f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5781f-127">Requirement</span></span> | <span data-ttu-id="5781f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5781f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5781f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5781f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5781f-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5781f-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5781f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="5781f-131">Library</span></span><br/> | <dl> <span data-ttu-id="5781f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5781f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5781f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5781f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5781f-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5781f-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5781f-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5781f-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5781f-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="5781f-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
