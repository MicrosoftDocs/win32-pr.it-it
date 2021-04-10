---
title: Enumerazione VMUSBDeviceClassEnum (VPCCOMInterfaces. h)
description: Specifica la classe del dispositivo USB.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- VMUSBDeviceClassEnum enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120586"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="31795-104">Enumerazione VMUSBDeviceClassEnum</span><span class="sxs-lookup"><span data-stu-id="31795-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="31795-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="31795-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31795-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="31795-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31795-107">Specifica la classe del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="31795-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="31795-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31795-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="31795-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="31795-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31795-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**\_InterfaceDescriptor vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="31795-111">Un dispositivo non identificato.</span><span class="sxs-lookup"><span data-stu-id="31795-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**\_audio vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="31795-113">Dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="31795-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**\_comunicazione vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="31795-115">Dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="31795-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass \_ HID**</span><span class="sxs-lookup"><span data-stu-id="31795-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="31795-117">Dispositivo HID.</span><span class="sxs-lookup"><span data-stu-id="31795-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass \_ fisico**</span><span class="sxs-lookup"><span data-stu-id="31795-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="31795-119">Dispositivo sensoriale fisico.</span><span class="sxs-lookup"><span data-stu-id="31795-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**immagine di vmUSBDeviceClass \_**</span><span class="sxs-lookup"><span data-stu-id="31795-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="31795-121">Scansione o dispositivo di imaging.</span><span class="sxs-lookup"><span data-stu-id="31795-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**\_stampante vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="31795-123">Dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="31795-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**\_MassStorage vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="31795-125">Dispositivo di archiviazione di massa.</span><span class="sxs-lookup"><span data-stu-id="31795-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**\_Hub vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="31795-127">Dispositivo hub.</span><span class="sxs-lookup"><span data-stu-id="31795-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**\_CDCData vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="31795-129">Dispositivo dati CDC.</span><span class="sxs-lookup"><span data-stu-id="31795-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**\_Smart Card vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="31795-131">Dispositivo smart card.</span><span class="sxs-lookup"><span data-stu-id="31795-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**\_ContentSecurity vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="31795-133">Dispositivo di sicurezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="31795-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**Video di vmUSBDeviceClass \_**</span><span class="sxs-lookup"><span data-stu-id="31795-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="31795-135">Dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="31795-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**\_PersonalHealthcare vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="31795-137">Dispositivo Health Care.</span><span class="sxs-lookup"><span data-stu-id="31795-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**\_DiagnosticDevice vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="31795-139">Dispositivo di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="31795-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**\_WirelessController vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="31795-141">Dispositivo wireless.</span><span class="sxs-lookup"><span data-stu-id="31795-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass \_ varie**</span><span class="sxs-lookup"><span data-stu-id="31795-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="31795-143">Dispositivo vario.</span><span class="sxs-lookup"><span data-stu-id="31795-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**\_ApplicationSpecific vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="31795-145">Dispositivo specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31795-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="31795-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**\_VendorSpecific vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="31795-147">Dispositivo specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="31795-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31795-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31795-148">Requirements</span></span>



| <span data-ttu-id="31795-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="31795-149">Requirement</span></span> | <span data-ttu-id="31795-150">Valore</span><span class="sxs-lookup"><span data-stu-id="31795-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31795-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31795-151">Minimum supported client</span></span><br/> | <span data-ttu-id="31795-152">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31795-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31795-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31795-153">Minimum supported server</span></span><br/> | <span data-ttu-id="31795-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="31795-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31795-155">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="31795-155">End of client support</span></span><br/>    | <span data-ttu-id="31795-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31795-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31795-157">Prodotto</span><span class="sxs-lookup"><span data-stu-id="31795-157">Product</span></span><br/>                  | <span data-ttu-id="31795-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31795-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31795-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31795-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="31795-160"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="31795-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31795-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31795-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31795-162">**IVMUSBDevice::D eviceClass**</span><span class="sxs-lookup"><span data-stu-id="31795-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

