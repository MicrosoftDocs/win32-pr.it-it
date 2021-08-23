---
title: Proprietà IVMDVDDrive HostDriveLetter (VPCCOMInterfaces.h)
description: Lettera dell'unità host impostata per questo dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Proprietà HostDriveLetter Virtual PC
- Proprietà HostDriveLetter Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eb9105ec970331a755881d7f5b1425cf43c58f5267f5970042ce64b458070a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056869"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Proprietà IVMDVDDrive::HostDriveLetter

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la lettera dell'unità host impostata per questo dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valore proprietà

Lettera di unità.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                            | Significato                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | L'operazione è stata completata.<br/>                             |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                 | Il parametro è **NULL.**<br/>                                |
| <dl> <dt>E \_ FAIL</dt> <dt>0x80004005</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                         |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>         | Impossibile trovare la macchina virtuale.<br/>                   |
| <dl> <dt>Macchina virtuale \_ E \_ TIPO DI SUPPORTO \_ \_ ERRATO</dt> <dt>0xA00400728</dt> </dl> | Il supporto acquisito da questa unità DVD non è un'unità host.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>         | Si è verificato un errore imprevisto.<br/>                         |



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

 

