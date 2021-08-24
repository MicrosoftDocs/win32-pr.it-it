---
description: Il metodo get \_ LoopbackMode ottiene la modalità di loopback multicast.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: Metodo IMulticastControl::get_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013021"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>Metodo IMulticastControl::get \_ LoopbackMode

\[**get \_ LoopbackMode** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ LoopbackMode** ottiene la modalità di loopback multicast.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMode* \[ Cambio\]
</dt> <dd>

Puntatore al [**descrittore \_ MULTICAST LOOPBACK \_ MODE**](multicast-loopback-mode.md) della modalità di loopback corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Significato                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro pMode* non è valido.<br/> |



 

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

 

 




