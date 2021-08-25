---
title: Metodo IVMFloppyDrive ReleaseImage (VPCCOMInterfaces.h)
description: Rilascia un'immagine del supporto floppy nell'host dall'unità floppy.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- Metodo ReleaseImage Virtual PC
- Metodo ReleaseImage Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253e62ec35ccca5a254c6e70ef7fd1890fb6c1a52848c84d319686e0726a038d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654051"
---
# <a name="ivmfloppydrivereleaseimage-method"></a>Metodo IVMFloppyDrive::ReleaseImage

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rilascia un'immagine del supporto floppy nell'host dall'unità floppy.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                          | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>          | La configurazione per questa macchina virtuale non è valida o non è possibile trovare.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI SUPPORTO \_ \_ ERRATO**</dt> <dt>0xA00400728</dt> </dl>  | Il supporto collegato a questa unità floppy non è un'immagine disco floppy.<br/>         |
| <dl> <dt>**Macchina virtuale \_ E \_ NESSUN SUPPORTO ACQUISITO \_ \_ 0XA00400652**</dt> <dt></dt> </dl> | Non sono presenti supporti collegati a questa unità floppy.<br/>                            |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>          | Si è verificato un errore imprevisto.<br/>                                           |



 

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

 

