---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFile per creare istanze delle interfacce ID3DXFileEnumObject e ID3DXFileSaveObject e per registrare i modelli.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interfaccia ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322989"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="c0ea8-103">Interfaccia ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="c0ea8-103">ID3DXFile interface</span></span>

<span data-ttu-id="c0ea8-104">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFile per creare istanze delle interfacce [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) e per registrare i modelli.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="c0ea8-105">Membri</span><span class="sxs-lookup"><span data-stu-id="c0ea8-105">Members</span></span>

<span data-ttu-id="c0ea8-106">L'interfaccia **ID3DXFile** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0ea8-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0ea8-107">**ID3DXFile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0ea8-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="c0ea8-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0ea8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0ea8-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0ea8-109">Methods</span></span>

<span data-ttu-id="c0ea8-110">L'interfaccia **ID3DXFile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="c0ea8-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0ea8-111">Method</span></span>                                                            | <span data-ttu-id="c0ea8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0ea8-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0ea8-113">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="c0ea8-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="c0ea8-114">Crea un oggetto enumeratore in grado di leggere un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="c0ea8-115">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="c0ea8-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="c0ea8-116">Crea un oggetto Save che verrà utilizzato per salvare i dati in un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="c0ea8-117">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="c0ea8-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="c0ea8-118">Registra i modelli personalizzati, dato un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ea8-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="c0ea8-119">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="c0ea8-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="c0ea8-120">Registra i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c0ea8-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0ea8-121">Remarks</span></span>

<span data-ttu-id="c0ea8-122">Un oggetto ID3DXFile contiene anche un archivio di modelli locale.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="c0ea8-123">Questa risorsa di archiviazione locale può essere aggiunta solo a con i metodi [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) e [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ea8-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="c0ea8-124">Gli oggetti [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) creati con [**ID3DXFile:: CreateEnumObject**](id3dxfile--createenumobject.md) e [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) usano anche l'archivio dei modelli dell'oggetto ID3DXFile padre.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="c0ea8-125">L'interfaccia ID3DXFile viene ottenuta chiamando la funzione [**D3DXFileCreate**](d3dxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ea8-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="c0ea8-126">L'identificatore univoco globale (GUID) per l'interfaccia ID3DXFile è IID \_ ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="c0ea8-127">Il tipo LPD3DXFILE è definito come puntatore all'interfaccia ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="c0ea8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0ea8-128">Requirements</span></span>



| <span data-ttu-id="c0ea8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ea8-129">Requirement</span></span> | <span data-ttu-id="c0ea8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c0ea8-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ea8-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0ea8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c0ea8-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea8-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c0ea8-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0ea8-133">Library</span></span><br/> | <dl> <span data-ttu-id="c0ea8-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea8-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c0ea8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0ea8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ea8-136">Interfacce di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="c0ea8-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
