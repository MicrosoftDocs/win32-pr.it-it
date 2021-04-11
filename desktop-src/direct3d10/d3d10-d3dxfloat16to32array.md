---
description: Converte una matrice di float a 16 bit in float a 32 bit.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Funzione D3DXFloat16To32Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354989"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="652ca-103">Funzione D3DXFloat16To32Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="652ca-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="652ca-104">Converte una matrice di float a 16 bit in float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="652ca-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="652ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="652ca-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="652ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="652ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="652ca-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="652ca-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652ca-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="652ca-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="652ca-109">Puntatore alla matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="652ca-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="652ca-110">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="652ca-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652ca-111">Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="652ca-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="652ca-112">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="652ca-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="652ca-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="652ca-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652ca-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="652ca-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="652ca-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="652ca-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="652ca-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="652ca-116">Return value</span></span>

<span data-ttu-id="652ca-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="652ca-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="652ca-118">Puntatore a una matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="652ca-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="652ca-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="652ca-119">Requirements</span></span>



| <span data-ttu-id="652ca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="652ca-120">Requirement</span></span> | <span data-ttu-id="652ca-121">Valore</span><span class="sxs-lookup"><span data-stu-id="652ca-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="652ca-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="652ca-122">Header</span></span><br/>  | <dl> <span data-ttu-id="652ca-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="652ca-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="652ca-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="652ca-124">Library</span></span><br/> | <dl> <span data-ttu-id="652ca-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="652ca-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="652ca-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="652ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652ca-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="652ca-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
