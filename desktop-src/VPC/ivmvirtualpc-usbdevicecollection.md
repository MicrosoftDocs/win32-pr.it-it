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
# <a name="ivmvirtualpcusbdevicecollection-property"></a>Proprietà IVMVirtualPC:: USBDeviceCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una raccolta enumerabile di tutti i dispositivi USB connessi all'host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Valore proprietà

Riferimento a un puntatore [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) che rappresenta una raccolta di oggetti [**IVMUSBDevice**](ivmusbdevice.md) .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                                | Significato                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                     | Il parametro è **null**.<br/>                                                           |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                             | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>Macchina virtuale \_ L' \_ enumerazione USB di E \_ \_ non ha superato \_ più \_ dispositivi</dt> <dt>0xA0040930</dt> </dl> | Più di 16 dispositivi USB sono connessi all'host.<br/>                                  |
| <dl> <dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt> </dl>      | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

