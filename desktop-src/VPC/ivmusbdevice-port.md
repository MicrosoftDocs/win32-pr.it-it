---
title: Proprietà IvMUSBDevice Port (VPCCOMInterfaces.h)
description: Recupera l'identificatore della porta a cui è connesso il dispositivo.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Proprietà Port Virtual PC
- Proprietà Porta Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà Port
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
ms.openlocfilehash: d5b564f1e8c75ecbf5bb140d17218df83bc5b23f5de219c819dc5c4f31f7be14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998711"
---
# <a name="ivmusbdeviceport-property"></a>IVMUSBDevice::P ort

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl> | Il parametro è **NULL.**<br/>         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDevice è definito come \_ 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

