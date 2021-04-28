---
description: "Funzione D3DXQuaternionToAxisAngle (D3dx9math.h): calcola l'asse e l'angolo di rotazione di un quaternione."
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Funzione D3DXQuaternionToAxisAngle (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117979"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="37a2f-103">Funzione D3DXQuaternionToAxisAngle (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="37a2f-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="37a2f-104">Calcola l'asse e l'angolo di rotazione di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="37a2f-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37a2f-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="37a2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a2f-107">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="37a2f-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2f-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="37a2f-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="37a2f-109">Puntatore alla struttura [**D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="37a2f-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37a2f-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37a2f-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2f-111">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37a2f-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="37a2f-112">Questa funzione restituisce un puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che identifica l'asse di rotazione del quaternione.</span><span class="sxs-lookup"><span data-stu-id="37a2f-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="37a2f-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37a2f-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="37a2f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="37a2f-115">Questa funzione restituisce un puntatore a un valore FLOAT che identifica l'angolo di rotazione del quaternione in radianti.</span><span class="sxs-lookup"><span data-stu-id="37a2f-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a2f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37a2f-116">Return value</span></span>

<span data-ttu-id="37a2f-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="37a2f-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a2f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="37a2f-118">Remarks</span></span>

<span data-ttu-id="37a2f-119">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="37a2f-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a2f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37a2f-120">Requirements</span></span>



| <span data-ttu-id="37a2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a2f-121">Requirement</span></span> | <span data-ttu-id="37a2f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="37a2f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37a2f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37a2f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="37a2f-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37a2f-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="37a2f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="37a2f-125">Library</span></span><br/> | <dl> <span data-ttu-id="37a2f-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="37a2f-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37a2f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37a2f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a2f-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="37a2f-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
