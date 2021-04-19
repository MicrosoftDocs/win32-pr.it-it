---
description: Restituisce la dimensione di un vertice per un formato di vertice flessibile (FVF).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Funzione D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322666"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="0c143-103">D3DXGetFVFVertexSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="0c143-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="0c143-104">Restituisce la dimensione di un vertice per un formato di vertice flessibile (FVF).</span><span class="sxs-lookup"><span data-stu-id="0c143-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c143-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c143-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="0c143-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c143-107">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c143-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c143-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c143-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c143-109">FVF su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="0c143-109">FVF to be queried.</span></span> <span data-ttu-id="0c143-110">Combinazione di [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="0c143-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c143-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c143-111">Return value</span></span>

<span data-ttu-id="0c143-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c143-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c143-113">Dimensioni del vertice FVF in byte.</span><span class="sxs-lookup"><span data-stu-id="0c143-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c143-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c143-114">Requirements</span></span>



| <span data-ttu-id="0c143-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c143-115">Requirement</span></span> | <span data-ttu-id="0c143-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c143-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c143-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c143-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0c143-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c143-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0c143-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c143-119">Library</span></span><br/> | <dl> <span data-ttu-id="0c143-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c143-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c143-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c143-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c143-122">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="0c143-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
