---
title: Proprietà IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
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
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741095"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Proprietà IVMDVDDrive:: HostDriveLetter

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la lettera del set di unità host per questo dispositivo.

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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                 | Il parametro è **null**.<br/>                                |
| <dl> <dt>E \_ ERRORE</dt> <dt>0x80004005</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                         |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>         | Impossibile trovare la macchina virtuale.<br/>                   |
| <dl> <dt>Macchina virtuale \_ E \_ media \_ di \_ tipo errato</dt> <dt>0xA00400728</dt> </dl> | Il supporto acquisito da questa unità DVD non è un'unità host.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>         | Si è verificato un errore imprevisto.<br/>                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

