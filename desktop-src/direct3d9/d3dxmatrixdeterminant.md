---
description: 'Funzione D3DXMatrixDeterminant (D3dx9math.h): restituisce il determinante di una matrice.'
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Funzione D3DXMatrixDeterminant (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098169"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="8bde7-103">Funzione D3DXMatrixDeterminant (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8bde7-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="8bde7-104">Restituisce il determinante di una matrice.</span><span class="sxs-lookup"><span data-stu-id="8bde7-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bde7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bde7-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8bde7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bde7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bde7-107">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8bde7-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bde7-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8bde7-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8bde7-109">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="8bde7-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bde7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bde7-110">Return value</span></span>

<span data-ttu-id="8bde7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bde7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8bde7-112">Restituisce il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="8bde7-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bde7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bde7-113">Requirements</span></span>



| <span data-ttu-id="8bde7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bde7-114">Requirement</span></span> | <span data-ttu-id="8bde7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8bde7-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bde7-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bde7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8bde7-117"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8bde7-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8bde7-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bde7-118">Library</span></span><br/> | <dl> <span data-ttu-id="8bde7-119"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bde7-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8bde7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bde7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bde7-121">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8bde7-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
