---
description: 'Funzione D3DXFloat16To32Array (D3dx9math.h): converte una matrice di valori float a 16 bit in float a 32 bit.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Funzione D3DXFloat16To32Array (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107599"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="1d6bf-103">Funzione D3DXFloat16To32Array (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1d6bf-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="1d6bf-104">Converte una matrice di valori float a 16 bit in float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1d6bf-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d6bf-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="1d6bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d6bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d6bf-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1d6bf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6bf-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d6bf-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d6bf-109">Puntatore alla matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1d6bf-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="1d6bf-110">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1d6bf-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6bf-111">Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d6bf-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="1d6bf-112">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1d6bf-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="1d6bf-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d6bf-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6bf-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6bf-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d6bf-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1d6bf-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d6bf-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d6bf-116">Return value</span></span>

<span data-ttu-id="1d6bf-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d6bf-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d6bf-118">Puntatore a una matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1d6bf-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6bf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d6bf-119">Requirements</span></span>



| <span data-ttu-id="1d6bf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d6bf-120">Requirement</span></span> | <span data-ttu-id="1d6bf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1d6bf-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6bf-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d6bf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1d6bf-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1d6bf-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1d6bf-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d6bf-124">Library</span></span><br/> | <dl> <span data-ttu-id="1d6bf-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d6bf-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d6bf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d6bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6bf-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1d6bf-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
