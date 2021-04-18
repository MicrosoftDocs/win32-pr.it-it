---
title: Metodo IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Connette un'unità host all'unità DVD all'interno della macchina virtuale.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Metodo AttachHostDrive Virtual PC
- Metodo AttachHostDrive Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302420"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>Metodo IVMDVDDrive:: AttachHostDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Connette un'unità host all'unità DVD all'interno della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LetteraUnità* \[ in\]
</dt> <dd>

Lettera dell'unità host da collegare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | L'operazione è stata completata.<br/>                                                                                                                                             |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>         | Non è stata specificata alcuna lettera di unità o la lettera di unità specificata non è valida.<br/>                                                                                                  |
| <dl> <dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt> </dl>               | Si è verificato un errore imprevisto.<br/>                                                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>    | Impossibile trovare la macchina virtuale.<br/>                                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ \_Unità E \_ in \_ use**</dt> <dt>0xA0040727</dt> </dl> | Un'unità DVD o un'immagine ISO host è già collegata a questa unità all'interno della macchina virtuale oppure l'unità host specificata è già in uso in un'altra macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl> | Il percorso del bus per questa unità non è valido o l'unità non sembra essere un'unità DVD valida.<br/>                                                                         |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>    | Si è verificato un errore imprevisto.<br/>                                                                                                                                         |



 

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

 

