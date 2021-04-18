---
title: Funzione CBCreateClientInstance (Cbclient. h)
description: Crea un'istanza del client RPC di Connessione Desktop remoto broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione CBCreateClientInstance
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
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333646"
---
# <a name="cbcreateclientinstance-function"></a>CBCreateClientInstance (funzione)

Crea un'istanza del client RPC di Connessione Desktop remoto broker.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Versione* \[ di in\]
</dt> <dd>

Specifica la versione dell'interfaccia client di Connessione Desktop remoto broker richiesta. Deve corrispondere al valore seguente.

<dt>

1
</dt> <dd>

Versione 1 del client di Connessione Desktop remoto broker.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a interfaccia [**IConnectionBrokerClient**](iconnectionbrokerclient.md) che riceve l'oggetto client di connessione Desktop remoto broker.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cbclient. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





