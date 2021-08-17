---
description: Put \_ LoopbackMode imposta la modalità di loopback multicast.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: Metodo IMulticastControl::p ut_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d564fbfd3e5ea0db2c168b6207823945eceb148af17d78bed25cbc59bb4e5ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140414"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>Metodo IMulticastControl::p ut \_ LoopbackMode

\[**put \_ LoopbackMode** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**Put \_ LoopbackMode imposta** la modalità di loopback multicast.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modalità* \[ Pollici\]
</dt> <dd>

[**MULTICAST \_ Descrittore \_ LOOPBACK MODE**](multicast-loopback-mode.md) della nuova modalità di loopback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro mode* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




