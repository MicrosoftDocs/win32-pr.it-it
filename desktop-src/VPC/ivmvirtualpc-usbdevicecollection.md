---
title: Proprietà IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces. h)
description: Raccolta enumerabile di tutti i dispositivi USB connessi all'host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Proprietà USBDeviceCollection Virtual PC
- Proprietà USBDeviceCollection Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742039"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="69f0e-106">Proprietà IVMVirtualPC:: USBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="69f0e-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="69f0e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="69f0e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69f0e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69f0e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69f0e-109">Recupera una raccolta enumerabile di tutti i dispositivi USB connessi all'host.</span><span class="sxs-lookup"><span data-stu-id="69f0e-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="69f0e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="69f0e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f0e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69f0e-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="69f0e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="69f0e-112">Property value</span></span>

<span data-ttu-id="69f0e-113">Riferimento a un puntatore [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) che rappresenta una raccolta di oggetti [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="69f0e-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69f0e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="69f0e-114">Error codes</span></span>



| <span data-ttu-id="69f0e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="69f0e-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="69f0e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="69f0e-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69f0e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="69f0e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="69f0e-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="69f0e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="69f0e-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="69f0e-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="69f0e-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="69f0e-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="69f0e-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="69f0e-123"><dt>Macchina virtuale \_ L' \_ enumerazione USB di E \_ \_ non ha superato \_ più \_ dispositivi</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="69f0e-124">Più di 16 dispositivi USB sono connessi all'host.</span><span class="sxs-lookup"><span data-stu-id="69f0e-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="69f0e-125"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="69f0e-126">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="69f0e-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69f0e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69f0e-127">Requirements</span></span>



| <span data-ttu-id="69f0e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f0e-128">Requirement</span></span> | <span data-ttu-id="69f0e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="69f0e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f0e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69f0e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69f0e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="69f0e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69f0e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69f0e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69f0e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69f0e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69f0e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="69f0e-134">End of client support</span></span><br/>    | <span data-ttu-id="69f0e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69f0e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69f0e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="69f0e-136">Product</span></span><br/>                  | <span data-ttu-id="69f0e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69f0e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69f0e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69f0e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="69f0e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f0e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69f0e-140">IID</span><span class="sxs-lookup"><span data-stu-id="69f0e-140">IID</span></span><br/>                      | <span data-ttu-id="69f0e-141">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="69f0e-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="69f0e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69f0e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f0e-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="69f0e-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

