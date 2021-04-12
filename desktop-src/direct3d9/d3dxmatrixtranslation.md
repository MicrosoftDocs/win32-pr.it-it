---
description: Compila una matrice utilizzando gli offset specificati.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Funzione D3DXMatrixTranslation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354784"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="a0f4b-103">Funzione D3DXMatrixTranslation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a0f4b-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="a0f4b-104">Compila una matrice utilizzando gli offset specificati.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f4b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="a0f4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f4b-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a0f4b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f4b-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0f4b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0f4b-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0f4b-110">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f4b-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f4b-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f4b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f4b-112">Offset della coordinata X.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="a0f4b-113">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f4b-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f4b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f4b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f4b-115">Offset della coordinata Y.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="a0f4b-116">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f4b-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f4b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f4b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f4b-118">Offset della coordinata Z.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f4b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f4b-119">Return value</span></span>

<span data-ttu-id="a0f4b-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0f4b-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0f4b-121">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che contiene una matrice di trasformazione convertita.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f4b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f4b-122">Remarks</span></span>

<span data-ttu-id="a0f4b-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a0f4b-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a0f4b-124">In questo modo, D3DXMATRIXTranslation può essere utilizzato come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f4b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f4b-125">Requirements</span></span>



| <span data-ttu-id="a0f4b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f4b-126">Requirement</span></span> | <span data-ttu-id="a0f4b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f4b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f4b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f4b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a0f4b-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f4b-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0f4b-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0f4b-130">Library</span></span><br/> | <dl> <span data-ttu-id="a0f4b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0f4b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0f4b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f4b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f4b-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a0f4b-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
