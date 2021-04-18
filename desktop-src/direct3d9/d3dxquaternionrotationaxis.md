---
description: Ruota un quaternione su un asse arbitrario.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Funzione D3DXQuaternionRotationAxis (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322492"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="51326-103">Funzione D3DXQuaternionRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="51326-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="51326-104">Ruota un quaternione su un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="51326-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="51326-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51326-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="51326-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51326-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="51326-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51326-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="51326-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="51326-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="51326-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="51326-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51326-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51326-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="51326-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="51326-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che identifica l'asse attorno al quale ruotare il quaternione.</span><span class="sxs-lookup"><span data-stu-id="51326-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="51326-113">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51326-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51326-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51326-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51326-115">Angolo di rotazione, in radianti.</span><span class="sxs-lookup"><span data-stu-id="51326-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="51326-116">Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="51326-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51326-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51326-117">Return value</span></span>

<span data-ttu-id="51326-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="51326-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="51326-119">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) ruotata intorno all'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="51326-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="51326-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="51326-120">Remarks</span></span>

<span data-ttu-id="51326-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="51326-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="51326-122">In questo modo, la funzione **D3DXQuaternionRotationAxis** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="51326-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="51326-123">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="51326-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="51326-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51326-124">Requirements</span></span>



| <span data-ttu-id="51326-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51326-125">Requirement</span></span> | <span data-ttu-id="51326-126">Valore</span><span class="sxs-lookup"><span data-stu-id="51326-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51326-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51326-127">Header</span></span><br/>  | <dl> <span data-ttu-id="51326-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="51326-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="51326-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="51326-129">Library</span></span><br/> | <dl> <span data-ttu-id="51326-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51326-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51326-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51326-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51326-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="51326-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="51326-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="51326-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="51326-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="51326-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
