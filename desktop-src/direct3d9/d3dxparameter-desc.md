---
description: Descrive un parametro usato per un oggetto effetto.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Struttura D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234941"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="a4c0b-103">\_Struttura D3DXPARAMETER DESC</span><span class="sxs-lookup"><span data-stu-id="a4c0b-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="a4c0b-104">Descrive un parametro usato per un oggetto effetto.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4c0b-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="a4c0b-106">Members</span><span class="sxs-lookup"><span data-stu-id="a4c0b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4c0b-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-109">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-110">**Semantica**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-112">Significato semantico, detto anche utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-113">**Classe**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-114">Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-115">Classe Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-115">Parameter class.</span></span> <span data-ttu-id="a4c0b-116">Impostare questa impostazione su uno dei valori nella [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="a4c0b-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-118">Tipo: **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-119">Tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-119">Parameter type.</span></span> <span data-ttu-id="a4c0b-120">Impostare questa impostazione su uno dei valori di [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="a4c0b-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-121">**prime righe**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-123">Numero di righe nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-124">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-126">Numero di colonne nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-127">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-129">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-130">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-131">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-132">Numero di annotazioni.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-133">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-135">Numero di membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-136">**Flag**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-138">Attributi di parametro.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-138">Parameter attributes.</span></span> <span data-ttu-id="a4c0b-139">Vedere [costanti di effetto](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a4c0b-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c0b-140">**Byte**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="a4c0b-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c0b-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4c0b-142">Dimensioni, in byte, del parametro.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4c0b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4c0b-143">Requirements</span></span>



| <span data-ttu-id="a4c0b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c0b-144">Requirement</span></span> | <span data-ttu-id="a4c0b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c0b-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c0b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4c0b-146">Header</span></span><br/> | <dl> <span data-ttu-id="a4c0b-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c0b-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c0b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4c0b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c0b-149">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="a4c0b-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
