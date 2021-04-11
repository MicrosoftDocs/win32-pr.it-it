---
description: Struttura di supporto che contiene informazioni sulla struttura del membro.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Struttura D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354624"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="f32e9-103">\_Struttura D3DXSHADER STRUCTMEMBERINFO</span><span class="sxs-lookup"><span data-stu-id="f32e9-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="f32e9-104">Struttura di supporto che contiene informazioni sulla struttura del membro.</span><span class="sxs-lookup"><span data-stu-id="f32e9-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f32e9-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="f32e9-106">Members</span><span class="sxs-lookup"><span data-stu-id="f32e9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f32e9-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f32e9-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f32e9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f32e9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f32e9-109">Offset dall'inizio della struttura, in byte, alla stringa che contiene il nome del membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="f32e9-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="f32e9-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="f32e9-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f32e9-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f32e9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f32e9-112">Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="f32e9-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="f32e9-113">Vedere [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="f32e9-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f32e9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f32e9-114">Requirements</span></span>



| <span data-ttu-id="f32e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32e9-115">Requirement</span></span> | <span data-ttu-id="f32e9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f32e9-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32e9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f32e9-117">Header</span></span><br/> | <dl> <span data-ttu-id="f32e9-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32e9-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32e9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f32e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32e9-120">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="f32e9-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f32e9-121">**\_TYPEINFO D3DXSHADER**</span><span class="sxs-lookup"><span data-stu-id="f32e9-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
