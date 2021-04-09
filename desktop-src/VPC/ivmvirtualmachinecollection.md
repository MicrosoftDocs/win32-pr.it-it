---
title: Interfaccia IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di macchine virtuali all'interno di Windows Virtual PC. Per ottenere un oggetto IVMVirtualMachineCollection, usare la proprietà IVMVirtualPC VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Interfaccia IVMVirtualMachineCollection Virtual PC
- Interfaccia IVMVirtualMachineCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121082"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="8e9a8-106">Interfaccia IVMVirtualMachineCollection</span><span class="sxs-lookup"><span data-stu-id="8e9a8-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="8e9a8-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e9a8-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e9a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e9a8-109">Definisce la raccolta di macchine virtuali all'interno di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="8e9a8-110">Per ottenere un oggetto **IVMVirtualMachineCollection** , usare la proprietà [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .</span><span class="sxs-lookup"><span data-stu-id="8e9a8-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8e9a8-111">Membri</span><span class="sxs-lookup"><span data-stu-id="8e9a8-111">Members</span></span>

<span data-ttu-id="8e9a8-112">L'interfaccia **IVMVirtualMachineCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8e9a8-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8e9a8-113">**IVMVirtualMachineCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8e9a8-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8e9a8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e9a8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e9a8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e9a8-115">Properties</span></span>

<span data-ttu-id="8e9a8-116">L'interfaccia **IVMVirtualMachineCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="8e9a8-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e9a8-117">Property</span></span>                                                             | <span data-ttu-id="8e9a8-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="8e9a8-118">Access type</span></span>          | <span data-ttu-id="8e9a8-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e9a8-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8e9a8-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8e9a8-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="8e9a8-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e9a8-121">Read-only</span></span><br/> | <span data-ttu-id="8e9a8-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="8e9a8-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="8e9a8-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="8e9a8-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e9a8-124">Read-only</span></span><br/> | <span data-ttu-id="8e9a8-125">Numero di macchine virtuali in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="8e9a8-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e9a8-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="8e9a8-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e9a8-127">Read-only</span></span><br/> | <span data-ttu-id="8e9a8-128">Oggetto macchina virtuale che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="8e9a8-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8e9a8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e9a8-129">Requirements</span></span>



| <span data-ttu-id="8e9a8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e9a8-130">Requirement</span></span> | <span data-ttu-id="8e9a8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8e9a8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9a8-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e9a8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8e9a8-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e9a8-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e9a8-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e9a8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8e9a8-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8e9a8-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8e9a8-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8e9a8-136">End of client support</span></span><br/>    | <span data-ttu-id="8e9a8-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e9a8-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="8e9a8-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8e9a8-138">Product</span></span><br/>                  | <span data-ttu-id="8e9a8-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e9a8-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="8e9a8-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e9a8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e9a8-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e9a8-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="8e9a8-142">IID</span><span class="sxs-lookup"><span data-stu-id="8e9a8-142">IID</span></span><br/>                      | <span data-ttu-id="8e9a8-143">IID \_ IVMVirtualMachineCollection è definito come 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="8e9a8-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e9a8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e9a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9a8-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8e9a8-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="8e9a8-146">**IVMVirtualPC:: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="8e9a8-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

