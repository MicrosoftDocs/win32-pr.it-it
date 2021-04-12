---
description: Restituisce il determinante di una matrice.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Funzione D3DXMatrixDeterminant (D3dx9math. h)
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
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354209"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="4df29-103">Funzione D3DXMatrixDeterminant (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4df29-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="4df29-104">Restituisce il determinante di una matrice.</span><span class="sxs-lookup"><span data-stu-id="4df29-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df29-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4df29-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4df29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4df29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df29-107">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df29-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df29-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4df29-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4df29-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4df29-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df29-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4df29-110">Return value</span></span>

<span data-ttu-id="4df29-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df29-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df29-112">Restituisce il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="4df29-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df29-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4df29-113">Requirements</span></span>



| <span data-ttu-id="4df29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df29-114">Requirement</span></span> | <span data-ttu-id="4df29-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4df29-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df29-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4df29-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4df29-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df29-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4df29-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="4df29-118">Library</span></span><br/> | <dl> <span data-ttu-id="4df29-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4df29-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4df29-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df29-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df29-121">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4df29-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
