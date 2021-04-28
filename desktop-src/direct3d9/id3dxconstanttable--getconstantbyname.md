---
description: 'Metodo ID3DXConstantTable::GetConstantByName: ottiene una costante cercandone il nome.'
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: Metodo ID3DXConstantTable::GetConstantByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88461a45bf484a72c085f1776eb923a8534b8be3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115249"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="f3cd8-103">Metodo ID3DXConstantTable::GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="f3cd8-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="f3cd8-104">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="f3cd8-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cd8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3cd8-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="f3cd8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3cd8-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f3cd8-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cd8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f3cd8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f3cd8-109">Identificatore univoco della struttura dei dati padre.</span><span class="sxs-lookup"><span data-stu-id="f3cd8-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="f3cd8-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f3cd8-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3cd8-111">*pName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f3cd8-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cd8-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3cd8-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3cd8-113">Nome della costante.</span><span class="sxs-lookup"><span data-stu-id="f3cd8-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3cd8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3cd8-114">Return value</span></span>

<span data-ttu-id="f3cd8-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f3cd8-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f3cd8-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="f3cd8-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3cd8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3cd8-117">Requirements</span></span>



| <span data-ttu-id="f3cd8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3cd8-118">Requirement</span></span> | <span data-ttu-id="f3cd8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f3cd8-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cd8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3cd8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f3cd8-121"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="f3cd8-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f3cd8-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3cd8-122">Library</span></span><br/> | <dl> <span data-ttu-id="f3cd8-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3cd8-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f3cd8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3cd8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cd8-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f3cd8-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
