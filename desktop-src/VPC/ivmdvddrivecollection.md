---
title: Interfaccia IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale. Per ottenere un oggetto IVMDVDDriveCollection, usare la proprietà IVMVirtualMachine DVDROMDrives.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Interfaccia IVMDVDDriveCollection Virtual PC
- Interfaccia IVMDVDDriveCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301849"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="5eb6f-106">Interfaccia IVMDVDDriveCollection</span><span class="sxs-lookup"><span data-stu-id="5eb6f-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="5eb6f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5eb6f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5eb6f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5eb6f-109">Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="5eb6f-110">Per ottenere un oggetto **IVMDVDDriveCollection** , usare la proprietà [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb6f-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="5eb6f-111">Membri</span><span class="sxs-lookup"><span data-stu-id="5eb6f-111">Members</span></span>

<span data-ttu-id="5eb6f-112">L'interfaccia **IVMDVDDriveCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5eb6f-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5eb6f-113">**IVMDVDDriveCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5eb6f-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="5eb6f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb6f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5eb6f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb6f-115">Properties</span></span>

<span data-ttu-id="5eb6f-116">L'interfaccia **IVMDVDDriveCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="5eb6f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb6f-117">Property</span></span>                                                       | <span data-ttu-id="5eb6f-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="5eb6f-118">Access type</span></span>          | <span data-ttu-id="5eb6f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb6f-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb6f-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5eb6f-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="5eb6f-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb6f-121">Read-only</span></span><br/> | <span data-ttu-id="5eb6f-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="5eb6f-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="5eb6f-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="5eb6f-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb6f-124">Read-only</span></span><br/> | <span data-ttu-id="5eb6f-125">Numero di unità CD e DVD in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="5eb6f-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5eb6f-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="5eb6f-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb6f-127">Read-only</span></span><br/> | <span data-ttu-id="5eb6f-128">Oggetto unità CD o DVD corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="5eb6f-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5eb6f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eb6f-129">Requirements</span></span>



| <span data-ttu-id="5eb6f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb6f-130">Requirement</span></span> | <span data-ttu-id="5eb6f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5eb6f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb6f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb6f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb6f-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5eb6f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5eb6f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb6f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb6f-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5eb6f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5eb6f-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5eb6f-136">End of client support</span></span><br/>    | <span data-ttu-id="5eb6f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5eb6f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5eb6f-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5eb6f-138">Product</span></span><br/>                  | <span data-ttu-id="5eb6f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5eb6f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5eb6f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5eb6f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb6f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb6f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5eb6f-142">IID</span><span class="sxs-lookup"><span data-stu-id="5eb6f-142">IID</span></span><br/>                      | <span data-ttu-id="5eb6f-143">IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="5eb6f-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="5eb6f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eb6f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb6f-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="5eb6f-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="5eb6f-146">**IVMVirtualMachine::D VDROMDrives**</span><span class="sxs-lookup"><span data-stu-id="5eb6f-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

