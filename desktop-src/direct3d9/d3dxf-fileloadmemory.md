---
description: Identifica i dati di memoria.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Struttura D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969356"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="c12d8-103">\_Struttura D3DXF FILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="c12d8-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="c12d8-104">Identifica i dati di memoria.</span><span class="sxs-lookup"><span data-stu-id="c12d8-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c12d8-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="c12d8-106">Members</span><span class="sxs-lookup"><span data-stu-id="c12d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c12d8-107">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="c12d8-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="c12d8-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c12d8-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c12d8-109">Puntatore a un blocco di memoria da caricare.</span><span class="sxs-lookup"><span data-stu-id="c12d8-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c12d8-110">**dSize**</span><span class="sxs-lookup"><span data-stu-id="c12d8-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="c12d8-111">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c12d8-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c12d8-112">Dimensione del blocco di memoria da caricare, in byte.</span><span class="sxs-lookup"><span data-stu-id="c12d8-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c12d8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c12d8-113">Remarks</span></span>

<span data-ttu-id="c12d8-114">Questa struttura identifica i dati da caricare dalla memoria quando un'applicazione usa il metodo [**CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il \_ flag D3DXF fileload \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c12d8-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="c12d8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c12d8-115">Requirements</span></span>



| <span data-ttu-id="c12d8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c12d8-116">Requirement</span></span> | <span data-ttu-id="c12d8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c12d8-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c12d8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c12d8-118">Header</span></span><br/> | <dl> <span data-ttu-id="c12d8-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="c12d8-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c12d8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c12d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12d8-121">Strutture di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="c12d8-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
