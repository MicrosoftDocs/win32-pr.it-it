---
title: Proprietà HardDisk IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Recupera un oggetto disco rigido corrispondente a questa connessione.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Proprietà disco rigido Virtual PC
- Proprietà HardDisk Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà HardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400724"
---
# <a name="ivmharddiskconnectionharddisk-property"></a>Proprietà IVMHardDiskConnection:: HardDisk

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un oggetto disco rigido corrispondente a questa connessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMHardDisk**](ivmharddisk.md) che descrive il disco rigido associato a questa connessione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                       | Significato                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | L'operazione è stata completata.<br/>                                                                                                    |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>            | Il parametro è **null** o non è valido.<br/>                                                                                          |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>    | La configurazione della macchina virtuale corrente non è valida.<br/>                                                                          |
| <dl> <dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt> </dl> | Il percorso del bus per questa connessione non è stato inizializzato correttamente o il dispositivo in questa posizione non è un disco rigido valido.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>    | Si è verificato un errore imprevisto.<br/>                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

