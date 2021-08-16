---
title: Metodo IVMDVDDrive ReleaseImage (VPCCOMInterfaces.h)
description: Rilascia un'immagine ISO acquisita dall'unità DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Metodo ReleaseImage Virtual PC
- Metodo ReleaseImage Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0fc61212ff07f3a0279dfdb38517d4ab2d265d89e15aaad61450e3effd9ec9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345733"
---
# <a name="ivmdvddrivereleaseimage-method"></a>Metodo IVMDVDDrive::ReleaseImage

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rilascia un'immagine ISO acquisita dall'unità DVD.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                         | Descrizione                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | L'operazione è stata completata.<br/>                                      |
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

 

