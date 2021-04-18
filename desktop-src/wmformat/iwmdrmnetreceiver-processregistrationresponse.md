---
title: Metodo IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: Il metodo ProcessRegistrationResponse elabora una risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Metodo ProcessRegistrationResponse Windows Media Format
- Metodo ProcessRegistrationResponse Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325554"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>IWMDRMNetReceiver::P metodo rocessRegistrationResponse

Il metodo **ProcessRegistrationResponse** elabora una risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbRegistrationResponse* \[ in\]
</dt> <dd>

Risposta di registrazione ricevuta dal trasmettitore.

</dd> <dt>

*cbRegistrationResponse* \[ in\]
</dt> <dd>

Dimensioni in byte della risposta di registrazione.

</dd> <dt>

*ppunkCancellationCookie* \[ out\]
</dt> <dd>

Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona. Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. al termine dell'elaborazione, l'evento MEProximityCompleted viene inviato all'interfaccia **IMFMediaEventGenerator** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





