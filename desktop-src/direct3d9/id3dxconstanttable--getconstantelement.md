---
description: Ottiene una costante da una matrice di costanti. Una matrice è costituita da elementi.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Metodo ID3DXConstantTable:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322823"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="4e08e-104">Metodo ID3DXConstantTable:: getconstantelement</span><span class="sxs-lookup"><span data-stu-id="4e08e-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="4e08e-105">Ottiene una costante da una matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="4e08e-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="4e08e-106">Una matrice è costituita da elementi.</span><span class="sxs-lookup"><span data-stu-id="4e08e-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e08e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e08e-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="4e08e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e08e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e08e-109">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e08e-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e08e-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4e08e-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4e08e-111">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="4e08e-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="4e08e-112">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="4e08e-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e08e-113">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4e08e-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e08e-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e08e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e08e-115">Indice in base zero dell'elemento nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4e08e-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e08e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e08e-116">Return value</span></span>

<span data-ttu-id="4e08e-117">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4e08e-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4e08e-118">Restituisce un identificatore univoco della costante dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4e08e-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e08e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e08e-119">Remarks</span></span>

<span data-ttu-id="4e08e-120">Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="4e08e-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e08e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e08e-121">Requirements</span></span>



| <span data-ttu-id="4e08e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e08e-122">Requirement</span></span> | <span data-ttu-id="4e08e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4e08e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e08e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e08e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e08e-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e08e-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4e08e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e08e-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e08e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e08e-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e08e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e08e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e08e-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="4e08e-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
