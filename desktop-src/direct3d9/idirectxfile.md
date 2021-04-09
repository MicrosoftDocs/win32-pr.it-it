---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFile per creare istanze delle interfacce IDirectXFileEnumObject e IDirectXFileSaveObject e per registrare i modelli. Deprecato.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interfaccia IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886316"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="1f7fd-104">Interfaccia IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="1f7fd-104">IDirectXFile interface</span></span>

<span data-ttu-id="1f7fd-105">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFile per creare istanze delle interfacce [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) e per registrare i modelli.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="1f7fd-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="1f7fd-107">Membri</span><span class="sxs-lookup"><span data-stu-id="1f7fd-107">Members</span></span>

<span data-ttu-id="1f7fd-108">L'interfaccia **IDirectXFile** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1f7fd-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f7fd-109">**IDirectXFile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1f7fd-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="1f7fd-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="1f7fd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f7fd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="1f7fd-111">Methods</span></span>

<span data-ttu-id="1f7fd-112">L'interfaccia **IDirectXFile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="1f7fd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f7fd-113">Method</span></span>                                                       | <span data-ttu-id="1f7fd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f7fd-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="1f7fd-115">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="1f7fd-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="1f7fd-116">Crea un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-116">Creates an enumerator object.</span></span> <span data-ttu-id="1f7fd-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="1f7fd-118">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="1f7fd-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="1f7fd-119">Crea un oggetto Save.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-119">Creates a save object.</span></span> <span data-ttu-id="1f7fd-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="1f7fd-121">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="1f7fd-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="1f7fd-122">Registra i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-122">Registers custom templates.</span></span> <span data-ttu-id="1f7fd-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="1f7fd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f7fd-124">Remarks</span></span>

<span data-ttu-id="1f7fd-125">L'identificatore univoco globale (GUID) per l'interfaccia IDirectXFile è IID \_ IDirectXFile.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="1f7fd-126">L'interfaccia IDirectXFile viene ottenuta chiamando la funzione [**DirectXFileCreate**](directxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7fd-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="1f7fd-127">Il tipo LPDIRECTXFILE è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1f7fd-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="1f7fd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f7fd-128">Requirements</span></span>



| <span data-ttu-id="1f7fd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7fd-129">Requirement</span></span> | <span data-ttu-id="1f7fd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fd-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7fd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f7fd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1f7fd-132"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7fd-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f7fd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f7fd-133">Library</span></span><br/> | <dl> <span data-ttu-id="1f7fd-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f7fd-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7fd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f7fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7fd-136">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="1f7fd-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
