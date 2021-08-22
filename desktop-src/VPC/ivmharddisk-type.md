---
title: Proprietà Tipo IVMHardDisk (VPCCOMInterfaces.h)
description: Tipo di disco rigido virtuale.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Proprietà Type Virtual PC
- Proprietà Type Virtual PC , interfaccia IVMHardDisk
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
ms.openlocfilehash: 39c2ba462496f6791d129918b93401c971b755ef40c40ef9a1177059dc7bcce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998931"
---
# <a name="ivmharddisktype-property"></a>Proprietà IVMHardDisk::Type

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il tipo di disco rigido virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Valore proprietà

Tipo dell'immagine del disco rigido corrente.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                  |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL.**<br/>                                                     |
| <dl> <dt>HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO) 0X80070002</dt> <dt></dt> </dl> | Impossibile trovare il file di immagine del disco rigido corrente.<br/>                           |
| <dl> <dt>Macchina virtuale \_ E \_ UNITÀ \_ NON</dt> <dt>0XA0040502</dt> </dl>                         | Il tipo dell'immagine del disco rigido corrente non è valido.<br/>                            |
| <dl> <dt>Macchina virtuale \_ E \_ HD IMAGE OPEN FAIL \_ \_ \_ 0xA004067C</dt> <dt></dt> </dl>                  | Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.<br/>   |
| <dl> <dt>Macchina virtuale \_ E \_ HD IMAGE ACCESS \_ \_ 0xA0040681</dt> <dt></dt> </dl>                      | Si è verificato un errore durante il tentativo di accedere al file di immagine del disco rigido corrente.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                              |



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

 

