---
description: Converte una matrice di float a 32 bit in float a 16 bit.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Funzione D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323344"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="11431-103">Funzione D3DXFloat32To16Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="11431-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="11431-104">Converte una matrice di float a 32 bit in float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="11431-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="11431-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11431-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="11431-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11431-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11431-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11431-108">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="11431-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="11431-109">Puntatore alla matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="11431-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="11431-110">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11431-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11431-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="11431-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="11431-112">Puntatore a una matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="11431-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="11431-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11431-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11431-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11431-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11431-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="11431-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11431-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11431-116">Return value</span></span>

<span data-ttu-id="11431-117">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="11431-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="11431-118">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="11431-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="11431-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11431-119">Requirements</span></span>



| <span data-ttu-id="11431-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11431-120">Requirement</span></span> | <span data-ttu-id="11431-121">Valore</span><span class="sxs-lookup"><span data-stu-id="11431-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11431-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11431-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11431-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="11431-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="11431-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="11431-124">Library</span></span><br/> | <dl> <span data-ttu-id="11431-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11431-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11431-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11431-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11431-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="11431-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
