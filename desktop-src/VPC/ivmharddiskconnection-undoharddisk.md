---
title: Proprietà IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces. h)
description: Recupera un oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Proprietà UndoHardDisk Virtual PC
- Proprietà UndoHardDisk Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118926"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>Proprietà IVMHardDiskConnection:: UndoHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMHardDisk**](ivmharddisk.md) che descrive il disco rigido di annullamento associato a questa connessione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                    |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null** o non è valido.<br/>                                                                                          |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Il disco di annullamento per questa connessione non è stato trovato.<br/>                                                                                 |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>                            | La configurazione della macchina virtuale corrente non è valida.<br/>                                                                          |
| <dl> <dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt> </dl>                         | Il percorso del bus per questa connessione non è stato inizializzato correttamente o il dispositivo in questa posizione non è un disco rigido valido.<br/> |



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

 

