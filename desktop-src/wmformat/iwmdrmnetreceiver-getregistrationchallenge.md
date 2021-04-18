---
title: Metodo IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: Il metodo GetRegistrationChallenge genera un messaggio di verifica della registrazione per i dispositivi di rete DRM di Windows Media.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Metodo GetRegistrationChallenge Windows Media Format
- Metodo GetRegistrationChallenge Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo GetRegistrationChallenge
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
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331563"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Metodo IWMDRMNetReceiver:: GetRegistrationChallenge

Il metodo **GetRegistrationChallenge** genera un messaggio di verifica della registrazione per i dispositivi di rete DRM di Windows Media.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbRegistrationChallenge* \[ out\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo della richiesta generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbRegistrationChallenge* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni in byte della richiesta di registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





