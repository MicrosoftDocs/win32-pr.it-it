---
title: Metodo IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces.h)
description: Rilascia un'unità host acquisita dall'unità DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Metodo ReleaseHostDrive Virtual PC
- Metodo ReleaseHostDrive Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865b9aa54304d8ddacacf048825d6c9767347f341d31524cbd4dd60d7060ae4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136804"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>Metodo IVMDVDDrive::ReleaseHostDrive

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rilascia un'unità host acquisita dall'unità DVD.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                         | Descrizione                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | L'operazione è stata completata.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>         | Impossibile trovare la macchina virtuale.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728**</dt> <dt></dt> </dl> | Il supporto attualmente acquisito non è un'unità disco host.<br/>             |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON**</dt> VALIDA <dt>0xA0040502</dt> </dl>      | Impossibile inizializzare l'unità a causa di una posizione del bus non valida.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>         | Si è verificato un errore imprevisto.<br/>                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive è definito come \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

