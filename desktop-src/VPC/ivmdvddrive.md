---
title: Interfaccia IVMDVDDrive (VPCCOMInterfaces. h)
description: Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale. IVMDVDDrive può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Interfaccia IVMDVDDrive Virtual PC
- Interfaccia IVMDVDDrive Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048500"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="e8b9d-106">Interfaccia IVMDVDDrive</span><span class="sxs-lookup"><span data-stu-id="e8b9d-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="e8b9d-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8b9d-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8b9d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8b9d-109">Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="e8b9d-110">**IVMDVDDrive** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b9d-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="e8b9d-111">È possibile aggiungere una nuova unità CD-ROM o DVD-ROM a una macchina virtuale usando il metodo [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b9d-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="e8b9d-112">È possibile rimuovere un'unità CD-ROM o DVD-ROM esistente da una macchina virtuale usando il metodo [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b9d-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="e8b9d-113">È possibile recuperare un oggetto **IVMDVDDrive** dall'oggetto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) restituito dalla proprietà [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b9d-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="e8b9d-114">Membri</span><span class="sxs-lookup"><span data-stu-id="e8b9d-114">Members</span></span>

<span data-ttu-id="e8b9d-115">L'interfaccia **IVMDVDDrive** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e8b9d-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e8b9d-116">**IVMDVDDrive** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e8b9d-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="e8b9d-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="e8b9d-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="e8b9d-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8b9d-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e8b9d-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="e8b9d-119">Methods</span></span>

<span data-ttu-id="e8b9d-120">L'interfaccia **IVMDVDDrive** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="e8b9d-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="e8b9d-121">Method</span></span>                                                   | <span data-ttu-id="e8b9d-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8b9d-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8b9d-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="e8b9d-124">Connette un'unità host all'unità DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="e8b9d-125">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="e8b9d-126">Connette un'immagine ISO all'unità DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="e8b9d-127">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="e8b9d-128">Rilascia un'unità host acquisita dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="e8b9d-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="e8b9d-130">Rilascia un'immagine ISO acquisita dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="e8b9d-131">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="e8b9d-132">Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e8b9d-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8b9d-133">Properties</span></span>

<span data-ttu-id="e8b9d-134">L'interfaccia **IVMDVDDrive** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="e8b9d-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8b9d-135">Property</span></span>                                                          | <span data-ttu-id="e8b9d-136">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e8b9d-136">Access type</span></span>          | <span data-ttu-id="e8b9d-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8b9d-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e8b9d-138">**Attachment**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="e8b9d-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8b9d-139">Read-only</span></span><br/> | <span data-ttu-id="e8b9d-140">Tipo di supporto collegato all'unità DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="e8b9d-141">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="e8b9d-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8b9d-142">Read-only</span></span><br/> | <span data-ttu-id="e8b9d-143">Numero del bus a cui è collegato il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="e8b9d-144">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="e8b9d-145">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8b9d-145">Read-only</span></span><br/> | <span data-ttu-id="e8b9d-146">Numero del dispositivo a cui è collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="e8b9d-147">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="e8b9d-148">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8b9d-148">Read-only</span></span><br/> | <span data-ttu-id="e8b9d-149">Lettera dell'unità host impostata per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="e8b9d-150">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="e8b9d-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="e8b9d-151">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8b9d-151">Read-only</span></span><br/> | <span data-ttu-id="e8b9d-152">Percorso completo del file di immagine impostato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8b9d-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="e8b9d-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8b9d-153">Requirements</span></span>



| <span data-ttu-id="e8b9d-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b9d-154">Requirement</span></span> | <span data-ttu-id="e8b9d-155">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b9d-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b9d-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8b9d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b9d-157">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8b9d-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8b9d-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8b9d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b9d-159">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e8b9d-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8b9d-160">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e8b9d-160">End of client support</span></span><br/>    | <span data-ttu-id="e8b9d-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8b9d-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8b9d-162">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e8b9d-162">Product</span></span><br/>                  | <span data-ttu-id="e8b9d-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8b9d-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8b9d-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8b9d-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8b9d-165"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b9d-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8b9d-166">IID</span><span class="sxs-lookup"><span data-stu-id="e8b9d-166">IID</span></span><br/>                      | <span data-ttu-id="e8b9d-167">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="e8b9d-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

