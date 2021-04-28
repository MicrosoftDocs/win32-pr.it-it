---
description: "Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h): calcola l'asse e l'angolo di rotazione di un quaternione."
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108699"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="810d2-103">Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="810d2-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="810d2-104">Calcola l'asse e l'angolo di rotazione di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="810d2-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="810d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="810d2-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="810d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="810d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="810d2-107">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="810d2-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810d2-108">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="810d2-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="810d2-109">Puntatore all'oggetto [**D3DXQUATERNION di origine.**](d3d10-d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="810d2-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="810d2-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="810d2-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="810d2-111">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="810d2-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="810d2-112">Questa funzione restituisce un puntatore a [**un oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che identifica l'asse di rotazione del quaternione.</span><span class="sxs-lookup"><span data-stu-id="810d2-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="810d2-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="810d2-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="810d2-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="810d2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="810d2-115">Questa funzione restituisce un puntatore a un valore FLOAT che identifica l'angolo di rotazione del quaternione in radianti.</span><span class="sxs-lookup"><span data-stu-id="810d2-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="810d2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="810d2-116">Return value</span></span>

<span data-ttu-id="810d2-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="810d2-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="810d2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="810d2-118">Remarks</span></span>

<span data-ttu-id="810d2-119">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="810d2-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="810d2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="810d2-120">Requirements</span></span>



| <span data-ttu-id="810d2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="810d2-121">Requirement</span></span> | <span data-ttu-id="810d2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="810d2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="810d2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="810d2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="810d2-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="810d2-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="810d2-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="810d2-125">Library</span></span><br/> | <dl> <span data-ttu-id="810d2-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="810d2-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="810d2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="810d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810d2-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="810d2-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
