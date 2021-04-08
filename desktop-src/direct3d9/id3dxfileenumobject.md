---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati del file figlio nel file e per recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaccia ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969409"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="73034-103">Interfaccia ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="73034-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="73034-104">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileEnumObject per scorrere gli oggetti dati del file figlio nel file e per recuperare un oggetto figlio in base al relativo identificatore univoco globale (GUID) o in base al nome.</span><span class="sxs-lookup"><span data-stu-id="73034-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="73034-105">Membri</span><span class="sxs-lookup"><span data-stu-id="73034-105">Members</span></span>

<span data-ttu-id="73034-106">L'interfaccia **ID3DXFileEnumObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="73034-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73034-107">**ID3DXFileEnumObject** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73034-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="73034-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="73034-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73034-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="73034-109">Methods</span></span>

<span data-ttu-id="73034-110">L'interfaccia **ID3DXFileEnumObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="73034-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="73034-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="73034-111">Method</span></span>                                                                  | <span data-ttu-id="73034-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73034-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="73034-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="73034-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="73034-114">Recupera un oggetto figlio in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="73034-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="73034-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="73034-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="73034-116">Recupera il numero di oggetti figlio in questo oggetto dati di file.</span><span class="sxs-lookup"><span data-stu-id="73034-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="73034-117">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="73034-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="73034-118">Recupera l'oggetto dati con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="73034-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="73034-119">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="73034-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="73034-120">Recupera l'oggetto dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="73034-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="73034-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="73034-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="73034-122">Recupera l'oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="73034-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="73034-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="73034-123">Remarks</span></span>

<span data-ttu-id="73034-124">Il GUID per l'interfaccia ID3DXFileEnumObject è IID \_ ID3DXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="73034-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="73034-125">Il tipo LPD3DXFILEENUMOBJECT è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="73034-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="73034-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73034-126">Requirements</span></span>



| <span data-ttu-id="73034-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="73034-127">Requirement</span></span> | <span data-ttu-id="73034-128">Valore</span><span class="sxs-lookup"><span data-stu-id="73034-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73034-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73034-129">Header</span></span><br/>  | <dl> <span data-ttu-id="73034-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="73034-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="73034-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="73034-131">Library</span></span><br/> | <dl> <span data-ttu-id="73034-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73034-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="73034-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73034-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73034-134">Interfacce di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="73034-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
