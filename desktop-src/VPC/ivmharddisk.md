---
title: Interfaccia IVMHardDisk (VPCCOMInterfaces. h)
description: Consente di accedere a un'immagine del disco rigido. È possibile accedervi tramite la proprietà IVMHardDiskConnection HardDisk o il metodo IVMVirtualPC getharddisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Interfaccia IVMHardDisk Virtual PC
- Interfaccia IVMHardDisk Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475040"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="e6df8-106">Interfaccia IVMHardDisk</span><span class="sxs-lookup"><span data-stu-id="e6df8-106">IVMHardDisk interface</span></span>

<span data-ttu-id="e6df8-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6df8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6df8-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6df8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6df8-109">Consente di accedere a un'immagine del disco rigido.</span><span class="sxs-lookup"><span data-stu-id="e6df8-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="e6df8-110">È possibile accedervi tramite la proprietà [**IVMHardDiskConnection:: harddisk**](ivmharddiskconnection-harddisk.md) o il metodo [**IVMVirtualPC:: getharddisk**](ivmvirtualpc-getharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="e6df8-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="e6df8-111">Membri</span><span class="sxs-lookup"><span data-stu-id="e6df8-111">Members</span></span>

<span data-ttu-id="e6df8-112">L'interfaccia **IVMHardDisk** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e6df8-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e6df8-113">**IVMHardDisk** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e6df8-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="e6df8-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6df8-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6df8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6df8-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6df8-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6df8-116">Methods</span></span>

<span data-ttu-id="e6df8-117">L'interfaccia **IVMHardDisk** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e6df8-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="e6df8-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="e6df8-118">Method</span></span>                                 | <span data-ttu-id="e6df8-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6df8-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6df8-120">**Compact**</span><span class="sxs-lookup"><span data-stu-id="e6df8-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="e6df8-121">Compatta un'immagine del disco rigido virtuale ad espansione dinamica.</span><span class="sxs-lookup"><span data-stu-id="e6df8-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="e6df8-122">**Convertire**</span><span class="sxs-lookup"><span data-stu-id="e6df8-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="e6df8-123">Converte qualsiasi disco rigido virtuale in un disco rigido virtuale a espansione dinamica o a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="e6df8-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="e6df8-124">**Unione**</span><span class="sxs-lookup"><span data-stu-id="e6df8-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="e6df8-125">Unisce un disco rigido virtuale differenze con l'immagine del disco padre.</span><span class="sxs-lookup"><span data-stu-id="e6df8-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="e6df8-126">**MergeTo**</span><span class="sxs-lookup"><span data-stu-id="e6df8-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="e6df8-127">Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice) in un nuovo file di disco rigido.</span><span class="sxs-lookup"><span data-stu-id="e6df8-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6df8-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6df8-128">Properties</span></span>

<span data-ttu-id="e6df8-129">L'interfaccia **IVMHardDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e6df8-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="e6df8-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6df8-130">Property</span></span>                                                              | <span data-ttu-id="e6df8-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e6df8-131">Access type</span></span>           | <span data-ttu-id="e6df8-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6df8-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6df8-133">**File**</span><span class="sxs-lookup"><span data-stu-id="e6df8-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="e6df8-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6df8-134">Read-only</span></span><br/>  | <span data-ttu-id="e6df8-135">Nome del percorso completo del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6df8-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="e6df8-136">**HostFreeDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="e6df8-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="e6df8-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6df8-137">Read-only</span></span><br/>  | <span data-ttu-id="e6df8-138">Quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6df8-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="e6df8-139">**Padre**</span><span class="sxs-lookup"><span data-stu-id="e6df8-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="e6df8-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e6df8-140">Read/write</span></span><br/> | <span data-ttu-id="e6df8-141">Elemento padre del disco rigido virtuale differenze.</span><span class="sxs-lookup"><span data-stu-id="e6df8-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="e6df8-142">**SizeInGuest**</span><span class="sxs-lookup"><span data-stu-id="e6df8-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="e6df8-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6df8-143">Read-only</span></span><br/>  | <span data-ttu-id="e6df8-144">Dimensioni del disco rigido virtuale nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="e6df8-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="e6df8-145">**SizeOnHost**</span><span class="sxs-lookup"><span data-stu-id="e6df8-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="e6df8-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6df8-146">Read-only</span></span><br/>  | <span data-ttu-id="e6df8-147">Dimensioni del file del disco rigido virtuale nel computer host.</span><span class="sxs-lookup"><span data-stu-id="e6df8-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="e6df8-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e6df8-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="e6df8-149">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6df8-149">Read-only</span></span><br/>  | <span data-ttu-id="e6df8-150">Tipo del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6df8-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="e6df8-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6df8-151">Requirements</span></span>



| <span data-ttu-id="e6df8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6df8-152">Requirement</span></span> | <span data-ttu-id="e6df8-153">Valore</span><span class="sxs-lookup"><span data-stu-id="e6df8-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6df8-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6df8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e6df8-155">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6df8-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6df8-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6df8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e6df8-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e6df8-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6df8-158">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e6df8-158">End of client support</span></span><br/>    | <span data-ttu-id="e6df8-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6df8-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6df8-160">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e6df8-160">Product</span></span><br/>                  | <span data-ttu-id="e6df8-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6df8-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6df8-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6df8-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6df8-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6df8-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6df8-164">IID</span><span class="sxs-lookup"><span data-stu-id="e6df8-164">IID</span></span><br/>                      | <span data-ttu-id="e6df8-165">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="e6df8-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

