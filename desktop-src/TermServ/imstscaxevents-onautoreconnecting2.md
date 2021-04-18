---
title: Metodo IMsTscAxEvents OnAutoReconnecting2
description: Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto). | Metodo IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting2
- Metodo OnAutoReconnecting2 Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAutoReconnecting2
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
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321769"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Metodo IMsTscAxEvents:: OnAutoReconnecting2

Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto). Si tratta di una versione migliorata del metodo [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .

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

*disconnectReason* \[ in\]
</dt> <dd>

Codice che descrive il motivo dell'ultima disconnessione della sessione.

</dd> <dt>

*NetworkAvailable* \[ in\]
</dt> <dd>

Specifica se la rete è disponibile.

</dd> <dt>

*attemptCount* \[ in\]
</dt> <dd>

Numero di tentativi effettuati nel processo di riconnessione automatica corrente. Questo conteggio viene incrementato di uno per ogni tentativo eseguito.

</dd> <dt>

*maxAttemptCount* \[ in\]
</dt> <dd>

Numero massimo di tentativi che verranno eseguiti nel processo di riconnessione automatica corrente.

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

 

 





