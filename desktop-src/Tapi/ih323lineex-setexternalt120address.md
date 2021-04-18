---
description: Il metodo SetExternalT120Address viene chiamato da un'applicazione per configurare un indirizzo T. 120 esterno per lo scambio di dati.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'Metodo IH323LineEx:: SetExternalT120Address (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326146"
---
# <a name="ih323lineexsetexternalt120address-method"></a>Metodo IH323LineEx:: SetExternalT120Address

\[**SetExternalT120Address** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetExternalT120Address** viene chiamato da un'applicazione per configurare un indirizzo T. 120 esterno per lo scambio di dati. La funzionalità T. 120 verrà annunciata durante la negoziazione H. 245 e l'indirizzo verrà usato nel riconoscimento del canale della logica aperto, in modo che l'altro endpoint possa configurare sessioni T. 120 con il servizio in ascolto su tale indirizzo. Se questa funzione non viene chiamata, il provider di servizi H. 323 non annuncia la funzionalità T. 120.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnable* \[ in\]
</dt> <dd>

**True** per abilitare la funzionalità T. 120; **False** per disabilitare la funzionalità T. 120.

</dd> <dt>

*dwIP* \[ in\]
</dt> <dd>

**DWORD** che contiene l'indirizzo IP nell'ordine dei byte dell'host del servizio esterno T. 120.

</dd> <dt>

*wPort* \[ in\]
</dt> <dd>

**Parola** contenente la porta del servizio esterno T. 120.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




