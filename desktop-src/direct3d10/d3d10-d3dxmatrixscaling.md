---
description: "Funzione D3DXMatrixScaling (D3DX10Math.h): compila una matrice che viene ridimensionata lungo l'asse x, l'asse y e l'asse z."
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: Funzione D3DXMatrixScaling (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108929"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="38de0-103">Funzione D3DXMatrixScaling (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="38de0-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="38de0-104">Compila una matrice che viene ridimensionata lungo l'asse x, l'asse y e l'asse z.</span><span class="sxs-lookup"><span data-stu-id="38de0-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="38de0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38de0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="38de0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38de0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38de0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38de0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38de0-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="38de0-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="38de0-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="38de0-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="38de0-110">*sx* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="38de0-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de0-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38de0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38de0-112">Fattore di scala applicato lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="38de0-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="38de0-113">*sy* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="38de0-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de0-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38de0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38de0-115">Fattore di scala applicato lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="38de0-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="38de0-116">*sz* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="38de0-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de0-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38de0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38de0-118">Fattore di scala applicato lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="38de0-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38de0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38de0-119">Return value</span></span>

<span data-ttu-id="38de0-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="38de0-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="38de0-121">Puntatore alla trasformazione di ridimensionamento D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="38de0-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="38de0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="38de0-122">Remarks</span></span>

<span data-ttu-id="38de0-123">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="38de0-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="38de0-124">In questo modo, la funzione D3DXMatrixScaling può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="38de0-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38de0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38de0-125">Requirements</span></span>



| <span data-ttu-id="38de0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="38de0-126">Requirement</span></span> | <span data-ttu-id="38de0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="38de0-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38de0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38de0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="38de0-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="38de0-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="38de0-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="38de0-130">Library</span></span><br/> | <dl> <span data-ttu-id="38de0-131"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38de0-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38de0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38de0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38de0-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="38de0-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
