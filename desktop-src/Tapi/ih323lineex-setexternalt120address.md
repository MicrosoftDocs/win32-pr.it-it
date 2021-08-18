---
description: Il metodo SetExternalT120Address viene chiamato da un'applicazione per configurare un indirizzo T.120 esterno per lo scambio di dati.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: Metodo IH323LineEx::SetExternalT120Address (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8889887c396c427c28ac2906206b3e3cbbcb102daa937720b6b879472b47bbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992091"
---
# <a name="ih323lineexsetexternalt120address-method"></a>Metodo IH323LineEx::SetExternalT120Address

\[**SetExternalT120Address** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo SetExternalT120Address** viene chiamato da un'applicazione per configurare un indirizzo T.120 esterno per lo scambio di dati. La funzionalità T.120 verrà annunciata durante la negoziazione H.245 e l'indirizzo verrà usato nell'acknowledgement del canale logico aperto in modo che l'altro endpoint possa configurare sessioni T.120 con il servizio in ascolto su tale indirizzo. Se questa funzione non viene chiamata, il provider di servizi H.323 non pubblicizza la funzionalità T.120.

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

*fEnable* \[ Pollici\]
</dt> <dd>

**TRUE** per abilitare la funzionalità T.120; **FALSE** per disabilitare la funzionalità T.120.

</dd> <dt>

*dwIP* \[ Pollici\]
</dt> <dd>

**DWORD** contenente l'indirizzo IP nell'ordine dei byte host del servizio T.120 esterno.

</dd> <dt>

*wPort* \[ Pollici\]
</dt> <dd>

**WORD** contenente la porta del servizio T.120 esterno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




