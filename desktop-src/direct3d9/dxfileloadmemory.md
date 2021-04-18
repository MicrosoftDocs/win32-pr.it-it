---
description: Identifica i dati di memoria. Deprecato.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Struttura DXFILELOADMEMORY (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323085"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="fb00a-104">Struttura DXFILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="fb00a-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="fb00a-105">Identifica i dati di memoria.</span><span class="sxs-lookup"><span data-stu-id="fb00a-105">Identifies memory data.</span></span> <span data-ttu-id="fb00a-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="fb00a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb00a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb00a-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="fb00a-108">Members</span><span class="sxs-lookup"><span data-stu-id="fb00a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb00a-109">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="fb00a-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="fb00a-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb00a-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb00a-111">Puntatore a un blocco di memoria da caricare.</span><span class="sxs-lookup"><span data-stu-id="fb00a-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="fb00a-112">**dSize**</span><span class="sxs-lookup"><span data-stu-id="fb00a-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="fb00a-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb00a-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb00a-114">Dimensione del blocco di memoria da caricare, in byte.</span><span class="sxs-lookup"><span data-stu-id="fb00a-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb00a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb00a-115">Remarks</span></span>

<span data-ttu-id="fb00a-116">Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](idirectxfile--createenumobject.md) e specifica DXFILELOAD \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fb00a-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb00a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb00a-117">Requirements</span></span>



| <span data-ttu-id="fb00a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb00a-118">Requirement</span></span> | <span data-ttu-id="fb00a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fb00a-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb00a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb00a-120">Header</span></span><br/> | <dl> <span data-ttu-id="fb00a-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb00a-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb00a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb00a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb00a-123">Strutture di file X</span><span class="sxs-lookup"><span data-stu-id="fb00a-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="fb00a-124">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="fb00a-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="fb00a-125">Costanti DXFILE</span><span class="sxs-lookup"><span data-stu-id="fb00a-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
