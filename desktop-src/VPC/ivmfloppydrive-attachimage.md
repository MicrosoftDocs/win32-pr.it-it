---
title: Metodo IVMFloppyDrive AttachImage (VPCCOMInterfaces.h)
description: Collega un'immagine del supporto floppy nell'host all'unità floppy della macchina virtuale.
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
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595715"
---
# <a name="ivmfloppydriveattachimage-method"></a>Metodo IVMFloppyDrive::AttachImage

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Collega un'immagine del supporto floppy nell'host all'unità floppy della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mediaImagePath* \[ Pollici\]
</dt> <dd>

Percorso completo dell'immagine del supporto floppy da collegare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro mediaImagePath* non è valido.<br/>                                                                                 |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | La memoria disponibile non è sufficiente per completare la richiesta.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro mediaImagePath* è troppo lungo. Il percorso deve essere minore di **MAX \_ PATH** (260).<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro mediaImagePath* contiene un carattere non valido (uno tra " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Il *parametro mediaImagePath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                            | La configurazione per questa macchina virtuale non è valida o non è possibile trovare.<br/>                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ IMAGE CAPTURE FAIL \_ \_ 0XA00400650**</dt> <dt></dt> </dl>                  | Impossibile acquisire il file di immagine specificato.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive è definito come 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

