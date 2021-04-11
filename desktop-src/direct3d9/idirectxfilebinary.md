---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari. Deprecato.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaccia IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234980"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="97927-104">Interfaccia IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="97927-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="97927-105">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari.</span><span class="sxs-lookup"><span data-stu-id="97927-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="97927-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="97927-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="97927-107">Membri</span><span class="sxs-lookup"><span data-stu-id="97927-107">Members</span></span>

<span data-ttu-id="97927-108">L'interfaccia **IDirectXFileBinary** eredita da [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="97927-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="97927-109">**IDirectXFileBinary** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97927-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="97927-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="97927-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97927-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="97927-111">Methods</span></span>

<span data-ttu-id="97927-112">L'interfaccia **IDirectXFileBinary** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="97927-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="97927-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="97927-113">Method</span></span>                                                 | <span data-ttu-id="97927-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97927-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97927-115">**GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="97927-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="97927-116">Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari.</span><span class="sxs-lookup"><span data-stu-id="97927-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="97927-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="97927-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="97927-118">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="97927-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="97927-119">Recupera le dimensioni dei dati binari.</span><span class="sxs-lookup"><span data-stu-id="97927-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="97927-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="97927-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="97927-121">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="97927-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="97927-122">Legge i dati binari.</span><span class="sxs-lookup"><span data-stu-id="97927-122">Reads the binary data.</span></span> <span data-ttu-id="97927-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="97927-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="97927-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="97927-124">Remarks</span></span>

<span data-ttu-id="97927-125">Il GUID per l'interfaccia IDirectXFileBinary è IID \_ IDirectXFileBinary.</span><span class="sxs-lookup"><span data-stu-id="97927-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="97927-126">Il tipo LPDIRECTXFileBinary è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="97927-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="97927-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97927-127">Requirements</span></span>



| <span data-ttu-id="97927-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="97927-128">Requirement</span></span> | <span data-ttu-id="97927-129">Valore</span><span class="sxs-lookup"><span data-stu-id="97927-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97927-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97927-130">Header</span></span><br/>  | <dl> <span data-ttu-id="97927-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="97927-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="97927-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="97927-132">Library</span></span><br/> | <dl> <span data-ttu-id="97927-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97927-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97927-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97927-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97927-135">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="97927-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="97927-136">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="97927-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




