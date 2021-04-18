---
title: Interfaccia IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Definisce la connessione per un disco rigido all'interno della macchina virtuale.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Interfaccia IVMHardDiskConnection Virtual PC
- Interfaccia IVMHardDiskConnection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301848"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="8174c-105">Interfaccia IVMHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="8174c-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="8174c-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8174c-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8174c-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8174c-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8174c-108">Definisce la connessione per un disco rigido all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8174c-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="8174c-109">Viene restituito un oggetto **IVMHardDiskConnection** dal metodo [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="8174c-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="8174c-110">È anche possibile recuperare un oggetto **IVMHardDiskConnection** dall'oggetto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) restituito dalla proprietà [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="8174c-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8174c-111">Membri</span><span class="sxs-lookup"><span data-stu-id="8174c-111">Members</span></span>

<span data-ttu-id="8174c-112">L'interfaccia **IVMHardDiskConnection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8174c-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8174c-113">**IVMHardDiskConnection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8174c-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="8174c-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="8174c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8174c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8174c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8174c-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="8174c-116">Methods</span></span>

<span data-ttu-id="8174c-117">L'interfaccia **IVMHardDiskConnection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8174c-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="8174c-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="8174c-118">Method</span></span>                                                         | <span data-ttu-id="8174c-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8174c-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="8174c-120">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="8174c-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="8174c-121">Imposta la posizione del bus a cui è collegato il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="8174c-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8174c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8174c-122">Properties</span></span>

<span data-ttu-id="8174c-123">L'interfaccia **IVMHardDiskConnection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8174c-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="8174c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8174c-124">Property</span></span>                                                              | <span data-ttu-id="8174c-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="8174c-125">Access type</span></span>          | <span data-ttu-id="8174c-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8174c-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="8174c-127">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="8174c-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="8174c-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8174c-128">Read-only</span></span><br/> | <span data-ttu-id="8174c-129">Numero del bus a cui è collegata l'immagine dell'unità.</span><span class="sxs-lookup"><span data-stu-id="8174c-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="8174c-130">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="8174c-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="8174c-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8174c-131">Read-only</span></span><br/> | <span data-ttu-id="8174c-132">Numero del dispositivo a cui è collegata l'immagine dell'unità.</span><span class="sxs-lookup"><span data-stu-id="8174c-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="8174c-133">**HardDisk**</span><span class="sxs-lookup"><span data-stu-id="8174c-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="8174c-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8174c-134">Read-only</span></span><br/> | <span data-ttu-id="8174c-135">Oggetto disco rigido corrispondente a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="8174c-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="8174c-136">**UndoHardDisk**</span><span class="sxs-lookup"><span data-stu-id="8174c-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="8174c-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8174c-137">Read-only</span></span><br/> | <span data-ttu-id="8174c-138">Oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="8174c-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8174c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8174c-139">Requirements</span></span>



| <span data-ttu-id="8174c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8174c-140">Requirement</span></span> | <span data-ttu-id="8174c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8174c-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8174c-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8174c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8174c-143">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8174c-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8174c-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8174c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8174c-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8174c-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8174c-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8174c-146">End of client support</span></span><br/>    | <span data-ttu-id="8174c-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8174c-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8174c-148">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8174c-148">Product</span></span><br/>                  | <span data-ttu-id="8174c-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8174c-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8174c-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8174c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8174c-151"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8174c-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8174c-152">IID</span><span class="sxs-lookup"><span data-stu-id="8174c-152">IID</span></span><br/>                      | <span data-ttu-id="8174c-153">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="8174c-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

