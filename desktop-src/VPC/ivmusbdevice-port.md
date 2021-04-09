---
title: Proprietà porta IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera l'identificatore della porta a cui è connesso il dispositivo.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Proprietà porta PC virtuale
- Proprietà porta Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà porta
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743239"
---
# <a name="ivmusbdeviceport-property"></a>IVMUSBDevice::P proprietà Ort

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'identificatore della porta a cui è connesso il dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a>Valore proprietà

Identificatore di porta. Questo valore viene assegnato dal driver del connettore USB.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                            | Significato                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | Metodo completato correttamente.<br/> |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl> | Il parametro è **null**.<br/>         |



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

 

