---
description: Determina se una matrice è una matrice di identità.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: Funzione D3DXMatrixIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355434"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="92c3b-103">D3DXMatrixIsIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="92c3b-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="92c3b-104">Determina se una matrice è una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="92c3b-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92c3b-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="92c3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92c3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c3b-107">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92c3b-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c3b-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="92c3b-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92c3b-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che verrà testata per l'identità.</span><span class="sxs-lookup"><span data-stu-id="92c3b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c3b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92c3b-110">Return value</span></span>

<span data-ttu-id="92c3b-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c3b-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92c3b-112">Se la matrice è una matrice di identità, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="92c3b-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="92c3b-113">In caso contrario, la funzione restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="92c3b-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c3b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92c3b-114">Requirements</span></span>



| <span data-ttu-id="92c3b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c3b-115">Requirement</span></span> | <span data-ttu-id="92c3b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="92c3b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c3b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92c3b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="92c3b-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c3b-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="92c3b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="92c3b-119">Library</span></span><br/> | <dl> <span data-ttu-id="92c3b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92c3b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92c3b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92c3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c3b-122">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="92c3b-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="92c3b-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="92c3b-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 
