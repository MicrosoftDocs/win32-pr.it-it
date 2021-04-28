---
description: 'Funzione D3DXFloat32To16Array (D3dx9math.h): converte una matrice di valori float a 32 bit in float a 16 bit.'
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Funzione D3DXFloat32To16Array (D3dx9math.h)
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
ms.openlocfilehash: dc00df150c48e285d5478eb9b11df6c5203d6bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094259"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="6367e-103">Funzione D3DXFloat32To16Array (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6367e-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="6367e-104">Converte una matrice di valori float a 32 bit in valori float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6367e-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="6367e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6367e-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="6367e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6367e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6367e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6367e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6367e-108">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="6367e-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="6367e-109">Puntatore alla matrice di valori float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6367e-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="6367e-110">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6367e-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6367e-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6367e-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6367e-112">Puntatore a una matrice di valori float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6367e-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="6367e-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6367e-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6367e-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6367e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6367e-115">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6367e-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6367e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6367e-116">Return value</span></span>

<span data-ttu-id="6367e-117">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="6367e-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="6367e-118">Puntatore a una matrice di valori float a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6367e-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="6367e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6367e-119">Requirements</span></span>



| <span data-ttu-id="6367e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6367e-120">Requirement</span></span> | <span data-ttu-id="6367e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6367e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6367e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6367e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6367e-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6367e-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6367e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="6367e-124">Library</span></span><br/> | <dl> <span data-ttu-id="6367e-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6367e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6367e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6367e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6367e-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6367e-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
