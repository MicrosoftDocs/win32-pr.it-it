---
title: Proprietà IVMUSBDevice DeviceClass (VPCCOMInterfaces. h)
description: Recupera la classe dispositivo del dispositivo USB.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Proprietà DeviceClass Virtual PC
- Proprietà DeviceClass Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà DeviceClass
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400815"
---
# <a name="ivmusbdevicedeviceclass-property"></a><span data-ttu-id="44a85-106">IVMUSBDevice::D Proprietà eviceClass</span><span class="sxs-lookup"><span data-stu-id="44a85-106">IVMUSBDevice::DeviceClass property</span></span>

<span data-ttu-id="44a85-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="44a85-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="44a85-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="44a85-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="44a85-109">Recupera la classe dispositivo del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="44a85-109">Retrieves the device class of the USB device.</span></span>

<span data-ttu-id="44a85-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="44a85-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a85-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44a85-111">Syntax</span></span>


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a><span data-ttu-id="44a85-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="44a85-112">Property value</span></span>

<span data-ttu-id="44a85-113">Classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44a85-113">The device class.</span></span> <span data-ttu-id="44a85-114">Per un elenco di valori, vedere [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span><span class="sxs-lookup"><span data-stu-id="44a85-114">For a list of values, see [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="44a85-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="44a85-115">Error codes</span></span>



| <span data-ttu-id="44a85-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="44a85-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="44a85-117">Significato</span><span class="sxs-lookup"><span data-stu-id="44a85-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="44a85-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="44a85-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="44a85-119">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="44a85-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="44a85-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="44a85-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="44a85-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="44a85-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="44a85-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44a85-122">Requirements</span></span>



| <span data-ttu-id="44a85-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a85-123">Requirement</span></span> | <span data-ttu-id="44a85-124">Valore</span><span class="sxs-lookup"><span data-stu-id="44a85-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a85-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44a85-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44a85-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="44a85-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44a85-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44a85-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44a85-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="44a85-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="44a85-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="44a85-129">End of client support</span></span><br/>    | <span data-ttu-id="44a85-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44a85-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="44a85-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="44a85-131">Product</span></span><br/>                  | <span data-ttu-id="44a85-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="44a85-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="44a85-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44a85-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a85-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="44a85-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="44a85-135">IID</span><span class="sxs-lookup"><span data-stu-id="44a85-135">IID</span></span><br/>                      | <span data-ttu-id="44a85-136">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="44a85-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="44a85-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44a85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a85-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="44a85-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

