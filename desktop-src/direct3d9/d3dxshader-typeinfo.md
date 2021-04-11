---
description: Struttura di supporto che contiene informazioni sul tipo di membro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Struttura D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354714"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="8aa30-103">\_Struttura D3DXSHADER TYPEINFO</span><span class="sxs-lookup"><span data-stu-id="8aa30-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="8aa30-104">Struttura di supporto che contiene informazioni sul tipo di membro.</span><span class="sxs-lookup"><span data-stu-id="8aa30-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa30-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8aa30-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="8aa30-106">Members</span><span class="sxs-lookup"><span data-stu-id="8aa30-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8aa30-107">**Classe**</span><span class="sxs-lookup"><span data-stu-id="8aa30-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-109">Tipo di oggetto shader.</span><span class="sxs-lookup"><span data-stu-id="8aa30-109">Shader object type.</span></span> <span data-ttu-id="8aa30-110">Vedere [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="8aa30-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8aa30-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-112">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-113">Tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="8aa30-113">Data type.</span></span> <span data-ttu-id="8aa30-114">Vedere [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="8aa30-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-115">**prime righe**</span><span class="sxs-lookup"><span data-stu-id="8aa30-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-116">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-117">Numero di righe matrice (matrici).</span><span class="sxs-lookup"><span data-stu-id="8aa30-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-118">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="8aa30-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-119">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-120">Numero di colonne (vettori e matrici).</span><span class="sxs-lookup"><span data-stu-id="8aa30-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-121">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="8aa30-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-122">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-123">Dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="8aa30-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-124">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="8aa30-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-125">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-126">Numero di membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="8aa30-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="8aa30-127">**StructMemberInfo**</span><span class="sxs-lookup"><span data-stu-id="8aa30-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8aa30-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aa30-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aa30-129">Matrice di informazioni sui membri di struttura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] .</span><span class="sxs-lookup"><span data-stu-id="8aa30-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="8aa30-130">Vedere [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="8aa30-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8aa30-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aa30-131">Remarks</span></span>

<span data-ttu-id="8aa30-132">Le informazioni sul tipo fanno parte di [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="8aa30-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa30-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aa30-133">Requirements</span></span>



| <span data-ttu-id="8aa30-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa30-134">Requirement</span></span> | <span data-ttu-id="8aa30-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8aa30-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa30-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aa30-136">Header</span></span><br/> | <dl> <span data-ttu-id="8aa30-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa30-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa30-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aa30-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa30-139">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="8aa30-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="8aa30-140">**\_CONSTANTINFO D3DXSHADER**</span><span class="sxs-lookup"><span data-stu-id="8aa30-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
