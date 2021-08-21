---
description: Il metodo GetRange recupera l'intervallo di valori validi per una determinata proprietà del dispositivo audio.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: Metodo ITAudioDeviceControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87779131dea5bb01a1575074e4f019dbfa2a62addebf5b91a7eee6e9cc041710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003449"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>Metodo ITAudioDeviceControl::GetRange

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo GetRange** recupera l'intervallo di valori validi per una determinata [**proprietà del dispositivo audio**](audiodeviceproperty.md).

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

Membro [**dell'enumerazione AudioDeviceProperty.**](audiodeviceproperty.md)

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

Incremento del quale il valore della proprietà può essere aumentato o diminuito.

</dd> <dt>

*plDefault* \[ Cambio\]
</dt> <dd>

Valore predefinito per il *parametro Property.*

</dd> <dt>

*plFlags* \[ Cambio\]
</dt> <dd>

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come viene *controllato il valore* della proprietà.

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

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**Proprietà AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




