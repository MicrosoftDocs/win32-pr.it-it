---
title: Metodo IMsTscAxEvents OnAutoReconnecting2
description: Chiamato quando un client è in corso la riconnessione automatica di una sessione con un server host sessione Desktop remoto (Host sessione Desktop remoto). | Metodo IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Metodo OnAutoReconnecting2 Servizi Desktop remoto
- Metodo OnAutoReconnecting2 Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194c21fc8ddc6f93ac4816752956f8de5a1d5df71b3af98ddadf8aba48e421a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512491"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Metodo IMsTscAxEvents::OnAutoReconnecting2

Chiamato quando un client è in corso la riconnessione automatica di una sessione con un server host sessione Desktop remoto (Host sessione Desktop remoto). Si tratta di una versione avanzata del [**metodo OnAutoReconnecting.**](-imstscaxevents--onautoreconnecting.md)

## <a name="syntax"></a>Sintassi


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*disconnectReason* \[ Pollici\]
</dt> <dd>

Codice che descrive il motivo dell'ultima disconnessione della sessione.

</dd> <dt>

*networkAvailable* \[ Pollici\]
</dt> <dd>

Specifica se la rete è disponibile.

</dd> <dt>

*attemptCount* \[ Pollici\]
</dt> <dd>

Numero di tentativi evasi nel processo di riconnessione automatica corrente. Questo conteggio aumenta di uno per ogni tentativo effettuato.

</dd> <dt>

*maxAttemptCount* \[ Pollici\]
</dt> <dd>

Numero massimo di tentativi che verranno evasi nel processo di riconnessione automatica corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





