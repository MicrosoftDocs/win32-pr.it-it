---
description: Descrizione della tabella delle costanti.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: Struttura D3DXCONSTANTTABLE_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762095"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="c7a0c-103">\_Struttura D3DXCONSTANTTABLE DESC</span><span class="sxs-lookup"><span data-stu-id="c7a0c-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="c7a0c-104">Descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a0c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7a0c-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="c7a0c-106">Members</span><span class="sxs-lookup"><span data-stu-id="c7a0c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7a0c-107">**Autore**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="c7a0c-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7a0c-109">Nome del creatore della tabella di costanti.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="c7a0c-110">**Versione**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c7a0c-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7a0c-112">Versione shader.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="c7a0c-113">**Costanti**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="c7a0c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7a0c-115">Numero di costanti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7a0c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7a0c-116">Requirements</span></span>



| <span data-ttu-id="c7a0c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7a0c-117">Requirement</span></span> | <span data-ttu-id="c7a0c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c7a0c-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a0c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7a0c-119">Header</span></span><br/> | <dl> <span data-ttu-id="c7a0c-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a0c-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a0c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7a0c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a0c-122">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c7a0c-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="c7a0c-123">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="c7a0c-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
