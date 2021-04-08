---
title: Proprietà IVMUSBDevice DeviceString (VPCCOMInterfaces. h)
description: Recupera il nome del dispositivo USB.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Proprietà DeviceString Virtual PC
- Proprietà DeviceString Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà DeviceString
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873917"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="b7efb-106">IVMUSBDevice::D Proprietà eviceString</span><span class="sxs-lookup"><span data-stu-id="b7efb-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="b7efb-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7efb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7efb-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b7efb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7efb-109">Recupera il nome del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b7efb-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="b7efb-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b7efb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7efb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7efb-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="b7efb-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b7efb-112">Property value</span></span>

<span data-ttu-id="b7efb-113">Nome del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b7efb-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7efb-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b7efb-114">Error codes</span></span>



| <span data-ttu-id="b7efb-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="b7efb-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="b7efb-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b7efb-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="b7efb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7efb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="b7efb-118">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b7efb-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b7efb-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b7efb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="b7efb-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="b7efb-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="b7efb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7efb-121">Requirements</span></span>



| <span data-ttu-id="b7efb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7efb-122">Requirement</span></span> | <span data-ttu-id="b7efb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b7efb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7efb-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7efb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b7efb-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b7efb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7efb-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7efb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b7efb-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b7efb-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7efb-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b7efb-128">End of client support</span></span><br/>    | <span data-ttu-id="b7efb-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7efb-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7efb-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b7efb-130">Product</span></span><br/>                  | <span data-ttu-id="b7efb-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7efb-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7efb-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7efb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7efb-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7efb-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7efb-134">IID</span><span class="sxs-lookup"><span data-stu-id="b7efb-134">IID</span></span><br/>                      | <span data-ttu-id="b7efb-135">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="b7efb-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b7efb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7efb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7efb-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="b7efb-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

