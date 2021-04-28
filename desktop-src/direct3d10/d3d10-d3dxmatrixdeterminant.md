---
description: 'Funzione D3DXMatrixDeterminant (D3DX10Math.h): restituisce il determinante di una matrice.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Funzione D3DXMatrixDeterminant (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103459"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="9bc09-103">Funzione D3DXMatrixDeterminant (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="9bc09-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="9bc09-104">Restituisce il determinante di una matrice.</span><span class="sxs-lookup"><span data-stu-id="9bc09-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bc09-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="9bc09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc09-107">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9bc09-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc09-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9bc09-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9bc09-109">Puntatore alla struttura D3DXMATRIX di origine.</span><span class="sxs-lookup"><span data-stu-id="9bc09-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc09-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc09-110">Return value</span></span>

<span data-ttu-id="9bc09-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bc09-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bc09-112">Restituisce il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="9bc09-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc09-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc09-113">Requirements</span></span>



| <span data-ttu-id="9bc09-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc09-114">Requirement</span></span> | <span data-ttu-id="9bc09-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc09-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc09-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc09-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9bc09-117"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc09-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9bc09-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="9bc09-118">Library</span></span><br/> | <dl> <span data-ttu-id="9bc09-119"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bc09-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9bc09-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bc09-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc09-121">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9bc09-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
