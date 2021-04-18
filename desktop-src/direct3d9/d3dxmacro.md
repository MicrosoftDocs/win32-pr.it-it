---
description: Descrive le definizioni del preprocessore utilizzate da un oggetto effetto.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Struttura D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323247"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="9c824-103">Struttura D3DXMACRO</span><span class="sxs-lookup"><span data-stu-id="9c824-103">D3DXMACRO structure</span></span>

<span data-ttu-id="9c824-104">Descrive le definizioni del preprocessore utilizzate da un oggetto effetto.</span><span class="sxs-lookup"><span data-stu-id="9c824-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c824-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c824-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="9c824-106">Members</span><span class="sxs-lookup"><span data-stu-id="9c824-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c824-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9c824-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="9c824-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c824-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c824-109">Nome del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="9c824-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="9c824-110">**Definition**</span><span class="sxs-lookup"><span data-stu-id="9c824-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="9c824-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c824-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c824-112">Nome della definizione.</span><span class="sxs-lookup"><span data-stu-id="9c824-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c824-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c824-113">Remarks</span></span>

<span data-ttu-id="9c824-114">Per usare **D3DXMACRO** in più di una riga, anteporre a ogni carattere di nuova riga una barra rovesciata (ad esempio, \# define nel linguaggio C).</span><span class="sxs-lookup"><span data-stu-id="9c824-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="9c824-115">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9c824-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="9c824-116">Si notino i 3 caratteri di barra rovesciata alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="9c824-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="9c824-117">I primi due sono necessari per restituire un singolo oggetto ' \\ ', seguito dal carattere di nuova riga " \\ n".</span><span class="sxs-lookup"><span data-stu-id="9c824-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="9c824-118">Facoltativamente, è anche possibile terminare le righe usando " \\ \\ \\ r \\ n".</span><span class="sxs-lookup"><span data-stu-id="9c824-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="9c824-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c824-119">Requirements</span></span>



| <span data-ttu-id="9c824-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c824-120">Requirement</span></span> | <span data-ttu-id="9c824-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9c824-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c824-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c824-122">Header</span></span><br/> | <dl> <span data-ttu-id="9c824-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c824-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c824-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c824-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c824-125">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="9c824-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="9c824-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="9c824-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
