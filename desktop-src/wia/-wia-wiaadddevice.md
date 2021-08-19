---
description: La funzione WiaAddDevice richiama l'interfaccia utente dell'Installazione guidata scanner e fotocamera. Equivale a eseguire &\# 0034;rundll32.exe sti \_ci.dll AddDevice&\# 0034; dal prompt dei comandi.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Funzione WiaAddDevice (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965400"
---
# <a name="wiaadddevice-function"></a>Funzione WiaAddDevice

La **funzione WiaAddDevice** richiama l'interfaccia utente dell'Installazione guidata scanner e fotocamera. Equivale a eseguire "rundll32.exe sti \_ci.dll AddDevice" dal prompt dei comandi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata con credenziali di amministratore. Quando viene eseguito in Controllo dell'account utente , il processo deve essere elevato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




