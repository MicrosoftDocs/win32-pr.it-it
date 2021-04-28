---
description: 'Funzione D3DXFloat32To16Array (D3DX10Math.h): converte una matrice di valori float a 32 bit in float a 16 bit.'
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Funzione D3DXFloat32To16Array (D3DX10Math.h)
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
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103519"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="fe41f-103">Funzione D3DXFloat32To16Array (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="fe41f-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="fe41f-104">Converte una matrice di valori float a 32 bit in float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fe41f-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe41f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe41f-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="fe41f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe41f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe41f-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe41f-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe41f-108">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe41f-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="fe41f-109">Puntatore alla matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fe41f-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="fe41f-110">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fe41f-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe41f-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe41f-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fe41f-112">Puntatore a una matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fe41f-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="fe41f-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe41f-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe41f-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe41f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe41f-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fe41f-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe41f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe41f-116">Return value</span></span>

<span data-ttu-id="fe41f-117">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe41f-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="fe41f-118">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fe41f-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe41f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe41f-119">Requirements</span></span>



| <span data-ttu-id="fe41f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe41f-120">Requirement</span></span> | <span data-ttu-id="fe41f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fe41f-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe41f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe41f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fe41f-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe41f-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe41f-124">Library</span></span><br/> | <dl> <span data-ttu-id="fe41f-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe41f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe41f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe41f-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fe41f-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
