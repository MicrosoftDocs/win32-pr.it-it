---
title: Metodo IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: Il metodo ProcessLicenseResponse elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Metodo ProcessLicenseResponse Windows Media Format
- Metodo ProcessLicenseResponse Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325555"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>IWMDRMNetReceiver::P metodo rocessLicenseResponse

Il metodo **ProcessLicenseResponse** elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbLicenseResponse* \[ in\]
</dt> <dd>

Risposta di licenza ricevuta dal trasmettitore.

</dd> <dt>

*cbLicenseResponse* \[ in\]
</dt> <dd>

Dimensione della risposta in byte.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve l'indirizzo della rappresentazione di licenza interna per la licenza contenuta nel messaggio di risposta della licenza. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**. Questo parametro può essere impostato su **null** se la rappresentazione della licenza non è necessaria.

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della rappresentazione di licenza. Deve essere impostato su **null** se *ppbWMDRMNetLicenseRepresentation* è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt> </dl> | È necessario un elenco di revoche di contenuti aggiornato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

La risposta di licenza elaborata utilizzando questo metodo deve corrispondere all'ultima richiesta di licenza generata sul computer client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





