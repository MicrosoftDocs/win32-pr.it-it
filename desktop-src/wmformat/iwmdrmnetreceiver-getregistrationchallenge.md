---
title: Metodo IWMDRMNetReceiver GetRegistrationChallenge (Wmdrmsdk.h)
description: Il metodo GetRegistrationChallenge genera un messaggio Windows richiesta di registrazione di Media DRM per i dispositivi di rete.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Metodo GetRegistrationChallenge per Windows Media Format
- Metodo GetRegistrationChallenge windows Media Format , interfaccia IWMDRMNetReceiver
- Metodo GetRegistrationChallenge dell'interfaccia IWMDRMNetReceiver per Windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701036"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Metodo IWMDRMNetReceiver::GetRegistrationChallenge

Il **metodo GetRegistrationChallenge** genera un messaggio Windows richiesta di registrazione di Media DRM per i dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbRegistrationChallenge* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo della richiesta di richiesta generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree.**

</dd> <dt>

*pcbRegistrationChallenge* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della richiesta di registrazione in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





