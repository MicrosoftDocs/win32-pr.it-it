---
title: Proprietà BusNumber IVMDVDDrive (VPCCOMInterfaces.h)
description: Recupera il numero di bus a cui è collegato il dispositivo.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Proprietà BusNumber Virtual PC
- Proprietà BusNumber Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420a3ebdb2f4b4d04532e387c0466a2938e2e51c9ffafac3b975862cddb11169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136824"
---
# <a name="ivmdvddrivebusnumber-property"></a>Proprietà IVMDVDDrive::BusNumber

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il numero di bus a cui è collegato il dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valore proprietà

Numero del bus. Ad esempio, in un bus IDE, questo valore rappresenta la posizione primaria o secondaria.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                       | Significato                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | L'operazione è stata completata.<br/>                                          |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>            | Il parametro è **NULL.**<br/>                                             |
| <dl> <dt>Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA</dt> <dt>0xA0040502</dt> </dl> | Il percorso del bus per questa unità DVD non è stato inizializzato correttamente.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>    | Si è verificato un errore imprevisto.<br/>                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

