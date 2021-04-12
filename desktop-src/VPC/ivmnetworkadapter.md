---
title: Interfaccia IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Funge da interfaccia per una scheda di interfaccia di rete virtuale.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Interfaccia IVMNetworkAdapter Virtual PC
- Interfaccia IVMNetworkAdapter Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400669"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="d203a-105">Interfaccia IVMNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="d203a-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="d203a-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d203a-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d203a-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d203a-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d203a-108">Funge da interfaccia per una scheda di interfaccia di rete virtuale (NIC).</span><span class="sxs-lookup"><span data-stu-id="d203a-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="d203a-109">Viene usato per configurare la modalità di rete di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d203a-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="d203a-110">È possibile aggiungere e rimuovere schede di interfaccia di rete usando [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="d203a-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="d203a-111">È anche possibile recuperare un oggetto **IVMNetworkAdapter** dalla raccolta [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) restituito dalle proprietà [**IVMVirtualMachine:: I NetworkAdapter**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork:: i NetworkAdapter**](ivmvirtualnetwork-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="d203a-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="d203a-112">Membri</span><span class="sxs-lookup"><span data-stu-id="d203a-112">Members</span></span>

<span data-ttu-id="d203a-113">L'interfaccia **IVMNetworkAdapter** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d203a-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d203a-114">**IVMNetworkAdapter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d203a-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="d203a-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="d203a-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="d203a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d203a-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d203a-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="d203a-117">Methods</span></span>

<span data-ttu-id="d203a-118">L'interfaccia **IVMNetworkAdapter** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d203a-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="d203a-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="d203a-119">Method</span></span>                                                                         | <span data-ttu-id="d203a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d203a-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="d203a-121">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="d203a-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="d203a-122">Recupera l'identificatore interno di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d203a-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="d203a-123">**AttachToVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="d203a-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="d203a-124">Connette l'interfaccia di rete alla rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="d203a-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="d203a-125">**DetachFromVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="d203a-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="d203a-126">Scollega l'interfaccia di rete dalla relativa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d203a-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="d203a-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d203a-127">Properties</span></span>

<span data-ttu-id="d203a-128">L'interfaccia **IVMNetworkAdapter** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d203a-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="d203a-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d203a-129">Property</span></span>                                                                                  | <span data-ttu-id="d203a-130">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d203a-130">Access type</span></span>           | <span data-ttu-id="d203a-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d203a-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="d203a-132">**EthernetAddress**</span><span class="sxs-lookup"><span data-stu-id="d203a-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="d203a-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d203a-133">Read/write</span></span><br/> | <span data-ttu-id="d203a-134">Indirizzo Ethernet (MAC) dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d203a-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="d203a-135">**IsEthernetAddressDynamic**</span><span class="sxs-lookup"><span data-stu-id="d203a-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="d203a-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d203a-136">Read/write</span></span><br/> | <span data-ttu-id="d203a-137">Indica se l'indirizzo Ethernet viene generato dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d203a-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="d203a-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d203a-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="d203a-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d203a-139">Read-only</span></span><br/>  | <span data-ttu-id="d203a-140">Macchina virtuale associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d203a-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="d203a-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="d203a-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="d203a-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d203a-142">Read-only</span></span><br/>  | <span data-ttu-id="d203a-143">Rete virtuale a cui è collegata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d203a-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d203a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="d203a-144">Remarks</span></span>

<span data-ttu-id="d203a-145">L'indirizzo Ethernet predefinito per un'interfaccia di rete è "00-00-00-00-00-00", che è considerato un indirizzo Ethernet non valido per la maggior parte dei sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="d203a-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="d203a-146">Se [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) è impostato su **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) deve essere inizializzato con un indirizzo di rete Ethernet valido.</span><span class="sxs-lookup"><span data-stu-id="d203a-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="d203a-147">Nelle procedure riportate di seguito viene illustrato come utilizzare l'interfaccia **IVMNetworkAdapter** .</span><span class="sxs-lookup"><span data-stu-id="d203a-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="d203a-148">**Per alleghi una scheda di interfaccia di rete virtuale a una NIC host**</span><span class="sxs-lookup"><span data-stu-id="d203a-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="d203a-149">Le NIC virtuali (Guest) non sono collegate direttamente a una scheda di interfaccia di rete host.</span><span class="sxs-lookup"><span data-stu-id="d203a-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="d203a-150">La scheda di interfaccia di rete virtuale è invece collegata a una rete virtuale collegata a una scheda di interfaccia di rete host.</span><span class="sxs-lookup"><span data-stu-id="d203a-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="d203a-151">Per ulteriori informazioni sulla configurazione delle reti virtuali, vedere [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="d203a-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="d203a-152">Per alleghi la scheda di interfaccia di rete virtuale a una rete virtuale, usare il metodo [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="d203a-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="d203a-153">**Per disconnettere una scheda di interfaccia di rete virtuale dalla rete virtuale**</span><span class="sxs-lookup"><span data-stu-id="d203a-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="d203a-154">Il metodo [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) scollega la scheda di interfaccia di rete virtuale dalla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d203a-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="d203a-155">Dopo la chiamata a questa funzione, la proprietà [**virtualnetwork**](ivmnetworkadapter-virtualnetwork.md) restituirà un ID di rete virtuale non valido.</span><span class="sxs-lookup"><span data-stu-id="d203a-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="d203a-156">**Per rimuovere una scheda di interfaccia di rete virtuale da una macchina virtuale se si dispone dell'oggetto NIC virtuale**</span><span class="sxs-lookup"><span data-stu-id="d203a-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="d203a-157">Ottenere la macchina virtuale associata alla scheda di interfaccia di rete virtuale usando la proprietà [**virtualmachine**](ivmnetworkadapter-virtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="d203a-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="d203a-158">Usare l'oggetto corrente come parametro per il metodo [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="d203a-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d203a-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d203a-159">Requirements</span></span>



| <span data-ttu-id="d203a-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="d203a-160">Requirement</span></span> | <span data-ttu-id="d203a-161">Valore</span><span class="sxs-lookup"><span data-stu-id="d203a-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d203a-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d203a-162">Minimum supported client</span></span><br/> | <span data-ttu-id="d203a-163">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d203a-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d203a-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d203a-164">Minimum supported server</span></span><br/> | <span data-ttu-id="d203a-165">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d203a-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d203a-166">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d203a-166">End of client support</span></span><br/>    | <span data-ttu-id="d203a-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d203a-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d203a-168">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d203a-168">Product</span></span><br/>                  | <span data-ttu-id="d203a-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d203a-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d203a-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d203a-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="d203a-171"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d203a-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d203a-172">IID</span><span class="sxs-lookup"><span data-stu-id="d203a-172">IID</span></span><br/>                      | <span data-ttu-id="d203a-173">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="d203a-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

