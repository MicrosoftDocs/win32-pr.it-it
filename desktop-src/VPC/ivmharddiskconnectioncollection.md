---
title: Interfaccia IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di connessioni del disco rigido all'interno della macchina virtuale. Per ottenere un oggetto IVMHardDiskConnectionCollection, usare la proprietà IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Interfaccia IVMHardDiskConnectionCollection Virtual PC
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475034"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="43c91-106">Interfaccia IVMHardDiskConnectionCollection</span><span class="sxs-lookup"><span data-stu-id="43c91-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="43c91-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="43c91-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43c91-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="43c91-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43c91-109">Definisce la raccolta di connessioni del disco rigido all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c91-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="43c91-110">Per ottenere un oggetto **IVMHardDiskConnectionCollection** , usare la proprietà [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="43c91-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="43c91-111">Membri</span><span class="sxs-lookup"><span data-stu-id="43c91-111">Members</span></span>

<span data-ttu-id="43c91-112">L'interfaccia **IVMHardDiskConnectionCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="43c91-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="43c91-113">**IVMHardDiskConnectionCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43c91-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="43c91-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43c91-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43c91-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43c91-115">Properties</span></span>

<span data-ttu-id="43c91-116">L'interfaccia **IVMHardDiskConnectionCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43c91-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="43c91-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43c91-117">Property</span></span>                                                                 | <span data-ttu-id="43c91-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="43c91-118">Access type</span></span>          | <span data-ttu-id="43c91-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43c91-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="43c91-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="43c91-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="43c91-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43c91-121">Read-only</span></span><br/> | <span data-ttu-id="43c91-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="43c91-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="43c91-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="43c91-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="43c91-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43c91-124">Read-only</span></span><br/> | <span data-ttu-id="43c91-125">Numero di connessioni del disco rigido in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="43c91-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="43c91-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43c91-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="43c91-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43c91-127">Read-only</span></span><br/> | <span data-ttu-id="43c91-128">Oggetto connessione al disco rigido che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="43c91-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43c91-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43c91-129">Requirements</span></span>



| <span data-ttu-id="43c91-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c91-130">Requirement</span></span> | <span data-ttu-id="43c91-131">Valore</span><span class="sxs-lookup"><span data-stu-id="43c91-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c91-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43c91-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43c91-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="43c91-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="43c91-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43c91-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43c91-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="43c91-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="43c91-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="43c91-136">End of client support</span></span><br/>    | <span data-ttu-id="43c91-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43c91-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="43c91-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="43c91-138">Product</span></span><br/>                  | <span data-ttu-id="43c91-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43c91-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="43c91-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43c91-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c91-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c91-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="43c91-142">IID</span><span class="sxs-lookup"><span data-stu-id="43c91-142">IID</span></span><br/>                      | <span data-ttu-id="43c91-143">IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="43c91-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43c91-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43c91-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c91-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="43c91-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="43c91-146">**IVMVirtualMachine::HardDiskConnections**</span><span class="sxs-lookup"><span data-stu-id="43c91-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

