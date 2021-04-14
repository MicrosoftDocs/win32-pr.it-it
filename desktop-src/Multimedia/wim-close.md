---
title: Messaggio WIM_CLOSE (mmsystem. h)
description: Il \_ messaggio di chiusura WIM viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478718"
---
# <a name="wim_close-message"></a>\_Messaggio di chiusura Wim

Il messaggio di **\_ chiusura Wim** viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Riservati deve essere zero.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Audio Waveform](waveform-audio.md)
</dt> <dt>

[Messaggi di forma d'onda](waveform-messages.md)
</dt> </dl>

 

 





