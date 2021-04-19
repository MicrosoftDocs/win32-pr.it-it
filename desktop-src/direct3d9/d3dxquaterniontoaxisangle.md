---
description: Calcola l'asse e l'angolo di rotazione di un quaternione.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Funzione D3DXQuaternionToAxisAngle (D3dx9math. h)
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
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322484"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="35f23-103">Funzione D3DXQuaternionToAxisAngle (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="35f23-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="35f23-104">Calcola l'asse e l'angolo di rotazione di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="35f23-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35f23-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="35f23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35f23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f23-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35f23-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f23-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="35f23-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="35f23-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="35f23-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35f23-110">*pAxis* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="35f23-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35f23-111">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="35f23-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="35f23-112">Questa funzione restituisce un puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che identifica l'asse di rotazione del quaternione.</span><span class="sxs-lookup"><span data-stu-id="35f23-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="35f23-113">*pAngle* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="35f23-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35f23-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="35f23-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="35f23-115">Questa funzione restituisce un puntatore a un valore FLOAT che identifica l'angolo di rotazione del quaternione in radianti.</span><span class="sxs-lookup"><span data-stu-id="35f23-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f23-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35f23-116">Return value</span></span>

<span data-ttu-id="35f23-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="35f23-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35f23-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="35f23-118">Remarks</span></span>

<span data-ttu-id="35f23-119">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="35f23-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f23-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35f23-120">Requirements</span></span>



| <span data-ttu-id="35f23-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f23-121">Requirement</span></span> | <span data-ttu-id="35f23-122">Valore</span><span class="sxs-lookup"><span data-stu-id="35f23-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f23-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35f23-123">Header</span></span><br/>  | <dl> <span data-ttu-id="35f23-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="35f23-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="35f23-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="35f23-125">Library</span></span><br/> | <dl> <span data-ttu-id="35f23-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35f23-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35f23-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35f23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f23-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="35f23-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
