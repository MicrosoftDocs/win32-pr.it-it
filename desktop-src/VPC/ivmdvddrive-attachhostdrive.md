---
title: Metodo IVMDVDDrive AttachHostDrive (VPCCOMInterfaces.h)
description: Collega un'unità host all'unità DVD all'interno della macchina virtuale.
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
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136854"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>Metodo IVMDVDDrive::AttachHostDrive

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Collega un'unità host all'unità DVD all'interno della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*driveLetter* \[ Pollici\]
</dt> <dd>

Lettera dell'unità host da collegare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | L'operazione è stata completata.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ InvalidARG**</dt> <dt>0x80000003</dt> </dl>         | Non è stata specificata alcuna lettera di unità oppure la lettera di unità specificata non è valida.<br/>                                                                                                  |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>               | Si è verificato un errore imprevisto.<br/>                                                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>    | Impossibile trovare la macchina virtuale.<br/>                                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ UNITÀ \_ E \_ IN \_ USO**</dt> <dt>0xA0040727</dt> </dl> | Un'unità DVD host o un'immagine ISO è già collegata a questa unità all'interno della macchina virtuale oppure l'unità host specificata è già in uso all'interno di un'altra macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA**</dt> <dt>0xA0040502</dt> </dl> | Il percorso del bus per questa unità non è valido o l'unità non sembra essere un'unità DVD valida.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>    | Si è verificato un errore imprevisto.<br/>                                                                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

