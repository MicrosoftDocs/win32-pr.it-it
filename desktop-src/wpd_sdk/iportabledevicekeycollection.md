---
description: L'interfaccia IPortableDeviceKeyCollection include una raccolta di valori PROPERTYKEY. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare CoCreate con CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interfaccia IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329894"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="db582-104">Interfaccia IPortableDeviceKeyCollection</span><span class="sxs-lookup"><span data-stu-id="db582-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="db582-105">L'interfaccia **IPortableDeviceKeyCollection** include una raccolta di valori **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="db582-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="db582-106">Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceKeyCollection**.</span><span class="sxs-lookup"><span data-stu-id="db582-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="db582-107">Membri</span><span class="sxs-lookup"><span data-stu-id="db582-107">Members</span></span>

<span data-ttu-id="db582-108">L'interfaccia **IPortableDeviceKeyCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db582-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="db582-109">**IPortableDeviceKeyCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db582-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="db582-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="db582-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db582-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="db582-111">Methods</span></span>

<span data-ttu-id="db582-112">L'interfaccia **IPortableDeviceKeyCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="db582-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="db582-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="db582-113">Method</span></span>                                                    | <span data-ttu-id="db582-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db582-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="db582-115">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="db582-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="db582-116">Aggiunge una chiave di proprietà alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="db582-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="db582-117">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="db582-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="db582-118">Elimina tutti gli elementi dall'insieme.</span><span class="sxs-lookup"><span data-stu-id="db582-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="db582-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="db582-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="db582-120">Recupera un **PropertyKey** dalla raccolta in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="db582-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="db582-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="db582-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="db582-122">Recupera il numero di chiavi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="db582-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="db582-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="db582-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="db582-124">Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="db582-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db582-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db582-125">Requirements</span></span>



| <span data-ttu-id="db582-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="db582-126">Requirement</span></span> | <span data-ttu-id="db582-127">Valore</span><span class="sxs-lookup"><span data-stu-id="db582-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db582-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db582-128">Header</span></span><br/>  | <dl> <span data-ttu-id="db582-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="db582-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="db582-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="db582-130">Library</span></span><br/> | <dl> <span data-ttu-id="db582-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db582-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db582-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db582-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db582-133">**Interfacce di raccolta**</span><span class="sxs-lookup"><span data-stu-id="db582-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

