---
title: Interfaccia IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di dispositivi USB collegati al sistema host. Per ottenere un oggetto IVMUSBDeviceCollection, usare la proprietà IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Interfaccia IVMUSBDeviceCollection Virtual PC
- Interfaccia IVMUSBDeviceCollection Virtual PC, descritta
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
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301562"
---
# <a name="ivmusbdevicecollection-interface"></a>Interfaccia IVMUSBDeviceCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la raccolta di dispositivi USB collegati al sistema host. Per ottenere un oggetto **IVMUSBDeviceCollection** , usare la proprietà [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMUSBDeviceCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDeviceCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMUSBDeviceCollection** ha queste proprietà.



| Proprietà                                                        | Tipo di accesso          | Descrizione                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                        |
| [**Conteggio**](ivmusbdevicecollection-count.md)<br/>        | Sola lettura<br/> | Numero di dispositivi USB in questa raccolta.<br/>                            |
| [**Elemento**](ivmusbdevicecollection-item.md)<br/>          | Sola lettura<br/> | Oggetto dispositivo USB che corrisponde all'indice specificato (in base 1).<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

