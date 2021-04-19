---
description: Ottiene una costante cercando il relativo indice.
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'Metodo ID3DXConstantTable:: getconstant (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4ab7318dc4a05f586db77817653e7df59ef6083
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322827"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="fe6fc-103">Metodo ID3DXConstantTable:: getconstant</span><span class="sxs-lookup"><span data-stu-id="fe6fc-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="fe6fc-104">Ottiene una costante cercando il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="fe6fc-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe6fc-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="fe6fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6fc-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6fc-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6fc-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fe6fc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fe6fc-109">Identificatore univoco della struttura di dati padre.</span><span class="sxs-lookup"><span data-stu-id="fe6fc-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="fe6fc-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.</span><span class="sxs-lookup"><span data-stu-id="fe6fc-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe6fc-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fe6fc-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6fc-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe6fc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe6fc-113">Indice in base zero della costante.</span><span class="sxs-lookup"><span data-stu-id="fe6fc-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6fc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe6fc-114">Return value</span></span>

<span data-ttu-id="fe6fc-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fe6fc-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fe6fc-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="fe6fc-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6fc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe6fc-117">Remarks</span></span>

<span data-ttu-id="fe6fc-118">Per ottenere una costante da una matrice di costanti, usare [**ID3DXConstantTable:: Getconstantelement**](id3dxconstanttable--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="fe6fc-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6fc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe6fc-119">Requirements</span></span>



| <span data-ttu-id="fe6fc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6fc-120">Requirement</span></span> | <span data-ttu-id="fe6fc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fe6fc-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6fc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe6fc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fe6fc-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe6fc-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fe6fc-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe6fc-124">Library</span></span><br/> | <dl> <span data-ttu-id="fe6fc-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe6fc-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fe6fc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe6fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6fc-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fe6fc-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
