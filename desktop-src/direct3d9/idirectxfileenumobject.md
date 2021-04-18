---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e per recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o in base al nome. Deprecato.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interfaccia IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322538"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="678f2-104">Interfaccia IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="678f2-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="678f2-105">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileEnumObject per scorrere gli oggetti dati nel file e per recuperare un oggetto dati in base al relativo identificatore univoco globale (GUID) o in base al nome.</span><span class="sxs-lookup"><span data-stu-id="678f2-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="678f2-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="678f2-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="678f2-107">Membri</span><span class="sxs-lookup"><span data-stu-id="678f2-107">Members</span></span>

<span data-ttu-id="678f2-108">L'interfaccia **IDirectXFileEnumObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="678f2-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="678f2-109">**IDirectXFileEnumObject** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="678f2-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="678f2-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="678f2-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="678f2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="678f2-111">Methods</span></span>

<span data-ttu-id="678f2-112">L'interfaccia **IDirectXFileEnumObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="678f2-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="678f2-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="678f2-113">Method</span></span>                                                                     | <span data-ttu-id="678f2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="678f2-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="678f2-115">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="678f2-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="678f2-116">Recupera l'oggetto dati con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="678f2-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="678f2-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="678f2-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="678f2-118">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="678f2-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="678f2-119">Recupera l'oggetto dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="678f2-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="678f2-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="678f2-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="678f2-121">**GetNextDataObject**</span><span class="sxs-lookup"><span data-stu-id="678f2-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="678f2-122">Recupera l'oggetto di primo livello successivo nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="678f2-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="678f2-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="678f2-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="678f2-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="678f2-124">Remarks</span></span>

<span data-ttu-id="678f2-125">Il GUID per l'interfaccia IDirectXFileEnumObject è IID \_ IDirectXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="678f2-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="678f2-126">Il tipo LPDIRECTXFILEENUMOBJECT è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="678f2-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="678f2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="678f2-127">Requirements</span></span>



| <span data-ttu-id="678f2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="678f2-128">Requirement</span></span> | <span data-ttu-id="678f2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="678f2-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="678f2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="678f2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="678f2-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="678f2-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="678f2-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="678f2-132">Library</span></span><br/> | <dl> <span data-ttu-id="678f2-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="678f2-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678f2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="678f2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678f2-135">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="678f2-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
