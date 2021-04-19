---
description: Identifica i dati della risorsa. Deprecato.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Struttura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323084"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="5665a-104">Struttura DXFILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="5665a-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="5665a-105">Identifica i dati della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5665a-105">Identifies resource data.</span></span> <span data-ttu-id="5665a-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5665a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5665a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5665a-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="5665a-108">Members</span><span class="sxs-lookup"><span data-stu-id="5665a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5665a-109">**hModule**</span><span class="sxs-lookup"><span data-stu-id="5665a-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="5665a-110">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5665a-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5665a-111">Handle del modulo che contiene la risorsa da caricare.</span><span class="sxs-lookup"><span data-stu-id="5665a-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="5665a-112">Se questo membro è **null**, la risorsa deve essere collegata al file eseguibile che lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="5665a-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="5665a-113">**lpName**</span><span class="sxs-lookup"><span data-stu-id="5665a-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="5665a-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5665a-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5665a-115">Puntatore a una stringa che specifica il nome della risorsa da caricare.</span><span class="sxs-lookup"><span data-stu-id="5665a-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="5665a-116">Ad esempio, se la risorsa è una mesh, questo membro deve specificare il nome del file mesh.</span><span class="sxs-lookup"><span data-stu-id="5665a-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="5665a-117">**lpType**</span><span class="sxs-lookup"><span data-stu-id="5665a-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="5665a-118">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5665a-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5665a-119">Puntatore a una stringa che specifica il tipo definito dall'utente che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5665a-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5665a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5665a-120">Remarks</span></span>

<span data-ttu-id="5665a-121">Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](idirectxfile--createenumobject.md) e specifica DXFILELOAD \_ FROMRESOURCE.</span><span class="sxs-lookup"><span data-stu-id="5665a-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5665a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5665a-122">Requirements</span></span>



| <span data-ttu-id="5665a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5665a-123">Requirement</span></span> | <span data-ttu-id="5665a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5665a-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5665a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5665a-125">Header</span></span><br/> | <dl> <span data-ttu-id="5665a-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5665a-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5665a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5665a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5665a-128">Strutture di file X</span><span class="sxs-lookup"><span data-stu-id="5665a-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="5665a-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="5665a-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="5665a-130">Costanti DXFILE</span><span class="sxs-lookup"><span data-stu-id="5665a-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
