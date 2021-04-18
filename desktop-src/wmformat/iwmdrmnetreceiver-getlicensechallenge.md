---
title: Metodo IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: Il metodo GetLicenseChallenge genera una richiesta di licenza di Windows Media DRM per i dispositivi di rete che può essere inviata a un trasmettitore quando richiede contenuto protetto.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Metodo GetLicenseChallenge Windows Media Format
- Metodo GetLicenseChallenge Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325556"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>Metodo IWMDRMNetReceiver:: GetLicenseChallenge

Il metodo **GetLicenseChallenge** genera una richiesta di licenza di Windows Media DRM per i dispositivi di rete che può essere inviata a un trasmettitore quando richiede contenuto protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAction* \[ in\]
</dt> <dd>

Azione per la quale generare la richiesta di verifica.

</dd> <dt>

*ppbLicenseChallenge* \[ out\]
</dt> <dd>

Indirizzo di un puntatore impostato sull'indirizzo della richiesta generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseChallenge* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della richiesta di licenza in byte.

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

[**IWMDRMNetReceiver::P rocessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





