---
title: Proprietà IVMUSBDevice ManufacturerString (VPCCOMInterfaces.h)
description: Recupera il nome del produttore del dispositivo USB.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Proprietà ManufacturerString Virtual PC
- Proprietà ManufacturerString Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà ManufacturerString
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0ec725779e4ffd18d46752f4083ad53c5b77c8392b45dc414d927b1038988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973711"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a>IvMUSBDevice::ManufacturerString - proprietà

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il nome del produttore del dispositivo USB.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a>Valore proprietà

Nome del produttore del dispositivo USB.

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

 

