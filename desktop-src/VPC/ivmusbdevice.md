---
title: Interfaccia IVMUSBDevice (VPCCOMInterfaces. h)
description: Definisce l'interfaccia per un dispositivo USB collegato all'host. È possibile connettere un dispositivo USB a una macchina virtuale per usare il dispositivo all'interno della macchina virtuale.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Interfaccia IVMUSBDevice Virtual PC
- Interfaccia IVMUSBDevice Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301732"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="601b7-106">Interfaccia IVMUSBDevice</span><span class="sxs-lookup"><span data-stu-id="601b7-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="601b7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="601b7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="601b7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="601b7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="601b7-109">Definisce l'interfaccia per un dispositivo USB collegato all'host.</span><span class="sxs-lookup"><span data-stu-id="601b7-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="601b7-110">È possibile connettere un dispositivo USB a una macchina virtuale per usare il dispositivo all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="601b7-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="601b7-111">Membri</span><span class="sxs-lookup"><span data-stu-id="601b7-111">Members</span></span>

<span data-ttu-id="601b7-112">L'interfaccia **IVMUSBDevice** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="601b7-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="601b7-113">**IVMUSBDevice** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="601b7-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="601b7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="601b7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="601b7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="601b7-115">Properties</span></span>

<span data-ttu-id="601b7-116">L'interfaccia **IVMUSBDevice** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="601b7-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="601b7-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="601b7-117">Property</span></span>                                                                 | <span data-ttu-id="601b7-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="601b7-118">Access type</span></span>          | <span data-ttu-id="601b7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601b7-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="601b7-120">**AttachedToVM**</span><span class="sxs-lookup"><span data-stu-id="601b7-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="601b7-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-121">Read-only</span></span><br/> | <span data-ttu-id="601b7-122">Nome della macchina virtuale a cui è collegato il dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="601b7-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="601b7-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="601b7-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="601b7-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-124">Read-only</span></span><br/> | <span data-ttu-id="601b7-125">Classe dispositivo del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="601b7-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="601b7-126">**DeviceString**</span><span class="sxs-lookup"><span data-stu-id="601b7-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="601b7-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-127">Read-only</span></span><br/> | <span data-ttu-id="601b7-128">Nome del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="601b7-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="601b7-129">**HubID**</span><span class="sxs-lookup"><span data-stu-id="601b7-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="601b7-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-130">Read-only</span></span><br/> | <span data-ttu-id="601b7-131">Identificatore dell'hub a cui è connesso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="601b7-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="601b7-132">**ManufacturerString**</span><span class="sxs-lookup"><span data-stu-id="601b7-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="601b7-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-133">Read-only</span></span><br/> | <span data-ttu-id="601b7-134">Nome del produttore del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="601b7-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="601b7-135">**Porta**</span><span class="sxs-lookup"><span data-stu-id="601b7-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="601b7-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="601b7-136">Read-only</span></span><br/> | <span data-ttu-id="601b7-137">Identificatore della porta a cui è connesso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="601b7-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="601b7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="601b7-138">Requirements</span></span>



| <span data-ttu-id="601b7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="601b7-139">Requirement</span></span> | <span data-ttu-id="601b7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="601b7-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="601b7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="601b7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="601b7-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="601b7-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="601b7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="601b7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="601b7-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="601b7-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="601b7-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="601b7-145">End of client support</span></span><br/>    | <span data-ttu-id="601b7-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="601b7-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="601b7-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="601b7-147">Product</span></span><br/>                  | <span data-ttu-id="601b7-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="601b7-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="601b7-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="601b7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="601b7-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="601b7-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="601b7-151">IID</span><span class="sxs-lookup"><span data-stu-id="601b7-151">IID</span></span><br/>                      | <span data-ttu-id="601b7-152">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="601b7-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

