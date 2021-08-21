---
title: Proprietà IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces.h)
description: Recupera la quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Proprietà HostFreeDiskSpace Virtual PC
- Proprietà HostFreeDiskSpace Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b92c8a1253fb4dbefb6db2f2ed9a9d278b907ecfb30e448edb36ec2cbe98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123701"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>Proprietà IVMHardDisk::HostFreeDiskSpace

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valore proprietà

Quantità di spazio su disco rimanente disponibile nel computer host per il file di immagine del disco rigido corrente. Questo valore è variant **di** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                            | Significato                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | L'operazione è stata completata.<br/>                                |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                 | Il parametro è **NULL.**<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl> | Il percorso del file del disco rigido virtuale corrente non è valido.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                         | Si è verificato un errore imprevisto.<br/>                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk è definito come \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

