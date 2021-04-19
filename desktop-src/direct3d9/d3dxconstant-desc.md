---
description: Descrizione di una costante in una tabella di costanti.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Struttura D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323427"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="842f6-103">\_Struttura D3DXCONSTANT DESC</span><span class="sxs-lookup"><span data-stu-id="842f6-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="842f6-104">Descrizione di una costante in una tabella di costanti.</span><span class="sxs-lookup"><span data-stu-id="842f6-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="842f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="842f6-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="842f6-106">Members</span><span class="sxs-lookup"><span data-stu-id="842f6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="842f6-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="842f6-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-109">Nome della costante.</span><span class="sxs-lookup"><span data-stu-id="842f6-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-110">**Registro**</span><span class="sxs-lookup"><span data-stu-id="842f6-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-111">Tipo: **[ **D3DXREGISTER \_ impostato**](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-112">Tipo di dati Constant.</span><span class="sxs-lookup"><span data-stu-id="842f6-112">Constant data type.</span></span> <span data-ttu-id="842f6-113">Vedere [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="842f6-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="842f6-114">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="842f6-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-116">Indice in base zero della costante nella tabella.</span><span class="sxs-lookup"><span data-stu-id="842f6-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-117">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="842f6-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-119">Numero di registri che contengono dati.</span><span class="sxs-lookup"><span data-stu-id="842f6-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-120">**Classe**</span><span class="sxs-lookup"><span data-stu-id="842f6-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-121">Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-122">Classe Parameter.</span><span class="sxs-lookup"><span data-stu-id="842f6-122">Parameter class.</span></span> <span data-ttu-id="842f6-123">Vedere [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="842f6-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="842f6-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="842f6-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-125">Tipo: **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-126">Tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="842f6-126">Parameter type.</span></span> <span data-ttu-id="842f6-127">Vedere [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="842f6-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="842f6-128">**prime righe**</span><span class="sxs-lookup"><span data-stu-id="842f6-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-130">Numero di righe.</span><span class="sxs-lookup"><span data-stu-id="842f6-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-131">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="842f6-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-133">Numero di colonne.</span><span class="sxs-lookup"><span data-stu-id="842f6-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-134">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="842f6-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-136">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="842f6-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-137">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="842f6-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-139">Numero di sottoparametri dei membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="842f6-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-140">**Byte**</span><span class="sxs-lookup"><span data-stu-id="842f6-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-142">Dimensioni dei dati in numero di byte.</span><span class="sxs-lookup"><span data-stu-id="842f6-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="842f6-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="842f6-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="842f6-144">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842f6-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="842f6-145">Puntatore al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="842f6-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="842f6-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842f6-146">Requirements</span></span>



| <span data-ttu-id="842f6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="842f6-147">Requirement</span></span> | <span data-ttu-id="842f6-148">Valore</span><span class="sxs-lookup"><span data-stu-id="842f6-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="842f6-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="842f6-149">Header</span></span><br/> | <dl> <span data-ttu-id="842f6-150"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="842f6-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842f6-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="842f6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842f6-152">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="842f6-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="842f6-153">**D3DXCONSTANTTABLE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="842f6-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
