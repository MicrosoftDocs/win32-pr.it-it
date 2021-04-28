---
description: 'Funzione D3DXFloat16To32Array (D3DX10Math.h): converte una matrice di valori float a 16 bit in valori float a 32 bit.'
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Funzione D3DXFloat16To32Array (D3DX10Math.h)
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
ms.openlocfilehash: 5ae624fb05ce10447bd3b9082e171dc01224baaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113289"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="d8a4c-103">Funzione D3DXFloat16To32Array (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d8a4c-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="d8a4c-104">Converte una matrice di valori float a 16 bit in valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d8a4c-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a4c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8a4c-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d8a4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8a4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a4c-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8a4c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a4c-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8a4c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8a4c-109">Puntatore alla matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d8a4c-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="d8a4c-110">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8a4c-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a4c-111">Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8a4c-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="d8a4c-112">Puntatore a una matrice di valori float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="d8a4c-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="d8a4c-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8a4c-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a4c-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8a4c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8a4c-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="d8a4c-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a4c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8a4c-116">Return value</span></span>

<span data-ttu-id="d8a4c-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8a4c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8a4c-118">Puntatore a una matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d8a4c-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a4c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8a4c-119">Requirements</span></span>



| <span data-ttu-id="d8a4c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8a4c-120">Requirement</span></span> | <span data-ttu-id="d8a4c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d8a4c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a4c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8a4c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d8a4c-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8a4c-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8a4c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8a4c-124">Library</span></span><br/> | <dl> <span data-ttu-id="d8a4c-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8a4c-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8a4c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8a4c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a4c-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d8a4c-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
