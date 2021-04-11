---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interfaccia IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132426"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="62f6d-103">Interfaccia IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="62f6d-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="62f6d-104">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati.</span><span class="sxs-lookup"><span data-stu-id="62f6d-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="62f6d-105">Un oggetto riferimento ai dati fa riferimento a un oggetto dati definito in precedenza nel file.</span><span class="sxs-lookup"><span data-stu-id="62f6d-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="62f6d-106">In questo modo è possibile utilizzare lo stesso oggetto più volte senza ripeterlo nel file.</span><span class="sxs-lookup"><span data-stu-id="62f6d-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="62f6d-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="62f6d-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="62f6d-108">Membri</span><span class="sxs-lookup"><span data-stu-id="62f6d-108">Members</span></span>

<span data-ttu-id="62f6d-109">L'interfaccia **IDirectXFileDataReference** eredita da [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="62f6d-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="62f6d-110">**IDirectXFileDataReference** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="62f6d-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="62f6d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="62f6d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62f6d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="62f6d-112">Methods</span></span>

<span data-ttu-id="62f6d-113">L'interfaccia **IDirectXFileDataReference** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="62f6d-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="62f6d-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="62f6d-114">Method</span></span>                                                | <span data-ttu-id="62f6d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62f6d-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="62f6d-116">**Risolvi**</span><span class="sxs-lookup"><span data-stu-id="62f6d-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="62f6d-117">Risolve i riferimenti ai dati.</span><span class="sxs-lookup"><span data-stu-id="62f6d-117">Resolves data references.</span></span> <span data-ttu-id="62f6d-118">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="62f6d-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62f6d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="62f6d-119">Remarks</span></span>

<span data-ttu-id="62f6d-120">Dopo aver determinato che un oggetto è un oggetto riferimento ai dati, usare il metodo [**IDirectXFileDataReference:: Resolve**](idirectxfiledatareference--resolve.md) per recuperare l'oggetto a cui si fa riferimento definito in precedenza nel file.</span><span class="sxs-lookup"><span data-stu-id="62f6d-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="62f6d-121">Per informazioni su come identificare un oggetto riferimento ai dati, vedere l'interfaccia [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="62f6d-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="62f6d-122">Il GUID per l'interfaccia IDirectXFileDataReference è IID \_ IDirectXFileDataReference.</span><span class="sxs-lookup"><span data-stu-id="62f6d-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="62f6d-123">Il tipo LPDIRECTXFILEDataReference è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="62f6d-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="62f6d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f6d-124">Requirements</span></span>



| <span data-ttu-id="62f6d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f6d-125">Requirement</span></span> | <span data-ttu-id="62f6d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="62f6d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62f6d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62f6d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62f6d-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f6d-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="62f6d-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="62f6d-129">Library</span></span><br/> | <dl> <span data-ttu-id="62f6d-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62f6d-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f6d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62f6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f6d-132">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="62f6d-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="62f6d-133">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="62f6d-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




