---
title: Proprietà IVMNetworkAdapter VirtualNetwork (VPCCOMInterfaces. h)
description: Recupera la rete virtuale a cui è collegata l'interfaccia di rete.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- Proprietà VirtualNetwork Virtual PC
- Proprietà VirtualNetwork Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, proprietà VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047802"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="a8e7e-106">Proprietà IVMNetworkAdapter:: VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8e7e-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="a8e7e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a8e7e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a8e7e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a8e7e-109">Recupera la rete virtuale a cui è collegata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="a8e7e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e7e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8e7e-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="a8e7e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a8e7e-112">Property value</span></span>

<span data-ttu-id="a8e7e-113">Interfaccia [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che rappresenta la rete virtuale a cui è collegata l'interfaccia di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8e7e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a8e7e-114">Error codes</span></span>



| <span data-ttu-id="a8e7e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="a8e7e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a8e7e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a8e7e-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8e7e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a8e7e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a8e7e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="a8e7e-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="a8e7e-121"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="a8e7e-122">Questa interfaccia di rete viene scollegata e non è connessa a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="a8e7e-123"><dt>Macchina virtuale \_ E \_ \_ \_ \_ ID rete virtuale non valido</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="a8e7e-124">Questa interfaccia è connessa a una rete virtuale con un ID non valido.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="a8e7e-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a8e7e-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a8e7e-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="a8e7e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8e7e-127">Requirements</span></span>



| <span data-ttu-id="a8e7e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e7e-128">Requirement</span></span> | <span data-ttu-id="a8e7e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a8e7e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e7e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8e7e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e7e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8e7e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8e7e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8e7e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e7e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a8e7e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a8e7e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a8e7e-134">End of client support</span></span><br/>    | <span data-ttu-id="a8e7e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8e7e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a8e7e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a8e7e-136">Product</span></span><br/>                  | <span data-ttu-id="a8e7e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a8e7e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a8e7e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8e7e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e7e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a8e7e-140">IID</span><span class="sxs-lookup"><span data-stu-id="a8e7e-140">IID</span></span><br/>                      | <span data-ttu-id="a8e7e-141">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="a8e7e-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a8e7e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8e7e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e7e-143">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="a8e7e-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

