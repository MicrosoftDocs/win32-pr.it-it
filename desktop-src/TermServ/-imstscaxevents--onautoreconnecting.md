---
title: Metodo IMsTscAxEvents OnAutoReconnecting
description: Chiamato quando un client sta per riconnettersi automaticamente a una sessione con un server Host sessione Desktop remoto sessione Desktop remoto. | Metodo IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Metodo OnAutoReconnecting Servizi Desktop remoto
- Metodo OnAutoReconnecting Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnAutoReconnecting
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
ms.openlocfilehash: 2a26bb57416cd73f6d838ab08167923c4900b7b923a6a6f411239bbacd3fdbac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309141"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>Metodo IMsTscAxEvents::OnAutoReconnecting

Chiamato quando un client sta per riconnettersi automaticamente a una sessione con un server Host sessione Desktop remoto sessione Desktop remoto.

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

*disconnectReason* \[ Pollici\]
</dt> <dd>

Codice che descrive il motivo dell'ultima disconnessione della sessione.

</dd> <dt>

*attemptCount* \[ Pollici\]
</dt> <dd>

Numero di tentativi effettuati nel processo di riconnessione automatica corrente. Questo conteggio aumenta di uno per ogni tentativo eseguito.

</dd> <dt>

*pArcContinueStatus* \[ Cambio\]
</dt> <dd>

Puntatore a un codice restituito che specifica lo stato del processo di riconnessione automatica. Questo codice può essere reimpostato per modificare lo stato del processo di riconnessione automatica corrente.

Per altre informazioni sulla reimpostazione di questo codice, vedere la sezione Osservazioni.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic**** (0)


</dt> <dd>

Il processo di riconnessione viene eseguita automaticamente. Si tratta del valore predefinito.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop**** (1)


</dt> <dd>

Il processo di riconnessione è stato arrestato.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual**** (2)


</dt> <dd>

Il processo di riconnessione avviene manualmente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere la notifica che il controllo sta ristabilindo una connessione con un server Host sessione Desktop remoto.

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueAutomatic,** questo metodo funziona in modalità puramente consultivo. I contenitori possono restare in ascolto di questo evento per le notifiche che il processo di riconnessione automatica sta procedendo. Il controllo continuerà automaticamente a tentare di ristabilire una connessione in base al proprio intervallo interno e ai conteggi dei tentativi. Questo metodo viene chiamato durante ogni tentativo di riconnessione automatica per notificare al contenitore.

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueStop**, il tentativo di riconnessione automatica corrente verrà terminato, verrà inviata una notifica di disconnessione al contenitore e non verranno emesse altre notifiche di riconnessione automatica.

> [!Note]  
> Usare la [**proprietà EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) per abilitare o disabilitare la riconnessione automatica.

 

Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueManual,** il contenitore controlla manualmente il processo di riconnessione automatica chiamando [**Connessione per**](imstscax-connect.md) attivare un tentativo di connessione o [**Disconnetti**](imstscax-disconnect.md) per annullare il processo di riconnessione automatica. Una volta impostato su questo valore, il controllo smette di eseguire tentativi di riconnessione automatica e diventa il criterio del contenitore **per** eseguire chiamate Connessione per attivare i tentativi di riconnessione automatica. Questa operazione viene eseguita quando il contenitore fornisce un comportamento personalizzato dell'interfaccia utente per la riconnessione automatica, ad esempio il riavvio di una connessione RAS o VPN eliminata prima del processo di riconnessione automatica.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





