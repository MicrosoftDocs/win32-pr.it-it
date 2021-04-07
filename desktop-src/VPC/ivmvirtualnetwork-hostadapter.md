---
title: Proprietà IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nome dell'adapter a cui è connessa la rete virtuale.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Proprietà HostAdapter Virtual PC
- Proprietà HostAdapter Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, proprietà HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048621"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="02204-106">Proprietà IVMVirtualNetwork:: HostAdapter</span><span class="sxs-lookup"><span data-stu-id="02204-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="02204-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02204-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02204-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02204-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02204-109">Recupera il nome dell'adapter a cui è connessa la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="02204-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="02204-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="02204-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02204-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02204-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="02204-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="02204-112">Property value</span></span>

<span data-ttu-id="02204-113">Nome della scheda host a cui è connessa la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="02204-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02204-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="02204-114">Error codes</span></span>



| <span data-ttu-id="02204-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="02204-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="02204-116">Significato</span><span class="sxs-lookup"><span data-stu-id="02204-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02204-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02204-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="02204-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="02204-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="02204-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="02204-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="02204-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="02204-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="02204-121"><dt>Macchina virtuale \_ L' \_ adapter \_ E \_ non</dt> è stato trovato <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="02204-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="02204-122">La scheda Ethernet host a cui è connessa la rete virtuale non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="02204-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="02204-123">La scheda Ethernet host potrebbe essere stata rimossa o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="02204-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="02204-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02204-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="02204-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="02204-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="02204-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="02204-126">Remarks</span></span>

<span data-ttu-id="02204-127">La scheda di rete virtuale consente a una rete virtuale di comunicare con reti esterne.</span><span class="sxs-lookup"><span data-stu-id="02204-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="02204-128">In genere, una scheda per ogni scheda Ethernet è installata nel computer host.</span><span class="sxs-lookup"><span data-stu-id="02204-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="02204-129">Supponiamo, ad esempio, che un computer host disponga di un adattatore con etichetta "10/100 ENET".</span><span class="sxs-lookup"><span data-stu-id="02204-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="02204-130">Per connettere una scheda di interfaccia di rete virtuale alla rete collegata a "10/100 ENET", impostare la proprietà Network **hostadapter** della rete virtuale su "10/100 ENET" e connettere la scheda di interfaccia di rete virtuale a questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="02204-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="02204-131">Se la proprietà **hostadapter** è impostata su una stringa vuota (""), la scheda NIC virtuale è connessa alla rete "rete interna" o "rete di rete condivisa (NAT)".</span><span class="sxs-lookup"><span data-stu-id="02204-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="02204-132">Le schede di rete virtuali collegate alla rete "rete interna" non avranno accesso alle reti esterne nell'host di sistema.</span><span class="sxs-lookup"><span data-stu-id="02204-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="02204-133">Tuttavia, le schede di rete virtuali collegate a questa rete virtuale sono ancora in grado di comunicare tra loro.</span><span class="sxs-lookup"><span data-stu-id="02204-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="02204-134">È possibile accedere all'elenco completo degli adapter tramite la proprietà [**IVMHostInfo:: i NetworkAdapter**](ivmhostinfo-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="02204-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="02204-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02204-135">Requirements</span></span>



| <span data-ttu-id="02204-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="02204-136">Requirement</span></span> | <span data-ttu-id="02204-137">Valore</span><span class="sxs-lookup"><span data-stu-id="02204-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02204-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02204-138">Minimum supported client</span></span><br/> | <span data-ttu-id="02204-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02204-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02204-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02204-140">Minimum supported server</span></span><br/> | <span data-ttu-id="02204-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02204-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02204-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="02204-142">End of client support</span></span><br/>    | <span data-ttu-id="02204-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02204-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02204-144">Prodotto</span><span class="sxs-lookup"><span data-stu-id="02204-144">Product</span></span><br/>                  | <span data-ttu-id="02204-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02204-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02204-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02204-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="02204-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02204-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02204-148">IID</span><span class="sxs-lookup"><span data-stu-id="02204-148">IID</span></span><br/>                      | <span data-ttu-id="02204-149">IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="02204-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="02204-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02204-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02204-151">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="02204-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

