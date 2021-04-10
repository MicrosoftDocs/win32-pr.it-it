---
title: Interfaccia IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controlla un'unità floppy all'interno di una macchina virtuale.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Interfaccia IVMFloppyDrive Virtual PC
- Interfaccia IVMFloppyDrive Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964773"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="69bed-105">Interfaccia IVMFloppyDrive</span><span class="sxs-lookup"><span data-stu-id="69bed-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="69bed-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="69bed-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69bed-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69bed-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69bed-108">Controlla un'unità floppy all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="69bed-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="69bed-109">**IVMFloppyDrive** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="69bed-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="69bed-110">È possibile recuperare un oggetto **IVMFloppyDrive** dall'oggetto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) restituito dalla proprietà [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="69bed-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="69bed-111">Membri</span><span class="sxs-lookup"><span data-stu-id="69bed-111">Members</span></span>

<span data-ttu-id="69bed-112">L'interfaccia **IVMFloppyDrive** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="69bed-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="69bed-113">**IVMFloppyDrive** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="69bed-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="69bed-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="69bed-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="69bed-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69bed-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="69bed-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="69bed-116">Methods</span></span>

<span data-ttu-id="69bed-117">L'interfaccia **IVMFloppyDrive** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="69bed-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="69bed-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="69bed-118">Method</span></span>                                                      | <span data-ttu-id="69bed-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69bed-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69bed-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="69bed-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="69bed-121">Connette un'unità fisica nell'host all'unità floppy della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="69bed-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="69bed-122">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="69bed-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="69bed-123">Connette un'immagine multimediale floppy sull'host all'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="69bed-124">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="69bed-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="69bed-125">Rilascia un'unità fisica nell'host dall'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="69bed-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="69bed-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="69bed-127">Rilascia un'immagine di supporti floppy nell'host dall'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="69bed-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69bed-128">Properties</span></span>

<span data-ttu-id="69bed-129">L'interfaccia **IVMFloppyDrive** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="69bed-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="69bed-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69bed-130">Property</span></span>                                                             | <span data-ttu-id="69bed-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="69bed-131">Access type</span></span>          | <span data-ttu-id="69bed-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69bed-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69bed-133">**Attachment**</span><span class="sxs-lookup"><span data-stu-id="69bed-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="69bed-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="69bed-134">Read-only</span></span><br/> | <span data-ttu-id="69bed-135">Tipo di supporto collegato all'unità floppy all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="69bed-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="69bed-136">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="69bed-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="69bed-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="69bed-137">Read-only</span></span><br/> | <span data-ttu-id="69bed-138">Indice in base zero del controller a cui è collegata l'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="69bed-139">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="69bed-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="69bed-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="69bed-140">Read-only</span></span><br/> | <span data-ttu-id="69bed-141">Lettera dell'unità host a cui è collegata l'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="69bed-142">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="69bed-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="69bed-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="69bed-143">Read-only</span></span><br/> | <span data-ttu-id="69bed-144">Percorso completo del file di immagine a cui è collegata l'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="69bed-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="69bed-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69bed-145">Requirements</span></span>



| <span data-ttu-id="69bed-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bed-146">Requirement</span></span> | <span data-ttu-id="69bed-147">Valore</span><span class="sxs-lookup"><span data-stu-id="69bed-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bed-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69bed-148">Minimum supported client</span></span><br/> | <span data-ttu-id="69bed-149">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="69bed-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69bed-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69bed-150">Minimum supported server</span></span><br/> | <span data-ttu-id="69bed-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69bed-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69bed-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="69bed-152">End of client support</span></span><br/>    | <span data-ttu-id="69bed-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69bed-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69bed-154">Prodotto</span><span class="sxs-lookup"><span data-stu-id="69bed-154">Product</span></span><br/>                  | <span data-ttu-id="69bed-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69bed-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69bed-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69bed-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="69bed-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bed-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69bed-158">IID</span><span class="sxs-lookup"><span data-stu-id="69bed-158">IID</span></span><br/>                      | <span data-ttu-id="69bed-159">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="69bed-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

