---
description: L'interfaccia IPortableDeviceValuesCollection include una raccolta di interfacce IPortableDeviceValues indicizzate in base zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interfaccia IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324505"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="cfe3e-103">Interfaccia IPortableDeviceValuesCollection</span><span class="sxs-lookup"><span data-stu-id="cfe3e-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="cfe3e-104">L'interfaccia **IPortableDeviceValuesCollection** include una raccolta di interfacce **IPortableDeviceValues** indicizzate in base zero.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="cfe3e-105">Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceValuesCollection**.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="cfe3e-106">Membri</span><span class="sxs-lookup"><span data-stu-id="cfe3e-106">Members</span></span>

<span data-ttu-id="cfe3e-107">L'interfaccia **IPortableDeviceValuesCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cfe3e-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cfe3e-108">**IPortableDeviceValuesCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cfe3e-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="cfe3e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="cfe3e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cfe3e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="cfe3e-110">Methods</span></span>

<span data-ttu-id="cfe3e-111">L'interfaccia **IPortableDeviceValuesCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="cfe3e-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="cfe3e-112">Method</span></span>                                                       | <span data-ttu-id="cfe3e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe3e-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfe3e-114">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="cfe3e-115">Aggiunge un elemento alla raccolta</span><span class="sxs-lookup"><span data-stu-id="cfe3e-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="cfe3e-116">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="cfe3e-117">Rilascia tutti gli elementi dall'insieme.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="cfe3e-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="cfe3e-119">Recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="cfe3e-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="cfe3e-121">Recupera il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="cfe3e-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="cfe3e-123">Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="cfe3e-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cfe3e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfe3e-124">Requirements</span></span>



| <span data-ttu-id="cfe3e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe3e-125">Requirement</span></span> | <span data-ttu-id="cfe3e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe3e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe3e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfe3e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cfe3e-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe3e-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfe3e-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="cfe3e-129">Library</span></span><br/> | <dl> <span data-ttu-id="cfe3e-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfe3e-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe3e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfe3e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe3e-132">**Interfacce di raccolta**</span><span class="sxs-lookup"><span data-stu-id="cfe3e-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

