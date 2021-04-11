---
description: '\_Struttura D3DXSHADER CONSTANTINFO'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Struttura D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235000"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="7a0db-103">\_Struttura D3DXSHADER CONSTANTINFO</span><span class="sxs-lookup"><span data-stu-id="7a0db-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0db-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a0db-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="7a0db-105">Members</span><span class="sxs-lookup"><span data-stu-id="7a0db-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a0db-106">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7a0db-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-107">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-108">Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni sulle costanti.</span><span class="sxs-lookup"><span data-stu-id="7a0db-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-109">**Registro**</span><span class="sxs-lookup"><span data-stu-id="7a0db-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-111">Set di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7a0db-111">Register set.</span></span> <span data-ttu-id="7a0db-112">Vedere [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="7a0db-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-113">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="7a0db-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-115">Indice del registro.</span><span class="sxs-lookup"><span data-stu-id="7a0db-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-116">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="7a0db-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-117">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-118">Numero di registri.</span><span class="sxs-lookup"><span data-stu-id="7a0db-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7a0db-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-120">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7a0db-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="7a0db-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-124">Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni di [**\_ TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0db-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="7a0db-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="7a0db-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="7a0db-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0db-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a0db-127">Offset dall'inizio della struttura, in byte, alla stringa che contiene il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a0db-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a0db-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a0db-128">Requirements</span></span>



| <span data-ttu-id="7a0db-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0db-129">Requirement</span></span> | <span data-ttu-id="7a0db-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7a0db-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0db-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a0db-131">Header</span></span><br/> | <dl> <span data-ttu-id="7a0db-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0db-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0db-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a0db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0db-134">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="7a0db-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
