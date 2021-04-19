---
description: Compila una matrice che si ridimensiona lungo l'asse x, l'asse y e l'asse z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Funzione D3DXMatrixScaling (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322122"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="a4442-103">Funzione D3DXMatrixScaling (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a4442-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="a4442-104">Compila una matrice che si ridimensiona lungo l'asse x, l'asse y e l'asse z.</span><span class="sxs-lookup"><span data-stu-id="a4442-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4442-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4442-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="a4442-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4442-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a4442-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4442-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4442-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4442-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a4442-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4442-110">*SX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4442-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4442-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4442-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4442-112">Fattore di scala applicato lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a4442-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a4442-113">*SY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4442-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4442-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4442-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4442-115">Fattore di scala applicato lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a4442-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a4442-116">*SZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4442-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4442-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4442-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4442-118">Fattore di scala applicato lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="a4442-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4442-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4442-119">Return value</span></span>

<span data-ttu-id="a4442-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4442-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4442-121">Puntatore alla trasformazione di scala [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a4442-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4442-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4442-122">Remarks</span></span>

<span data-ttu-id="a4442-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a4442-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a4442-124">In questo modo, la funzione **D3DXMatrixScaling** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a4442-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4442-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4442-125">Requirements</span></span>



| <span data-ttu-id="a4442-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4442-126">Requirement</span></span> | <span data-ttu-id="a4442-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a4442-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4442-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4442-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a4442-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4442-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4442-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4442-130">Library</span></span><br/> | <dl> <span data-ttu-id="a4442-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4442-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4442-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4442-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4442-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a4442-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
