---
description: Il metodo GetRange recupera l'intervallo di valori validi per una determinata proprietà delle impostazioni audio.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: Metodo ITAudioSettings::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08c9eed736725bd4200c79583dcc12abde11399ec272be04805881752b19119
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992011"
---
# <a name="itaudiosettingsgetrange-method"></a>Metodo ITAudioSettings::GetRange

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo GetRange** recupera l'intervallo di valori validi per una determinata [**proprietà delle impostazioni audio.**](audiosettingsproperty.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione AudioSettingsProperty.**](audiosettingsproperty.md)

</dd> <dt>

*plMin* \[ Cambio\]
</dt> <dd>

Valore minimo valido per la proprietà di input.

</dd> <dt>

*plMax* \[ Cambio\]
</dt> <dd>

Valore massimo valido per la proprietà di input.

</dd> <dt>

*plSteppingDelta* \[ Cambio\]
</dt> <dd>

Incremento in base al quale il valore della proprietà può essere aumentato o diminuito.

</dd> <dt>

*plDefault* \[ Cambio\]
</dt> <dd>

Valore predefinito per il *parametro Property.*

</dd> <dt>

*plFlags* \[ Cambio\]
</dt> <dd>

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come viene *controllato il valore* di Property.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**Proprietà AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




