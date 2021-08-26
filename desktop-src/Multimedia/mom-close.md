---
title: MOM_CLOSE messaggio (Mmsystem.h)
description: Il messaggio MOM \_ CLOSE viene inviato a una funzione di callback di output MIDI quando un dispositivo di output MIDI viene chiuso.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE messaggio Windows multimediali
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbabd0cae61c1b1ea3d88df3cd2e52524b779eb7cdb5ac2c1e1a371546724f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038871"
---
# <a name="mom_close-message"></a>Messaggio MOM \_ CLOSE

Il **messaggio MOM \_ CLOSE** viene inviato a una funzione di callback di output MIDI quando un dispositivo di output MIDI viene chiuso.


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Riservato; non utilizzare .

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Riservato; non utilizzare .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

L'handle del dispositivo non è più valido dopo l'invio del messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

 





