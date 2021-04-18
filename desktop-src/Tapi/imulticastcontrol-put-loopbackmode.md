---
description: Il \_ LoopbackMode put imposta la modalità loopback multicast.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl: metodo:p ut_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331602"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>IMulticastControl::p UT \_ LoopbackMode metodo

\[**Inserisci \_ LoopbackMode** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il **\_ LoopbackMode put** imposta la modalità loopback multicast.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modalità* \[ in\]
</dt> <dd>

[**Multicast \_ \_**](multicast-loopback-mode.md) Descrittore della modalità loopback della nuova modalità loopback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *mode* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




