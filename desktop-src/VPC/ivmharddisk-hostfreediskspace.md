---
title: Proprietà IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
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
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121191"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>Proprietà IVMHardDisk:: HostFreeDiskSpace

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valore proprietà

Quantità di spazio su disco rimanente disponibile nel computer host per il file di immagine del disco rigido corrente. Questo valore è una **variante** di tipo \_ decimale VT.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                            | Significato                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | L'operazione è stata completata.<br/>                                |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                 | Il parametro è **null**.<br/>                                   |
| <dl> <dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt> </dl> | Il percorso del file del disco rigido virtuale corrente non è valido.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                         | Si è verificato un errore imprevisto.<br/>                            |



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

 

