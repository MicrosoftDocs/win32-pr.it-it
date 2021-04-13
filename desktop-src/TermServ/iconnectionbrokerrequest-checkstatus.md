---
title: Metodo IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Chiamato per determinare lo stato di una richiesta asincrona.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CheckStatus
- Metodo CheckStatus Servizi Desktop remoto, interfaccia IConnectionBrokerRequest
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto, metodo CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400884"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>Metodo IConnectionBrokerRequest:: CheckStatus

Chiamato per determinare lo stato di una richiesta asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReqStatus* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un valore dell'enumerazione [**\_ \_ dello stato della richiesta CB**](cb-request-status.md) che indica lo stato della richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





