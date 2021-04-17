---
title: Interfaccia IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Definisce una raccolta di unità floppy all'interno della macchina virtuale.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Interfaccia IVMFloppyDriveCollection Virtual PC
- Interfaccia IVMFloppyDriveCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400914"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="15392-105">Interfaccia IVMFloppyDriveCollection</span><span class="sxs-lookup"><span data-stu-id="15392-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="15392-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="15392-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="15392-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="15392-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="15392-108">Definisce una raccolta di unità floppy all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="15392-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="15392-109">Per ottenere un oggetto **IVMFloppyDriveCollection** , usare la proprietà [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="15392-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="15392-110">Membri</span><span class="sxs-lookup"><span data-stu-id="15392-110">Members</span></span>

<span data-ttu-id="15392-111">L'interfaccia **IVMFloppyDriveCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="15392-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="15392-112">**IVMFloppyDriveCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="15392-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="15392-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15392-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15392-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15392-114">Properties</span></span>

<span data-ttu-id="15392-115">L'interfaccia **IVMFloppyDriveCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="15392-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="15392-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15392-116">Property</span></span>                                                          | <span data-ttu-id="15392-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="15392-117">Access type</span></span>          | <span data-ttu-id="15392-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15392-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="15392-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="15392-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="15392-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="15392-120">Read-only</span></span><br/> | <span data-ttu-id="15392-121">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="15392-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="15392-122">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="15392-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="15392-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="15392-123">Read-only</span></span><br/> | <span data-ttu-id="15392-124">Numero di unità floppy in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="15392-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="15392-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="15392-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="15392-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="15392-126">Read-only</span></span><br/> | <span data-ttu-id="15392-127">Oggetto unità floppy che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="15392-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15392-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15392-128">Requirements</span></span>



| <span data-ttu-id="15392-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="15392-129">Requirement</span></span> | <span data-ttu-id="15392-130">Valore</span><span class="sxs-lookup"><span data-stu-id="15392-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15392-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15392-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15392-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="15392-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15392-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15392-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15392-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="15392-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="15392-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="15392-135">End of client support</span></span><br/>    | <span data-ttu-id="15392-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15392-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="15392-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="15392-137">Product</span></span><br/>                  | <span data-ttu-id="15392-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="15392-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="15392-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15392-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="15392-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="15392-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="15392-141">IID</span><span class="sxs-lookup"><span data-stu-id="15392-141">IID</span></span><br/>                      | <span data-ttu-id="15392-142">IID \_ IVMFloppyDriveCollection è definito come 8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="15392-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="15392-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15392-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15392-144">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="15392-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="15392-145">**IVMVirtualMachine::FloppyDrives**</span><span class="sxs-lookup"><span data-stu-id="15392-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

