---
title: Metodo IMsTscAxEvents OnAutoReconnecting
description: Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto). | Metodo IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting
- Metodo OnAutoReconnecting Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353486"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>Metodo IMsTscAxEvents:: OnAutoReconnecting

Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*disconnectReason* \[ in\]
</dt> <dd>

Codice che descrive il motivo dell'ultima disconnessione della sessione.

</dd> <dt>

*attemptCount* \[ in\]
</dt> <dd>

Numero di tentativi effettuati nel processo di riconnessione automatica corrente. Questo conteggio viene incrementato di uno per ogni tentativo eseguito.

</dd> <dt>

*pArcContinueStatus* \[ out\]
</dt> <dd>

Puntatore a un codice restituito che specifica lo stato del processo di riconnessione automatica. Questo codice può essere reimpostato per modificare lo stato del processo di riconnessione automatica corrente.

Per ulteriori informazioni sulla reimpostazione del codice, fare riferimento alla sezione Osservazioni.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic * * * * (0)


</dt> <dd>

Il processo di riconnessione si verifica automaticamente. Si tratta del valore predefinito.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop * * * * (1)


</dt> <dd>

Il processo di riconnessione è stato arrestato.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual * * * * (2)


</dt> <dd>

Il processo di riconnessione è in corso manualmente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere una notifica che indica che il controllo sta ristabiliscendo una connessione con un server Host sessione Desktop remoto.

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueAutomatic**, questo metodo funziona in modalità puramente consultivo. I contenitori possono restare in ascolto di questo evento per le notifiche che il processo di riconnessione automatica sta procedendo. Il controllo tenterà automaticamente di ristabilire una connessione in base ai propri tempi interni e ai conteggi dei tentativi. Questo metodo viene chiamato durante ogni tentativo di riconnessione automatica per notificare il contenitore.

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueStop**, il tentativo di riconnessione automatica corrente verrà interrotto, una notifica di disconnessione verrà inviata al contenitore e non verranno rilasciate altre notifiche automatiche di riconnessione.

> [!Note]  
> Usare la proprietà [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) per abilitare o disabilitare la riconnessione automatica.

 

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueManual**, il contenitore controllerà manualmente il processo di riconnessione automatica chiamando [**Connect**](imstscax-connect.md) per attivare un tentativo di connessione o [**disconnettersi**](imstscax-disconnect.md) per annullare il processo di riconnessione automatica. Una volta impostato su questo valore, il controllo smette di eseguire tentativi di riconnessione automatici e diventa il criterio del contenitore per effettuare **chiamate di connessione per** attivare i tentativi di riconnessione automatici. Questa operazione viene eseguita quando il contenitore fornisce un comportamento personalizzato dell'interfaccia utente per la riconnessione automatica, ad esempio il riavvio di una connessione RAS o VPN eliminata prima del processo di riconnessione automatica.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





