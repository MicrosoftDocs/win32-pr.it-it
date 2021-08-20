---
title: Metodo GetTargetInfo IConnectionBrokerClient (Cbclient.h)
description: Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Metodo GetTargetInfo Servizi Desktop remoto
- Metodo GetTargetInfo Servizi Desktop remoto, interfaccia IConnectionBrokerClient
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto metodo , GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df214f23c09b7439843f0d7e8947d40cc32b2bf30eece887c921aac34306fbdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059189"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>Metodo IConnectionBrokerClient::GetTargetInfo

Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione. Questo metodo viene usato dal redirector per ottenere informazioni di reindirizzamento per la richiesta di connessione in ingresso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConnectionInfo* \[ Pollici\]
</dt> <dd>

Indirizzo di una struttura [**CB \_ CONNECTION \_ INFO**](cb-connection-info.md) che contiene informazioni sulla richiesta di connessione in ingresso.

</dd> <dt>

*Riservato* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere zero.

</dd> <dt>

*hStatusEvent* \[ Pollici\]
</dt> <dd>

Handle di un evento che verrà impostato ogni volta che viene aggiornato lo stato della richiesta. L'utente è responsabile della creazione e della chiusura di questo evento.

</dd> <dt>

*pTargetInfo* \[ Cambio\]
</dt> <dd>

Indirizzo di una struttura [**CB \_ TARGET \_ INFO**](cb-target-info.md) che riceve informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione in ingresso. Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*pResult* \[ Cambio\]
</dt> <dd>

Indirizzo di una **variabile DWORD** che riceve un codice risultato. Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta. Per altre informazioni, vedere la sezione Osservazioni.

Questo codice di risultato sarà uno dei valori seguenti.

<dt>

0
</dt> <dd>

Esito positivo.

</dd> <dt>

0x0000400
</dt> <dd>

Impossibile trovare il computer di destinazione.

</dd> <dt>

0x0000401
</dt> <dd>

Il computer di destinazione non è disponibile.

</dd> <dt>

0x0000402
</dt> <dd>

Errore durante il caricamento del computer di destinazione.

</dd> <dt>

0x0000403
</dt> <dd>

Errore durante la modalità online del computer di destinazione.

</dd> <dt>

0x0000404
</dt> <dd>

Errore durante il reindirizzamento al computer di destinazione.

</dd> <dt>

0x0000405
</dt> <dd>

Errore durante la ri sveglia della macchina virtuale.

</dd> <dt>

0x0000406
</dt> <dd>

Errore durante l'avvio della macchina virtuale.

</dd> <dt>

0x0000407
</dt> <dd>

Errore durante la ricerca dell'indirizzo IP della macchina virtuale.

</dd> <dt>

0x0000408
</dt> <dd>

Il gestore di sessione non è stato in grado di trovare computer disponibili nel pool.

</dd> <dt>

0x0000409
</dt> <dd>

Il gestore di sessione ha annullato la connessione.

</dd> <dt>

0x0000410
</dt> <dd>

Il gestore di sessione non è stato in grado di convalidare le impostazioni di connessione.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore a [**interfaccia IConnectionBrokerRequest**](iconnectionbrokerrequest.md) utilizzato per ottenere gli aggiornamenti dello stato per un'operazione asincrona. Questa interfaccia viene usata insieme al *parametro hStatusEvent* per attendere e ottenere i risultati di questa operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **E \_ PENDING se** viene creata la richiesta asincrona. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo è asincrono. I *parametri pTargetInfo* *e pResult* devono rimanere validi finché il metodo [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) non ottiene **CB STATUS REQUEST \_ \_ \_ COMPLETED.**

Per altre informazioni su come usare questo metodo, vedere [Come usare l'API client Connessione Desktop remoto Broker](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





