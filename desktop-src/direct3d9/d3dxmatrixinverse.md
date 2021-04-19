---
description: Calcola l'inverso di una matrice.
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Funzione D3DXMatrixInverse (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eac1072c0174a03482e60167180f900588a13a72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322504"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="19cc0-103">Funzione D3DXMatrixInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="19cc0-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="19cc0-104">Calcola l'inverso di una matrice.</span><span class="sxs-lookup"><span data-stu-id="19cc0-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cc0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19cc0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="19cc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19cc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cc0-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="19cc0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc0-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="19cc0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19cc0-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="19cc0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19cc0-110">*pDeterminant* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="19cc0-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="19cc0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="19cc0-112">Puntatore a un valore FLOAT contenente il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="19cc0-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="19cc0-113">Se il determinante non è necessario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="19cc0-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19cc0-114">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19cc0-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc0-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="19cc0-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19cc0-116">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="19cc0-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cc0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19cc0-117">Return value</span></span>

<span data-ttu-id="19cc0-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="19cc0-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19cc0-119">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta l'inverso della matrice.</span><span class="sxs-lookup"><span data-stu-id="19cc0-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="19cc0-120">Se la matrice Inversion ha esito negativo, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="19cc0-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="19cc0-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="19cc0-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="19cc0-122">In questo modo, la funzione **D3DXMatrixInverse** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="19cc0-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cc0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19cc0-123">Requirements</span></span>



| <span data-ttu-id="19cc0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19cc0-124">Requirement</span></span> | <span data-ttu-id="19cc0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="19cc0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19cc0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19cc0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="19cc0-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19cc0-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="19cc0-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="19cc0-128">Library</span></span><br/> | <dl> <span data-ttu-id="19cc0-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19cc0-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19cc0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19cc0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cc0-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="19cc0-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
