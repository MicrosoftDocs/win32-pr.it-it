---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati del file con estensione x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interfaccia ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322623"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="6d079-103">Interfaccia ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="6d079-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="6d079-104">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileSaveData per aggiungere oggetti dati come elementi figlio di un nodo dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="6d079-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="6d079-105">Membri</span><span class="sxs-lookup"><span data-stu-id="6d079-105">Members</span></span>

<span data-ttu-id="6d079-106">L'interfaccia **ID3DXFileSaveData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6d079-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6d079-107">**ID3DXFileSaveData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6d079-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="6d079-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d079-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6d079-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d079-109">Methods</span></span>

<span data-ttu-id="6d079-110">L'interfaccia **ID3DXFileSaveData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6d079-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="6d079-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="6d079-111">Method</span></span>                                                          | <span data-ttu-id="6d079-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d079-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d079-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="6d079-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="6d079-114">Aggiunge un oggetto dati come figlio del nodo dati del file **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="6d079-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="6d079-115">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="6d079-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="6d079-116">Aggiunge un riferimento ai dati come figlio del nodo dati del file **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="6d079-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="6d079-117">Il riferimento ai dati punta a un oggetto dati di file.</span><span class="sxs-lookup"><span data-stu-id="6d079-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="6d079-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="6d079-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="6d079-119">Recupera il GUID del nodo dati del file **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="6d079-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="6d079-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="6d079-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="6d079-121">Recupera il nome del nodo dati del file **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="6d079-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="6d079-122">**Getsave**</span><span class="sxs-lookup"><span data-stu-id="6d079-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="6d079-123">Recupera un puntatore a questo nodo dati del file [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="6d079-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="6d079-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="6d079-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="6d079-125">Recupera l'ID modello del nodo dati del file.</span><span class="sxs-lookup"><span data-stu-id="6d079-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="6d079-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d079-126">Remarks</span></span>

<span data-ttu-id="6d079-127">Il GUID per l'interfaccia ID3DXFileSaveObject è IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="6d079-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="6d079-128">Il tipo LPD3DXFileSaveData è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6d079-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="6d079-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d079-129">Requirements</span></span>



| <span data-ttu-id="6d079-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d079-130">Requirement</span></span> | <span data-ttu-id="6d079-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6d079-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d079-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d079-132">Header</span></span><br/>  | <dl> <span data-ttu-id="6d079-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d079-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="6d079-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d079-134">Library</span></span><br/> | <dl> <span data-ttu-id="6d079-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d079-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6d079-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d079-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d079-137">Interfacce di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="6d079-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
