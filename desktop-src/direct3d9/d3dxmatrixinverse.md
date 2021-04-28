---
description: "Funzione D3DXMatrixInverse (D3dx9math.h): calcola l'inverso di una matrice."
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Funzione D3DXMatrixInverse (D3dx9math.h)
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
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098149"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="2afa4-103">Funzione D3DXMatrixInverse (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2afa4-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="2afa4-104">Calcola l'inverso di una matrice.</span><span class="sxs-lookup"><span data-stu-id="2afa4-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afa4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2afa4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2afa4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2afa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afa4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2afa4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2afa4-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2afa4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2afa4-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2afa4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2afa4-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2afa4-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2afa4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2afa4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2afa4-112">Puntatore a un valore FLOAT contenente il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="2afa4-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="2afa4-113">Se il determinante non è necessario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="2afa4-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2afa4-114">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2afa4-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2afa4-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2afa4-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2afa4-116">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="2afa4-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afa4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2afa4-117">Return value</span></span>

<span data-ttu-id="2afa4-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2afa4-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2afa4-119">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta l'inverso della matrice.</span><span class="sxs-lookup"><span data-stu-id="2afa4-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="2afa4-120">Se l'inversione della matrice ha esito negativo, **viene restituito** NULL.</span><span class="sxs-lookup"><span data-stu-id="2afa4-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="2afa4-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="2afa4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2afa4-122">In questo modo, la **funzione D3DXMatrixInverse** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2afa4-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afa4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2afa4-123">Requirements</span></span>



| <span data-ttu-id="2afa4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2afa4-124">Requirement</span></span> | <span data-ttu-id="2afa4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2afa4-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2afa4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2afa4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2afa4-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2afa4-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2afa4-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="2afa4-128">Library</span></span><br/> | <dl> <span data-ttu-id="2afa4-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2afa4-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2afa4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2afa4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afa4-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2afa4-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
