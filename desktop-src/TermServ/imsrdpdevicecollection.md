---
title: Interfaccia IMsRdpDeviceCollection
description: Rappresenta una raccolta di oggetti dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400236"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="99653-105">Interfaccia IMsRdpDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="99653-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="99653-106">Rappresenta una raccolta di oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99653-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="99653-107">Membri</span><span class="sxs-lookup"><span data-stu-id="99653-107">Members</span></span>

<span data-ttu-id="99653-108">L'interfaccia **IMsRdpDeviceCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="99653-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="99653-109">**IMsRdpDeviceCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="99653-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="99653-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="99653-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="99653-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99653-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="99653-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="99653-112">Methods</span></span>

<span data-ttu-id="99653-113">L'interfaccia **IMsRdpDeviceCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="99653-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="99653-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="99653-114">Method</span></span>                                                        | <span data-ttu-id="99653-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99653-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="99653-116">**RescanDevices**</span><span class="sxs-lookup"><span data-stu-id="99653-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="99653-117">Aggiorna l'elenco di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="99653-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="99653-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99653-118">Properties</span></span>

<span data-ttu-id="99653-119">L'interfaccia **IMsRdpDeviceCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="99653-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="99653-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99653-120">Property</span></span>                                                                 | <span data-ttu-id="99653-121">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="99653-121">Access type</span></span>          | <span data-ttu-id="99653-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99653-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="99653-123">**DeviceById**</span><span class="sxs-lookup"><span data-stu-id="99653-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="99653-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="99653-124">Read-only</span></span><br/> | <span data-ttu-id="99653-125">Recupera il dispositivo con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="99653-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="99653-126">**DeviceByIndex**</span><span class="sxs-lookup"><span data-stu-id="99653-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="99653-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="99653-127">Read-only</span></span><br/> | <span data-ttu-id="99653-128">Recupera il dispositivo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="99653-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="99653-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="99653-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="99653-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="99653-130">Read-only</span></span><br/> | <span data-ttu-id="99653-131">Recupera il numero di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="99653-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="99653-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99653-132">Requirements</span></span>



| <span data-ttu-id="99653-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="99653-133">Requirement</span></span> | <span data-ttu-id="99653-134">Valore</span><span class="sxs-lookup"><span data-stu-id="99653-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="99653-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99653-135">Minimum supported client</span></span><br/> | <span data-ttu-id="99653-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99653-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="99653-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99653-137">Minimum supported server</span></span><br/> | <span data-ttu-id="99653-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99653-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="99653-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="99653-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="99653-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99653-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="99653-141">DLL</span><span class="sxs-lookup"><span data-stu-id="99653-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99653-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99653-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="99653-143">IID</span><span class="sxs-lookup"><span data-stu-id="99653-143">IID</span></span><br/>                      | <span data-ttu-id="99653-144">IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="99653-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99653-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99653-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99653-146">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="99653-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="99653-147">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="99653-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

