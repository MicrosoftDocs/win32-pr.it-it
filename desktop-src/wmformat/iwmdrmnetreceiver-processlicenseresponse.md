---
title: Metodo IWMDRMNetReceiver ProcessLicenseResponse (Wmdrmsdk.h)
description: Il metodo ProcessLicenseResponse elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Metodo ProcessLicenseResponse windows Media Format
- Metodo ProcessLicenseResponse windows Media Format , interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver windows Media Format , metodo ProcessLicenseResponse
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
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700825"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>Metodo IWMDRMNetReceiver::P rocessLicenseResponse

Il **metodo ProcessLicenseResponse** elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.

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

*pbLicenseResponse* \[ Pollici\]
</dt> <dd>

Risposta di licenza ricevuta dal trasmettitore.

</dd> <dt>

*cbLicenseResponse* \[ Pollici\]
</dt> <dd>

Dimensioni della risposta in byte.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve l'indirizzo della rappresentazione della licenza interna per la licenza contenuta nel messaggio di risposta della licenza. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**. Questo parametro può essere impostato su **NULL se** la rappresentazione della licenza non è necessaria.

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della rappresentazione della licenza. Deve essere impostato su **NULL** se *ppbWMDRMNetLicenseRepresentation* è **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

La risposta di licenza elaborata con questo metodo deve corrispondere all'ultima richiesta di licenza generata nel computer client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





