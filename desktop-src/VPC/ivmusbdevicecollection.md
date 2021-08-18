---
title: Interfaccia IVMUSBDeviceCollection (VPCCOMInterfaces.h)
description: Definisce la raccolta di dispositivi USB collegati al sistema host. Per ottenere un oggetto IVMUSBDeviceCollection, usare la proprietà IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Interfaccia IVMUSBDeviceCollection Virtual PC
- INTERFACCIA IVMUSBDeviceCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752540"
---
# <a name="ivmusbdevicecollection-interface"></a>Interfaccia IVMUSBDeviceCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce la raccolta di dispositivi USB collegati al sistema host. Per ottenere un **oggetto IVMUSBDeviceCollection,** usare la [**proprietà IVMVirtualPC::USBDeviceCollection.**](ivmvirtualpc-usbdevicecollection.md)

## <a name="members"></a>Membri

**L'interfaccia IVMUSBDeviceCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMUSBDeviceCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IVMUSBDeviceCollection** ha queste proprietà.



| Proprietà                                                        | Tipo di accesso          | Descrizione                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                        |
| [**Conteggio**](ivmusbdevicecollection-count.md)<br/>        | Sola lettura<br/> | Numero di dispositivi USB in questa raccolta.<br/>                            |
| [**Elemento**](ivmusbdevicecollection-item.md)<br/>          | Sola lettura<br/> | Oggetto dispositivo USB che corrisponde all'indice specificato (in base 1).<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

