---
description: Il metodo Get recupera il valore di una proprietà di impostazione audio specificata.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'Metodo ITAudioSettings:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331600"
---
# <a name="itaudiosettingsget-method"></a>Metodo ITAudioSettings:: Get

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **Get** Recupera il valore di una [**proprietà di impostazione audio**](audiosettingsproperty.md)specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ di in\]
</dt> <dd>

Membro dell'enumerazione [**AudioSettingsProperty**](audiosettingsproperty.md) .

</dd> <dt>

*plValue* \[ out\]
</dt> <dd>

Valore della *Proprietà* di input.

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




