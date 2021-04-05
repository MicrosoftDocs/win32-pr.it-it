---
description: Crea una matrice di identità.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Funzione D3DXMatrixIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969302"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="e72ed-103">D3DXMatrixIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="e72ed-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="e72ed-104">Crea una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="e72ed-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e72ed-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="e72ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e72ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e72ed-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e72ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e72ed-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e72ed-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e72ed-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e72ed-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e72ed-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e72ed-110">Return value</span></span>

<span data-ttu-id="e72ed-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e72ed-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e72ed-112">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="e72ed-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72ed-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e72ed-113">Remarks</span></span>

<span data-ttu-id="e72ed-114">La matrice di identità è una matrice in cui tutti i coefficienti sono 0 ad eccezione dei coefficienti \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , che sono impostati su 1.</span><span class="sxs-lookup"><span data-stu-id="e72ed-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="e72ed-115">La matrice di identità è speciale in quanto quando viene applicata ai vertici, non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="e72ed-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="e72ed-116">La matrice di identità viene utilizzata come punto di partenza per le matrici che modificheranno i valori dei vertici per creare rotazioni, traduzioni e altre trasformazioni che possono essere rappresentate da una matrice 4 x4.</span><span class="sxs-lookup"><span data-stu-id="e72ed-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="e72ed-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="e72ed-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e72ed-118">In questo modo, la funzione **D3DXMatrixIdentity** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e72ed-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e72ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e72ed-119">Requirements</span></span>



| <span data-ttu-id="e72ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e72ed-120">Requirement</span></span> | <span data-ttu-id="e72ed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e72ed-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e72ed-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e72ed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e72ed-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e72ed-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e72ed-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e72ed-124">Library</span></span><br/> | <dl> <span data-ttu-id="e72ed-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e72ed-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e72ed-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e72ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72ed-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e72ed-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e72ed-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="e72ed-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




