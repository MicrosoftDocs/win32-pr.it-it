---
title: Metodo IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTargetInfo
- Metodo GetTargetInfo Servizi Desktop remoto, interfaccia IConnectionBrokerClient
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto, metodo GetTargetInfo
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
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517368"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>Metodo IConnectionBrokerClient:: GetTargetInfo

Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione. Questo metodo viene utilizzato dal redirector per ottenere informazioni di reindirizzamento per la richiesta di connessione in ingresso.

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

*pConnectionInfo* \[ in\]
</dt> <dd>

Indirizzo di una struttura [**di \_ \_ informazioni di connessione CB**](cb-connection-info.md) che contiene informazioni sulla richiesta di connessione in ingresso.

</dd> <dt>

*Riservato* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere zero.

</dd> <dt>

*hStatusEvent* \[ in\]
</dt> <dd>

Handle di un evento che verrà impostato ogni volta che viene eseguito un aggiornamento dello stato di avanzamento della richiesta. L'utente è responsabile della creazione e della chiusura di questo evento.

</dd> <dt>

*pTargetInfo* \[ out\]
</dt> <dd>

Indirizzo di una struttura [**di \_ \_ informazioni di destinazione del CB**](cb-target-info.md) che riceve informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione in ingresso. Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*pResult* \[ out\]
</dt> <dd>

Indirizzo di una variabile **DWORD** che riceve un codice risultato. Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta. Per altre informazioni, vedere la sezione Osservazioni.

Il codice risultante sarà uno dei valori seguenti.

<dt>

0
</dt> <dd>

Esito positivo.

</dd> <dt>

0x0000400
</dt> <dd>

Il computer di destinazione non è stato trovato.

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

Errore durante la porta del computer di destinazione online.

</dd> <dt>

0x0000404
</dt> <dd>

Errore durante il reindirizzamento al computer di destinazione.

</dd> <dt>

0x0000405
</dt> <dd>

Errore durante il riattivazione della macchina virtuale.

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

Il broker di sessione non è riuscito a trovare i computer disponibili nel pool.

</dd> <dt>

0x0000409
</dt> <dd>

Il broker di sessione ha annullato la connessione.

</dd> <dt>

0x0000410
</dt> <dd>

Il broker di sessione non è riuscito a convalidare le impostazioni di connessione.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a interfaccia [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) usato per ottenere gli aggiornamenti di stato per un'operazione asincrona. Questa interfaccia viene utilizzata insieme al parametro *hStatusEvent* per attendere e ottenere i risultati di questa operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **E \_ in sospeso** se la richiesta asincrona viene creata. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo è asincrono. I parametri *pTargetInfo* e *pResult* devono rimanere validi finché il metodo [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) non ottiene la richiesta di **stato CB \_ \_ \_ completata**.

Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [come utilizzare l'API client di connessione Desktop remoto broker](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





