---
title: Metodo IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
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
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400514"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>Metodo IVMDVDDrive:: ReleaseHostDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                  |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>         | Impossibile trovare la macchina virtuale.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt> </dl> | Il supporto attualmente acquisito non è un'unità disco host.<br/>             |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl>      | Non è stato possibile inizializzare l'unità a causa di una posizione del bus non valida.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>         | Si è verificato un errore imprevisto.<br/>                                  |



 

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

 

