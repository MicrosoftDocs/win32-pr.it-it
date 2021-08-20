---
description: Il metodo Get recupera il valore di una determinata proprietà del dispositivo audio.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: Metodo ITAudioDeviceControl::Get (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2877b48eab2ecab6259a034c9d74f4c32b9fae9233f5ceb0a0a409f43add014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865785"
---
# <a name="itaudiodevicecontrolget-method"></a>Metodo ITAudioDeviceControl::Get

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Get** recupera il valore di una determinata proprietà del dispositivo [**audio.**](audiodeviceproperty.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione AudioDeviceProperty.**](audiodeviceproperty.md)

</dd> <dt>

*plValue* \[ Cambio\]
</dt> <dd>

Valore della proprietà *di* input .

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

 

 




