---
title: Proprietà File IVMHardDisk (VPCCOMInterfaces.h)
description: Recupera il nome del percorso completo del file del disco rigido virtuale.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Proprietà File Virtual PC
- Proprietà File Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà File
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e207b14bd974d42ee694b6897ae42106ba5c3f87adb9b4ed880f288f0d28fd9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593676"
---
# <a name="ivmharddiskfile-property"></a>Proprietà IVMHardDisk::File

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il nome del percorso completo del file del disco rigido virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a>Valore proprietà

Nome del percorso completo del file di immagine del disco rigido corrente.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



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

 

