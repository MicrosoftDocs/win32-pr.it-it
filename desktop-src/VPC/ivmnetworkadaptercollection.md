---
title: Interfaccia IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Definisce una raccolta di schede di interfaccia di rete virtuale. Per ottenere un oggetto IVMNetworkAdapterCollection, usare le proprietà IVMVirtualMachine I NetworkAdapter, IVMVirtualNetwork I NetworkAdapter e IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Interfaccia IVMNetworkAdapterCollection Virtual PC
- Interfaccia IVMNetworkAdapterCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048462"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="ca552-106">Interfaccia IVMNetworkAdapterCollection</span><span class="sxs-lookup"><span data-stu-id="ca552-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="ca552-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca552-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ca552-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ca552-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ca552-109">Definisce una raccolta di schede di interfaccia di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca552-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="ca552-110">Per ottenere un oggetto IVMNetworkAdapterCollection, usare le proprietà [**IVMVirtualMachine:: i NetworkAdapter**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: i NetworkAdapter**](ivmvirtualnetwork-networkadapters.md)e [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="ca552-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="ca552-111">Membri</span><span class="sxs-lookup"><span data-stu-id="ca552-111">Members</span></span>

<span data-ttu-id="ca552-112">L'interfaccia **IVMNetworkAdapterCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ca552-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ca552-113">**IVMNetworkAdapterCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca552-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="ca552-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca552-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca552-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca552-115">Properties</span></span>

<span data-ttu-id="ca552-116">L'interfaccia **IVMNetworkAdapterCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca552-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="ca552-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca552-117">Property</span></span>                                                             | <span data-ttu-id="ca552-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ca552-118">Access type</span></span>          | <span data-ttu-id="ca552-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca552-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca552-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="ca552-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="ca552-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca552-121">Read-only</span></span><br/> | <span data-ttu-id="ca552-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="ca552-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="ca552-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="ca552-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="ca552-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca552-124">Read-only</span></span><br/> | <span data-ttu-id="ca552-125">Numero di interfacce di rete in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="ca552-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="ca552-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ca552-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="ca552-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca552-127">Read-only</span></span><br/> | <span data-ttu-id="ca552-128">Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="ca552-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca552-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca552-129">Requirements</span></span>



| <span data-ttu-id="ca552-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca552-130">Requirement</span></span> | <span data-ttu-id="ca552-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ca552-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca552-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca552-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ca552-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ca552-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca552-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca552-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ca552-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ca552-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca552-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ca552-136">End of client support</span></span><br/>    | <span data-ttu-id="ca552-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca552-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="ca552-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ca552-138">Product</span></span><br/>                  | <span data-ttu-id="ca552-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ca552-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="ca552-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca552-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca552-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca552-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="ca552-142">IID</span><span class="sxs-lookup"><span data-stu-id="ca552-142">IID</span></span><br/>                      | <span data-ttu-id="ca552-143">IID \_ IVMNetworkAdapterCollection è definito come ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="ca552-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca552-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca552-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca552-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="ca552-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="ca552-146">**IVMVirtualMachine:: I NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="ca552-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="ca552-147">**IVMVirtualNetwork:: I NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="ca552-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="ca552-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="ca552-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

