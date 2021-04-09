---
title: Proprietà IVMNetworkAdapter EthernetAddress (VPCCOMInterfaces. h)
description: Indirizzo Ethernet (MAC) dell'interfaccia di rete.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Proprietà EthernetAddress Virtual PC
- Proprietà EthernetAddress Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, proprietà EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739759"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="47fd2-106">Proprietà IVMNetworkAdapter:: EthernetAddress</span><span class="sxs-lookup"><span data-stu-id="47fd2-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="47fd2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="47fd2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="47fd2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="47fd2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="47fd2-109">Recupera e imposta l'indirizzo Ethernet (MAC) dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="47fd2-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="47fd2-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="47fd2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47fd2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47fd2-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="47fd2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="47fd2-112">Property value</span></span>

<span data-ttu-id="47fd2-113">Indirizzo MAC della scheda di interfaccia di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="47fd2-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="47fd2-114">Deve avere il *formato "XX XX XX* XX XX -  -  -  -  - ", dove ogni *X* è una cifra esadecimale.</span><span class="sxs-lookup"><span data-stu-id="47fd2-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47fd2-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="47fd2-115">Error codes</span></span>



| <span data-ttu-id="47fd2-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="47fd2-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="47fd2-117">Significato</span><span class="sxs-lookup"><span data-stu-id="47fd2-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47fd2-118"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="47fd2-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="47fd2-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="47fd2-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="47fd2-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="47fd2-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="47fd2-122"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47fd2-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="47fd2-123">Il formato del parametro non è corretto.</span><span class="sxs-lookup"><span data-stu-id="47fd2-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="47fd2-124"><dt>Macchina virtuale \_ E \_ \_ set di \_ \_ \_ indirizzi MAC dinamici</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="47fd2-125">L'indirizzo Ethernet per un'interfaccia di rete può essere generato in modo dinamico o può essere impostato su un indirizzo statico da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="47fd2-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="47fd2-126">Questo metodo non può essere chiamato quando l'indirizzo è impostato per essere generato in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="47fd2-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="47fd2-127">La proprietà [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) viene usata per modificare il comportamento di generazione dell'indirizzo Ethernet.</span><span class="sxs-lookup"><span data-stu-id="47fd2-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="47fd2-128"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="47fd2-129">La macchina virtuale non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="47fd2-129">The virtual machine was not found.</span></span> <span data-ttu-id="47fd2-130">Questo problema può verificarsi se il computer è stato rimosso dopo la creazione dell'oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="47fd2-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="47fd2-131"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="47fd2-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="47fd2-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="47fd2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47fd2-133">Requirements</span></span>



| <span data-ttu-id="47fd2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="47fd2-134">Requirement</span></span> | <span data-ttu-id="47fd2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="47fd2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="47fd2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47fd2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="47fd2-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="47fd2-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47fd2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47fd2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="47fd2-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="47fd2-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="47fd2-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="47fd2-140">End of client support</span></span><br/>    | <span data-ttu-id="47fd2-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="47fd2-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="47fd2-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="47fd2-142">Product</span></span><br/>                  | <span data-ttu-id="47fd2-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47fd2-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="47fd2-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47fd2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="47fd2-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="47fd2-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="47fd2-146">IID</span><span class="sxs-lookup"><span data-stu-id="47fd2-146">IID</span></span><br/>                      | <span data-ttu-id="47fd2-147">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="47fd2-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="47fd2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47fd2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47fd2-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="47fd2-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

