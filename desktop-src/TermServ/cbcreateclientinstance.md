---
title: Funzione CBCreateClientInstance (Cbclient.h)
description: Crea un'istanza del client RPC Connessione Desktop remoto Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Funzione CBCreateClientInstance Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b0873fac5b33370333ec8f5774e5b8dbbcd896f6afb9777a6dd74dd6913dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610148"
---
# <a name="cbcreateclientinstance-function"></a>Funzione CBCreateClientInstance

Crea un'istanza del client RPC Connessione Desktop remoto Broker.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Versione* \[ Pollici\]
</dt> <dd>

Specifica la versione dell'Connessione Desktop remoto client broker richiesta. Deve essere il valore seguente.

<dt>

1
</dt> <dd>

Versione 1 del client Connessione Desktop remoto Broker.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ Cambio\]
</dt> <dd>

Indirizzo di un [**puntatore a interfaccia IConnectionBrokerClient**](iconnectionbrokerclient.md) che riceve l'Connessione Desktop remoto client di Broker.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cbclient.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





