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
# <a name="ivmusbdeviceattachedtovm-property"></a>Proprietà IVMUSBDevice:: AttachedToVM

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il nome della macchina virtuale a cui è collegato il dispositivo USB.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>Valore proprietà

Nome della macchina virtuale (VM).

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                           | Significato                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                              | Il dispositivo viene collegato alla macchina virtuale e viene restituito il relativo nome.<br/> |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                           | Il dispositivo è collegato all'host.<br/>                         |
| <dl> <dt>Macchina virtuale \_ 0xA00400929 \_ \_ \_ VM External USB E</dt> <dt></dt> </dl> | Il dispositivo è collegato a una macchina virtuale in un'altra sessione utente.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                | Il parametro è **null**.<br/>                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

