---
description: Ottiene una costante cercandone il nome.
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'Metodo ID3DXConstantTable:: GetConstantByName (D3DX9Shader. h)'
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
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322825"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="f095a-103">Metodo ID3DXConstantTable:: GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="f095a-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="f095a-104">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="f095a-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f095a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f095a-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="f095a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f095a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f095a-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f095a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f095a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f095a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f095a-109">Identificatore univoco della struttura di dati padre.</span><span class="sxs-lookup"><span data-stu-id="f095a-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="f095a-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.</span><span class="sxs-lookup"><span data-stu-id="f095a-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f095a-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f095a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f095a-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f095a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f095a-113">Nome della costante.</span><span class="sxs-lookup"><span data-stu-id="f095a-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f095a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f095a-114">Return value</span></span>

<span data-ttu-id="f095a-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f095a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f095a-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="f095a-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="f095a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f095a-117">Requirements</span></span>



| <span data-ttu-id="f095a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f095a-118">Requirement</span></span> | <span data-ttu-id="f095a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f095a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f095a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f095a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f095a-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f095a-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f095a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f095a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f095a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f095a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f095a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f095a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f095a-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f095a-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
