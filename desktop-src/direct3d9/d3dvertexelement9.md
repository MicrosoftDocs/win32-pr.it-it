---
description: Definisce il layout dei dati del vertice. Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Struttura D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323027"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="e5a67-104">Struttura D3DVERTEXELEMENT9</span><span class="sxs-lookup"><span data-stu-id="e5a67-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="e5a67-105">Definisce il layout dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="e5a67-105">Defines the vertex data layout.</span></span> <span data-ttu-id="e5a67-106">Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.</span><span class="sxs-lookup"><span data-stu-id="e5a67-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5a67-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="e5a67-108">Members</span><span class="sxs-lookup"><span data-stu-id="e5a67-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5a67-109">**Stream**</span><span class="sxs-lookup"><span data-stu-id="e5a67-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-111">Numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="e5a67-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="e5a67-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="e5a67-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-113">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-114">Offset dall'inizio dei dati dei vertici ai dati associati al tipo di dati specifico.</span><span class="sxs-lookup"><span data-stu-id="e5a67-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="e5a67-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e5a67-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-116">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-117">Tipo di dati, specificato come [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="e5a67-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="e5a67-118">Uno dei diversi tipi predefiniti che definiscono le dimensioni dei dati.</span><span class="sxs-lookup"><span data-stu-id="e5a67-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="e5a67-119">Alcuni metodi hanno un tipo implicito.</span><span class="sxs-lookup"><span data-stu-id="e5a67-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="e5a67-120">**Metodo**</span><span class="sxs-lookup"><span data-stu-id="e5a67-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-121">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-122">Il metodo specifica l'elaborazione mosaico, che determina il modo in cui mosaico interpreta o opera sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e5a67-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="e5a67-123">Per ulteriori informazioni, vedere [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="e5a67-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5a67-124">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="e5a67-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-126">Definisce gli elementi per i quali verranno utilizzati i dati. ovvero l'interoperabilità tra layout di dati dei vertici e vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e5a67-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="e5a67-127">Ogni utilizzo agisce per associare una dichiarazione di vertice a un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e5a67-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="e5a67-128">In alcuni casi, hanno un'interpretazione speciale.</span><span class="sxs-lookup"><span data-stu-id="e5a67-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="e5a67-129">Ad esempio, un elemento che specifica \_ la posizione normale o D3DDECLUSAGE \_ di D3DDECLUSAGE viene usato da N-patch mosaico per impostare lo schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="e5a67-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="e5a67-130">Per un elenco della semantica disponibile, vedere [**D3DDECLUSAGE**](./d3ddeclusage.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a67-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="e5a67-131">D3DDECLUSAGE \_ TEXCOORD può essere usato per i campi definiti dall'utente (che non hanno un utilizzo esistente definito).</span><span class="sxs-lookup"><span data-stu-id="e5a67-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="e5a67-132">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="e5a67-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e5a67-133">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5a67-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e5a67-134">Modifica i dati di utilizzo per consentire all'utente di specificare più tipi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e5a67-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a67-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5a67-135">Remarks</span></span>

<span data-ttu-id="e5a67-136">I dati dei vertici vengono definiti mediante una matrice di strutture **D3DVERTEXELEMENT9** .</span><span class="sxs-lookup"><span data-stu-id="e5a67-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="e5a67-137">Usare [**D3DDECL \_ end**](d3ddecl-end.md) per dichiarare l'ultimo elemento nella dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="e5a67-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a67-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5a67-138">Requirements</span></span>



| <span data-ttu-id="e5a67-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a67-139">Requirement</span></span> | <span data-ttu-id="e5a67-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e5a67-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a67-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5a67-141">Header</span></span><br/> | <dl> <span data-ttu-id="e5a67-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a67-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a67-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5a67-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a67-144">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="e5a67-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e5a67-145">Dichiarazione vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5a67-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
