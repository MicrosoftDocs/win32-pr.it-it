---
description: Converte una matrice di float a 16 bit in float a 32 bit.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Funzione D3DXFloat16To32Array (D3dx9math. h)
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
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322690"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="3f723-103">Funzione D3DXFloat16To32Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3f723-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="3f723-104">Converte una matrice di float a 16 bit in float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3f723-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f723-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f723-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="3f723-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f723-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f723-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3f723-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f723-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f723-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f723-109">Puntatore alla matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3f723-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="3f723-110">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f723-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f723-111">Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f723-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="3f723-112">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3f723-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="3f723-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f723-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f723-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f723-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f723-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3f723-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f723-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f723-116">Return value</span></span>

<span data-ttu-id="3f723-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f723-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f723-118">Puntatore a una matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3f723-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f723-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f723-119">Requirements</span></span>



| <span data-ttu-id="3f723-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f723-120">Requirement</span></span> | <span data-ttu-id="3f723-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3f723-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f723-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f723-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3f723-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f723-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3f723-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f723-124">Library</span></span><br/> | <dl> <span data-ttu-id="3f723-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f723-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f723-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f723-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f723-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3f723-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
