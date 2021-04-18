---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveObject per scrivere un file con estensione x su disco e per aggiungere e salvare oggetti dati e modelli.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interfaccia ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322619"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="e6323-103">Interfaccia ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="e6323-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="e6323-104">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveObject per scrivere un file con estensione x su disco e per aggiungere e salvare oggetti dati e modelli.</span><span class="sxs-lookup"><span data-stu-id="e6323-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="e6323-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e6323-105">Members</span></span>

<span data-ttu-id="e6323-106">L'interfaccia **ID3DXFileSaveObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e6323-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e6323-107">**ID3DXFileSaveObject** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e6323-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="e6323-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6323-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6323-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6323-109">Methods</span></span>

<span data-ttu-id="e6323-110">L'interfaccia **ID3DXFileSaveObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e6323-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="e6323-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="e6323-111">Method</span></span>                                                      | <span data-ttu-id="e6323-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6323-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6323-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="e6323-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="e6323-114">Aggiunge un oggetto dati come figlio dell'oggetto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="e6323-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="e6323-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="e6323-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="e6323-116">Ottiene l'interfaccia [**ID3DXFile**](id3dxfile.md) dell'oggetto che ha creato questo oggetto **ID3DXFileSaveObject** .</span><span class="sxs-lookup"><span data-stu-id="e6323-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="e6323-117">**Salva**</span><span class="sxs-lookup"><span data-stu-id="e6323-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="e6323-118">Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.</span><span class="sxs-lookup"><span data-stu-id="e6323-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="e6323-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6323-119">Remarks</span></span>

<span data-ttu-id="e6323-120">I modelli non sono necessari in ogni file.</span><span class="sxs-lookup"><span data-stu-id="e6323-120">Templates are not required in every file.</span></span> <span data-ttu-id="e6323-121">È ad esempio possibile inserire tutti i modelli in un unico file con estensione x anziché duplicarli in ogni file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="e6323-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="e6323-122">L'interfaccia ID3DXFileSaveObject viene ottenuta chiamando il metodo [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="e6323-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="e6323-123">L'identificatore univoco globale (GUID) per l'interfaccia ID3DXFileSaveObject è IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="e6323-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="e6323-124">Il tipo LPD3DXFILESAVEOBJECT è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e6323-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="e6323-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6323-125">Requirements</span></span>



| <span data-ttu-id="e6323-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6323-126">Requirement</span></span> | <span data-ttu-id="e6323-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e6323-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6323-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6323-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e6323-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6323-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e6323-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6323-130">Library</span></span><br/> | <dl> <span data-ttu-id="e6323-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6323-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e6323-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6323-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6323-133">Interfacce di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="e6323-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
