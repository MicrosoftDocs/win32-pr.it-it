---
title: Metodo IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Rilascia un'unità fisica nell'host dall'unità floppy.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Metodo ReleaseHostDrive Virtual PC
- Metodo ReleaseHostDrive Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739770"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>Metodo IVMFloppyDrive:: ReleaseHostDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Rilascia un'unità fisica nell'host dall'unità floppy.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                          | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>          | La configurazione per questa macchina virtuale non è valida o non è stata trovata.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt> </dl>  | Il supporto collegato a questa unità floppy non è un'unità floppy fisica.<br/>     |
| <dl> <dt>**Macchina virtuale \_ E \_ nessun \_ supporto \_ acquisito**</dt> <dt>0xA00400652</dt> </dl> | Nessun supporto collegato a questa unità floppy.<br/>                            |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>          | Si è verificato un errore imprevisto.<br/>                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

