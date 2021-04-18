---
title: Interfaccia IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di dispositivi USB collegati al sistema host. Per ottenere un oggetto IVMUSBDeviceCollection, usare la proprietà IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Interfaccia IVMUSBDeviceCollection Virtual PC
- Interfaccia IVMUSBDeviceCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301562"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="7de37-106">Interfaccia IVMUSBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="7de37-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="7de37-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7de37-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7de37-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7de37-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7de37-109">Definisce la raccolta di dispositivi USB collegati al sistema host.</span><span class="sxs-lookup"><span data-stu-id="7de37-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="7de37-110">Per ottenere un oggetto **IVMUSBDeviceCollection** , usare la proprietà [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7de37-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="7de37-111">Membri</span><span class="sxs-lookup"><span data-stu-id="7de37-111">Members</span></span>

<span data-ttu-id="7de37-112">L'interfaccia **IVMUSBDeviceCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7de37-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7de37-113">**IVMUSBDeviceCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7de37-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="7de37-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7de37-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7de37-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7de37-115">Properties</span></span>

<span data-ttu-id="7de37-116">L'interfaccia **IVMUSBDeviceCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7de37-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="7de37-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7de37-117">Property</span></span>                                                        | <span data-ttu-id="7de37-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7de37-118">Access type</span></span>          | <span data-ttu-id="7de37-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7de37-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="7de37-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="7de37-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="7de37-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7de37-121">Read-only</span></span><br/> | <span data-ttu-id="7de37-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="7de37-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="7de37-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="7de37-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="7de37-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7de37-124">Read-only</span></span><br/> | <span data-ttu-id="7de37-125">Numero di dispositivi USB in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="7de37-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="7de37-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7de37-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="7de37-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7de37-127">Read-only</span></span><br/> | <span data-ttu-id="7de37-128">Oggetto dispositivo USB che corrisponde all'indice specificato (in base 1).</span><span class="sxs-lookup"><span data-stu-id="7de37-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7de37-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7de37-129">Requirements</span></span>



| <span data-ttu-id="7de37-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de37-130">Requirement</span></span> | <span data-ttu-id="7de37-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7de37-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de37-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7de37-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7de37-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7de37-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7de37-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7de37-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7de37-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7de37-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7de37-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7de37-136">End of client support</span></span><br/>    | <span data-ttu-id="7de37-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7de37-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7de37-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7de37-138">Product</span></span><br/>                  | <span data-ttu-id="7de37-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7de37-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7de37-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7de37-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7de37-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de37-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7de37-142">IID</span><span class="sxs-lookup"><span data-stu-id="7de37-142">IID</span></span><br/>                      | <span data-ttu-id="7de37-143">IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="7de37-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="7de37-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7de37-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de37-145">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="7de37-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="7de37-146">**IVMVirtualPC::USBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="7de37-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

