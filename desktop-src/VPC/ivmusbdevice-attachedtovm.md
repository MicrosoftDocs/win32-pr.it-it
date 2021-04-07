---
title: Proprietà IVMUSBDevice AttachedToVM (VPCCOMInterfaces. h)
description: Recupera il nome della macchina virtuale a cui è collegato il dispositivo USB.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Proprietà AttachedToVM Virtual PC
- Proprietà AttachedToVM Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048432"
---
# <a name="ivmusbdeviceattachedtovm-property"></a><span data-ttu-id="b92c0-106">Proprietà IVMUSBDevice:: AttachedToVM</span><span class="sxs-lookup"><span data-stu-id="b92c0-106">IVMUSBDevice::AttachedToVM property</span></span>

<span data-ttu-id="b92c0-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b92c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b92c0-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b92c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b92c0-109">Recupera il nome della macchina virtuale a cui è collegato il dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b92c0-109">Retrieves the name of the virtual machine to which the USB Device is attached.</span></span>

<span data-ttu-id="b92c0-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b92c0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b92c0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b92c0-111">Syntax</span></span>


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a><span data-ttu-id="b92c0-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b92c0-112">Property value</span></span>

<span data-ttu-id="b92c0-113">Nome della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="b92c0-113">The name of the virtual machine (VM).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b92c0-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b92c0-114">Error codes</span></span>



| <span data-ttu-id="b92c0-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="b92c0-115">Name/value</span></span>                                                                                                                                                           | <span data-ttu-id="b92c0-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b92c0-116">Meaning</span></span>                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b92c0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b92c0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="b92c0-118">Il dispositivo viene collegato alla macchina virtuale e viene restituito il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="b92c0-118">The device is attached to the VM, and its name is returned.</span></span><br/> |
| <dl> <span data-ttu-id="b92c0-119"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b92c0-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                           | <span data-ttu-id="b92c0-120">Il dispositivo è collegato all'host.</span><span class="sxs-lookup"><span data-stu-id="b92c0-120">The device is attached to the host.</span></span><br/>                         |
| <dl> <span data-ttu-id="b92c0-121"><dt>Macchina virtuale \_ 0xA00400929 \_ \_ \_ VM External USB E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b92c0-121"><dt>VM\_E\_USB\_EXTERNAL\_VM</dt> <dt>0xA00400929</dt></span></span> </dl> | <span data-ttu-id="b92c0-122">Il dispositivo è collegato a una macchina virtuale in un'altra sessione utente.</span><span class="sxs-lookup"><span data-stu-id="b92c0-122">The device is attached to a VM in another user session.</span></span><br/>     |
| <dl> <span data-ttu-id="b92c0-123"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b92c0-123"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="b92c0-124">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="b92c0-124">The parameter is **NULL**.</span></span><br/>                                  |



## <a name="requirements"></a><span data-ttu-id="b92c0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b92c0-125">Requirements</span></span>



| <span data-ttu-id="b92c0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92c0-126">Requirement</span></span> | <span data-ttu-id="b92c0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b92c0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92c0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b92c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b92c0-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b92c0-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b92c0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b92c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b92c0-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b92c0-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b92c0-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b92c0-132">End of client support</span></span><br/>    | <span data-ttu-id="b92c0-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b92c0-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b92c0-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b92c0-134">Product</span></span><br/>                  | <span data-ttu-id="b92c0-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b92c0-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b92c0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b92c0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b92c0-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b92c0-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b92c0-138">IID</span><span class="sxs-lookup"><span data-stu-id="b92c0-138">IID</span></span><br/>                      | <span data-ttu-id="b92c0-139">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="b92c0-139">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b92c0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b92c0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92c0-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="b92c0-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

