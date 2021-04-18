---
title: Proprietà file IVMHardDisk (VPCCOMInterfaces. h)
description: Recupera il nome del percorso completo del file del disco rigido virtuale.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Proprietà file Virtual PC
- Proprietà file Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà file
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
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302417"
---
# <a name="ivmharddiskfile-property"></a>Proprietà IVMHardDisk:: file

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

