---
title: Enumerazione VMUSBDeviceClassEnum (VPCCOMInterfaces.h)
description: Specifica la classe di dispositivo USB.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- VMUSBDeviceClassEnum enumeration Virtual PC
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
ms.openlocfilehash: 75fa711718ecb37a89bd1c209131b2c18d1c25ca8aef91f4d0fb218f44b80c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866551"
---
# <a name="vmusbdeviceclassenum-enumeration"></a>Enumerazione VMUSBDeviceClassEnum

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica la classe di dispositivo USB.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**InterfaceDescriptor vmUSBDeviceClass \_**
</dt> <dd>

Un dispositivo non identificato.

</dd> <dt>

<span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass \_ Audio**
</dt> <dd>

Dispositivo audio.

</dd> <dt>

<span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**Comunicazione vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo di comunicazione.

</dd> <dt>

<span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**VMUSBDeviceClass \_ HID**
</dt> <dd>

Dispositivo HID.

</dd> <dt>

<span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass \_ Physical**
</dt> <dd>

Dispositivo sensoriale fisico.

</dd> <dt>

<span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**Immagine vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo di digitalizzazione o creazione di immagini.

</dd> <dt>

<span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**Stampante vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo della stampante.

</dd> <dt>

<span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass \_ MassStorage**
</dt> <dd>

Dispositivo di archiviazione di massa.

</dd> <dt>

<span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**Hub vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo hub.

</dd> <dt>

<span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass \_ CDCData**
</dt> <dd>

Dispositivo dati CDC.

</dd> <dt>

<span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**Smart Card vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo smart card.

</dd> <dt>

<span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**VmUSBDeviceClass \_ ContentSecurity**
</dt> <dd>

Dispositivo di sicurezza dei contenuti.

</dd> <dt>

<span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**Video vmUSBDeviceClass \_**
</dt> <dd>

Dispositivo video.

</dd> <dt>

<span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass \_ PersonalHealthcare**
</dt> <dd>

Dispositivo di assistenza sanitaria.

</dd> <dt>

<span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass \_ DiagnosticDevice**
</dt> <dd>

Dispositivo di diagnostica.

</dd> <dt>

<span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass \_ WirelessController**
</dt> <dd>

Dispositivo wireless.

</dd> <dt>

<span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**VmUSBDeviceClass \_ Varie**
</dt> <dd>

Dispositivo vario.

</dd> <dt>

<span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**VmUSBDeviceClass \_ ApplicationSpecific**
</dt> <dd>

Dispositivo specifico dell'applicazione.

</dd> <dt>

<span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass \_ VendorSpecific**
</dt> <dd>

Dispositivo specifico del fornitore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice::D eviceClass**](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

