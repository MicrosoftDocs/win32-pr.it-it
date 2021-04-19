---
description: L'interfaccia IPortableDevicePropVariantCollection include una raccolta di valori PROPVARIANT indicizzati dello stesso VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interfaccia IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326693"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="45c86-103">Interfaccia IPortableDevicePropVariantCollection</span><span class="sxs-lookup"><span data-stu-id="45c86-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="45c86-104">L'interfaccia **IPortableDevicePropVariantCollection** include una raccolta di valori **PROPVARIANT** indicizzati dello stesso VARTYPE.</span><span class="sxs-lookup"><span data-stu-id="45c86-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="45c86-105">Il VARTYPE del primo elemento aggiunto alla raccolta determina il VARTYPE della raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="45c86-106">Un tentativo di aggiungere un elemento di un VARTYPE diverso potrebbe non riuscire se non è possibile modificare il valore **PROPVARIANT** nell'elemento VarType corrente della raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="45c86-107">Per modificare il VARTYPE della raccolta, chiamare **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="45c86-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="45c86-108">Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDevicePropVariantCollection**.</span><span class="sxs-lookup"><span data-stu-id="45c86-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="45c86-109">Membri</span><span class="sxs-lookup"><span data-stu-id="45c86-109">Members</span></span>

<span data-ttu-id="45c86-110">L'interfaccia **IPortableDevicePropVariantCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="45c86-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="45c86-111">**IPortableDevicePropVariantCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="45c86-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="45c86-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="45c86-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="45c86-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="45c86-113">Methods</span></span>

<span data-ttu-id="45c86-114">L'interfaccia **IPortableDevicePropVariantCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="45c86-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="45c86-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="45c86-115">Method</span></span>                                                                | <span data-ttu-id="45c86-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45c86-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="45c86-117">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="45c86-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="45c86-118">Aggiunge un elemento alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="45c86-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="45c86-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="45c86-120">Converte tutti gli elementi della raccolta nell'oggetto VARTYPE specificato.</span><span class="sxs-lookup"><span data-stu-id="45c86-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="45c86-121">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="45c86-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="45c86-122">Libera, quindi rimuove tutti gli elementi dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="45c86-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="45c86-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="45c86-124">Recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="45c86-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="45c86-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="45c86-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="45c86-126">Recupera il numero di elementi in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="45c86-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="45c86-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="45c86-128">Recupera il tipo di dati degli elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="45c86-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="45c86-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="45c86-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="45c86-130">Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="45c86-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="45c86-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45c86-131">Requirements</span></span>



| <span data-ttu-id="45c86-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c86-132">Requirement</span></span> | <span data-ttu-id="45c86-133">Valore</span><span class="sxs-lookup"><span data-stu-id="45c86-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c86-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45c86-134">Header</span></span><br/>  | <dl> <span data-ttu-id="45c86-135"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c86-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="45c86-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="45c86-136">Library</span></span><br/> | <dl> <span data-ttu-id="45c86-137"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45c86-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c86-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45c86-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c86-139">**Interfacce di raccolta**</span><span class="sxs-lookup"><span data-stu-id="45c86-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

