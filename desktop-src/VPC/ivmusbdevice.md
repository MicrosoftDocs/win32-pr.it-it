---
title: Interfaccia IVMUSBDevice (VPCCOMInterfaces. h)
description: Definisce l'interfaccia per un dispositivo USB collegato all'host. È possibile connettere un dispositivo USB a una macchina virtuale per usare il dispositivo all'interno della macchina virtuale.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Interfaccia IVMUSBDevice Virtual PC
- Interfaccia IVMUSBDevice Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301732"
---
# <a name="ivmusbdevice-interface"></a>Interfaccia IVMUSBDevice

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia per un dispositivo USB collegato all'host. È possibile connettere un dispositivo USB a una macchina virtuale per usare il dispositivo all'interno della macchina virtuale.

## <a name="members"></a>Membri

L'interfaccia **IVMUSBDevice** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDevice** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMUSBDevice** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**AttachedToVM**](ivmusbdevice-attachedtovm.md)<br/>             | Sola lettura<br/> | Nome della macchina virtuale a cui è collegato il dispositivo USB.<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | Sola lettura<br/> | Classe dispositivo del dispositivo USB.<br/>                                  |
| [**DeviceString**](ivmusbdevice-devicestring.md)<br/>             | Sola lettura<br/> | Nome del dispositivo USB.<br/>                                          |
| [**HubID**](ivmusbdevice-hubid.md)<br/>                           | Sola lettura<br/> | Identificatore dell'hub a cui è connesso il dispositivo.<br/>          |
| [**ManufacturerString**](ivmusbdevice-manufacturerstring.md)<br/> | Sola lettura<br/> | Nome del produttore del dispositivo USB.<br/>                             |
| [**Porta**](ivmusbdevice-port.md)<br/>                             | Sola lettura<br/> | Identificatore della porta a cui è connesso il dispositivo.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



 

