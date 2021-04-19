---
description: Converte una matrice di float a 32 bit in float a 16 bit.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Funzione D3DXFloat32To16Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322688"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="8d813-103">Funzione D3DXFloat32To16Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8d813-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="8d813-104">Converte una matrice di float a 32 bit in float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8d813-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d813-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d813-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="8d813-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d813-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8d813-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d813-108">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d813-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="8d813-109">Puntatore alla matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8d813-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="8d813-110">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d813-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d813-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d813-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d813-112">Puntatore a una matrice di float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8d813-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="8d813-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d813-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d813-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d813-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d813-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="8d813-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d813-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d813-116">Return value</span></span>

<span data-ttu-id="8d813-117">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d813-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="8d813-118">Puntatore a una matrice di float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8d813-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d813-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d813-119">Requirements</span></span>



| <span data-ttu-id="8d813-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d813-120">Requirement</span></span> | <span data-ttu-id="8d813-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8d813-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d813-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d813-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8d813-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d813-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8d813-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d813-124">Library</span></span><br/> | <dl> <span data-ttu-id="8d813-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d813-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d813-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d813-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d813-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8d813-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
