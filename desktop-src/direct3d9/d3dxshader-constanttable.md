---
description: Struttura di supporto per la gestione di una tabella di costanti shader. Questa operazione può essere eseguita anche usando ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Struttura D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322594"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="1794c-104">\_Struttura D3DXSHADER CONSTANTTABLE</span><span class="sxs-lookup"><span data-stu-id="1794c-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="1794c-105">Struttura di supporto per la gestione di una tabella di costanti shader.</span><span class="sxs-lookup"><span data-stu-id="1794c-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="1794c-106">Questa operazione può essere eseguita anche usando [**ID3DXConstantTable**](id3dxconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="1794c-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1794c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1794c-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="1794c-108">Members</span><span class="sxs-lookup"><span data-stu-id="1794c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1794c-109">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="1794c-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-111">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="1794c-111">Size of the structure.</span></span> <span data-ttu-id="1794c-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1794c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1794c-113">**Autore**</span><span class="sxs-lookup"><span data-stu-id="1794c-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-115">Offset dall'inizio della struttura, in byte, alla stringa che contiene il nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="1794c-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="1794c-116">**Versione**</span><span class="sxs-lookup"><span data-stu-id="1794c-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-118">Versione shader.</span><span class="sxs-lookup"><span data-stu-id="1794c-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="1794c-119">**Costanti**</span><span class="sxs-lookup"><span data-stu-id="1794c-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-121">Numero di costanti.</span><span class="sxs-lookup"><span data-stu-id="1794c-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="1794c-122">**ConstantInfo**</span><span class="sxs-lookup"><span data-stu-id="1794c-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-124">Matrice di informazioni costanti, D3DXSHADER \_ CONSTANTINFO \[ *costanti* \] .</span><span class="sxs-lookup"><span data-stu-id="1794c-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="1794c-125">Vedere [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1794c-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="1794c-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="1794c-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-128">Flag [D3DXSHADER flag](d3dxshader-flags.md) utilizzati per compilare lo shader.</span><span class="sxs-lookup"><span data-stu-id="1794c-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1794c-129">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="1794c-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="1794c-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1794c-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1794c-131">Offset nella stringa che contiene la destinazione.</span><span class="sxs-lookup"><span data-stu-id="1794c-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1794c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="1794c-132">Remarks</span></span>

<span data-ttu-id="1794c-133">Le informazioni sulla costante dello shader sono incluse in una tabella di commenti delimitati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="1794c-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="1794c-134">Tutti gli offset sono misurati in byte a partire dall'inizio della struttura.</span><span class="sxs-lookup"><span data-stu-id="1794c-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="1794c-135">Le voci della tabella Constant sono ordinate in base all'autore in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="1794c-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="1794c-136">Una tabella delle costanti shader può essere gestita con le interfacce [**ID3DXConstantTable**](id3dxconstanttable.md) .</span><span class="sxs-lookup"><span data-stu-id="1794c-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="1794c-137">In alternativa, è possibile gestire la tabella delle costanti con **D3DXSHADER \_ CONSTANTTABLE**.</span><span class="sxs-lookup"><span data-stu-id="1794c-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="1794c-138">Questo membro di dimensione viene spesso inizializzato usando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1794c-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="1794c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1794c-139">Requirements</span></span>



| <span data-ttu-id="1794c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1794c-140">Requirement</span></span> | <span data-ttu-id="1794c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1794c-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1794c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1794c-142">Header</span></span><br/> | <dl> <span data-ttu-id="1794c-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1794c-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1794c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1794c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1794c-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="1794c-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="1794c-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="1794c-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
