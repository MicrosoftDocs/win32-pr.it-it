---
title: Proprietà IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces.h)
description: Recupera un oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk - proprietà Virtual PC
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
ms.openlocfilehash: 3ba90d72aeab4fae618c3113796de1335d005670369de514b4e0650fead75d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998921"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>Proprietà IVMHardDiskConnection::UndoHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL** o non è valido.<br/>                                                                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Impossibile trovare il disco di annullamento per questa connessione.<br/>                                                                                 |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>                            | La configurazione della macchina virtuale corrente non è valida.<br/>                                                                          |
| <dl> <dt>Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA</dt> <dt>0xA0040502</dt> </dl>                         | La posizione del bus per questa connessione non è stata inizializzata correttamente o il dispositivo in questa posizione non è un disco rigido valido.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection è definito come aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

