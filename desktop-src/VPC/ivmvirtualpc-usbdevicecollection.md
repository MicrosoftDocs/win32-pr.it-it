---
title: Proprietà IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces.h)
description: Raccolta enumerabile di tutti i dispositivi USB connessi all'host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Proprietà USBDeviceCollection Virtual PC
- Proprietà USBDeviceCollection Virtual PC , interfaccia IVMVirtualPC
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
ms.openlocfilehash: 2880a6f7adb60605e37fe78481613016d17fdbbd2e27f1a6add4ce031030deea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136524"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>Proprietà IVMVirtualPC::USBDeviceCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una raccolta enumerabile di tutti i dispositivi USB connessi all'host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Valore proprietà

Riferimento a un [**puntatore IVMUSBDeviceCollection**](ivmusbdevicecollection.md) che rappresenta una raccolta di [**oggetti IVMUSBDevice.**](ivmusbdevice.md)

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                                | Significato                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                     | Il parametro è **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                             | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>Macchina virtuale \_ E \_ USB ENUMERATION FAILED MORE DEVICES \_ \_ \_ \_ 0XA0040930</dt> <dt></dt> </dl> | All'host sono connessi più di 16 dispositivi USB.<br/>                                  |
| <dl> <dt>Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA</dt> <dt>0xA0040951</dt> </dl>      | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

