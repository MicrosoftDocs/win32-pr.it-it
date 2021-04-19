---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interfaccia IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322528"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="dd538-103">Interfaccia IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="dd538-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="dd538-104">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileSaveObject per creare oggetti dati e salvare modelli e oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="dd538-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="dd538-105">Si noti che i modelli non sono necessari in ogni file.</span><span class="sxs-lookup"><span data-stu-id="dd538-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="dd538-106">È ad esempio possibile inserire tutti i modelli in un singolo file Microsoft DirectX anziché duplicarli in ogni file DirectX.</span><span class="sxs-lookup"><span data-stu-id="dd538-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="dd538-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd538-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="dd538-108">Membri</span><span class="sxs-lookup"><span data-stu-id="dd538-108">Members</span></span>

<span data-ttu-id="dd538-109">L'interfaccia **IDirectXFileSaveObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd538-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd538-110">**IDirectXFileSaveObject** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd538-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="dd538-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="dd538-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd538-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="dd538-112">Methods</span></span>

<span data-ttu-id="dd538-113">L'interfaccia **IDirectXFileSaveObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dd538-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="dd538-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd538-114">Method</span></span>                                                               | <span data-ttu-id="dd538-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd538-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="dd538-116">**CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="dd538-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="dd538-117">Crea un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="dd538-117">Creates a data object.</span></span> <span data-ttu-id="dd538-118">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd538-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="dd538-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="dd538-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="dd538-120">Salva un oggetto dati e i relativi elementi figlio in un file DirectX.</span><span class="sxs-lookup"><span data-stu-id="dd538-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="dd538-121">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd538-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="dd538-122">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="dd538-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="dd538-123">Salva i modelli in un file DirectX.</span><span class="sxs-lookup"><span data-stu-id="dd538-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="dd538-124">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd538-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="dd538-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd538-125">Remarks</span></span>

<span data-ttu-id="dd538-126">L'identificatore univoco globale (GUID) per l'interfaccia IDirectXFileSaveObject è **IID \_ IDirectXFileSaveObject**.</span><span class="sxs-lookup"><span data-stu-id="dd538-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="dd538-127">L'interfaccia **IDirectXFileSaveObject** viene ottenuta chiamando il metodo [**IDirectXFile:: CreateSaveObject**](idirectxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="dd538-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="dd538-128">Il tipo **LPDIRECTXFILESAVEOBJECT** è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dd538-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="dd538-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd538-129">Requirements</span></span>



| <span data-ttu-id="dd538-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd538-130">Requirement</span></span> | <span data-ttu-id="dd538-131">Valore</span><span class="sxs-lookup"><span data-stu-id="dd538-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd538-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd538-132">Header</span></span><br/>  | <dl> <span data-ttu-id="dd538-133"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd538-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd538-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd538-134">Library</span></span><br/> | <dl> <span data-ttu-id="dd538-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd538-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd538-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd538-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd538-137">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="dd538-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
