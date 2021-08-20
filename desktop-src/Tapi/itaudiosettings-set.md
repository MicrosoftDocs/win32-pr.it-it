---
description: Il metodo Set imposta il valore di una determinata proprietà delle impostazioni audio.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: Metodo ITAudioSettings::Set (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf26b35e3d5be18721abb6d8dd109946503cb11cb30d5c7db869d92e88adfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003399"
---
# <a name="itaudiosettingsset-method"></a>Metodo ITAudioSettings::Set

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Set** imposta il valore di una determinata proprietà delle impostazioni [**audio**](audiosettingsproperty.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione AudioSettingsProperty.**](audiosettingsproperty.md)

</dd> <dt>

*lValue* \[ Pollici\]
</dt> <dd>

Valore desiderato per la proprietà.

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come *deve* essere controllato il valore della proprietà.

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

[**Proprietà AudioSettings**](audiosettingsproperty.md)
</dt> </dl>

 

 




