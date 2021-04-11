---
title: Metodo IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Connette un'immagine multimediale floppy nell'host all'unità floppy della macchina virtuale.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Metodo AttachImage Virtual PC
- Metodo AttachImage Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964071"
---
# <a name="ivmfloppydriveattachimage-method"></a>Metodo IVMFloppyDrive:: AttachImage

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Connette un'immagine multimediale floppy nell'host all'unità floppy della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mediaImagePath* \[ in\]
</dt> <dd>

Percorso completo dell'immagine multimediale floppy da collegare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                 | Il parametro *mediaImagePath* non è valido.<br/>                                                                                 |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt> </dl>      | La memoria disponibile non è sufficiente per completare la richiesta.<br/>                                                               |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal parametro *mediaImagePath* è troppo lungo. Il percorso deve essere minore di **Max \_ path** (260) caratteri.<br/> |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *mediaImagePath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *mediaImagePath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                            | La configurazione per questa macchina virtuale non è valida o non è stata trovata.<br/>                                                  |
| <dl> <dt>**Macchina virtuale \_ \_Acquisizione immagini \_ E \_ non riuscita**</dt> <dt>0xA00400650</dt> </dl>                  | Impossibile acquisire il file di immagine specificato.<br/>                                                                              |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

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

 

