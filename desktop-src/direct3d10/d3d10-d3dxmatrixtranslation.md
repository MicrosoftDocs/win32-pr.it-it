---
description: Creare una matrice di traslazione.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: Funzione D3DXMatrixTranslation (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323399"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="41352-103">Funzione D3DXMatrixTranslation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="41352-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="41352-104">Creare una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="41352-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="41352-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41352-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="41352-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41352-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="41352-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41352-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41352-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41352-109">Matrice che diventerà una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="41352-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="41352-110">Vedere [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="41352-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="41352-111">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41352-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41352-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41352-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41352-113">Componente x della traslazione.</span><span class="sxs-lookup"><span data-stu-id="41352-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="41352-114">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41352-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41352-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41352-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41352-116">Componente y della traslazione.</span><span class="sxs-lookup"><span data-stu-id="41352-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="41352-117">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41352-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41352-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41352-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41352-119">Componente z della traduzione.</span><span class="sxs-lookup"><span data-stu-id="41352-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41352-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41352-120">Return value</span></span>

<span data-ttu-id="41352-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41352-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41352-122">Matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="41352-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="41352-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41352-123">Requirements</span></span>



| <span data-ttu-id="41352-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="41352-124">Requirement</span></span> | <span data-ttu-id="41352-125">Valore</span><span class="sxs-lookup"><span data-stu-id="41352-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41352-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41352-126">Header</span></span><br/>  | <dl> <span data-ttu-id="41352-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="41352-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="41352-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="41352-128">Library</span></span><br/> | <dl> <span data-ttu-id="41352-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41352-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41352-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41352-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41352-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="41352-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
