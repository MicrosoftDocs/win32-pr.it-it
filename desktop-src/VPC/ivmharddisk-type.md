---
title: Proprietà Type di IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo del disco rigido virtuale.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Tipo proprietà PC virtuale
- Proprietà del tipo Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà Type
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048322"
---
# <a name="ivmharddisktype-property"></a>Proprietà IVMHardDisk:: Type

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il tipo del disco rigido virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Valore proprietà

Tipo di immagine del disco rigido corrente.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                  |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>                                                     |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Impossibile trovare il file di immagine del disco rigido corrente.<br/>                           |
| <dl> <dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt> </dl>                         | Il tipo di immagine del disco rigido corrente non è valido.<br/>                            |
| <dl> <dt>Macchina virtuale \_ E \_ \_ immagine HD \_ \_ non riuscita</dt> <dt>0xA004067C</dt> </dl>                  | Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.<br/>   |
| <dl> <dt>Macchina virtuale \_ E \_ \_ \_ accesso alle immagini HD</dt> <dt>0xA0040681</dt> </dl>                      | Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                              |



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

 

