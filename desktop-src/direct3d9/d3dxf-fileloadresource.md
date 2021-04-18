---
description: Identifica i dati della risorsa.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Struttura D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322704"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="07bf3-103">\_Struttura D3DXF FILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="07bf3-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="07bf3-104">Identifica i dati della risorsa.</span><span class="sxs-lookup"><span data-stu-id="07bf3-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bf3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07bf3-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="07bf3-106">Members</span><span class="sxs-lookup"><span data-stu-id="07bf3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07bf3-107">**hModule**</span><span class="sxs-lookup"><span data-stu-id="07bf3-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="07bf3-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf3-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07bf3-109">Handle del modulo che contiene la risorsa da caricare.</span><span class="sxs-lookup"><span data-stu-id="07bf3-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="07bf3-110">Se questo membro è **null**, la risorsa deve essere collegata al file eseguibile che lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="07bf3-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="07bf3-111">**lpName**</span><span class="sxs-lookup"><span data-stu-id="07bf3-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="07bf3-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf3-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07bf3-113">Puntatore a una stringa che specifica il nome della risorsa da caricare.</span><span class="sxs-lookup"><span data-stu-id="07bf3-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="07bf3-114">Ad esempio, se la risorsa è una mesh, questo membro deve specificare il nome del file mesh.</span><span class="sxs-lookup"><span data-stu-id="07bf3-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="07bf3-115">**lpType**</span><span class="sxs-lookup"><span data-stu-id="07bf3-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="07bf3-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf3-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07bf3-117">Puntatore a una stringa che specifica il tipo definito dall'utente che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="07bf3-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07bf3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="07bf3-118">Remarks</span></span>

<span data-ttu-id="07bf3-119">Questa struttura identifica una risorsa da caricare quando un'applicazione usa il metodo [**CreateEnumObject**](id3dxfile--createenumobject.md) e specifica il flag [D3DXF \_ fileload \_ FROMRESOURCE](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="07bf3-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="07bf3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07bf3-120">Requirements</span></span>



| <span data-ttu-id="07bf3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07bf3-121">Requirement</span></span> | <span data-ttu-id="07bf3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="07bf3-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07bf3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07bf3-123">Header</span></span><br/> | <dl> <span data-ttu-id="07bf3-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="07bf3-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07bf3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07bf3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bf3-126">Strutture di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="07bf3-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
