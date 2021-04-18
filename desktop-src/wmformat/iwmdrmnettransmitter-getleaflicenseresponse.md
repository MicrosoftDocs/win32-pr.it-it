---
title: Metodo IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: Il metodo GetLeafLicenseResponse genera un messaggio di risposta di licenza foglia.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Metodo GetLeafLicenseResponse Windows Media Format
- Metodo GetLeafLicenseResponse Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325552"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>Metodo IWMDRMNetTransmitter:: GetLeafLicenseResponse

Il metodo **GetLeafLicenseResponse** genera un messaggio di risposta di licenza foglia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ in\]
</dt> <dd>

Identificatore di chiave con codifica base64 da usare per la nuova licenza foglia. L'identificatore di chiave deve essere un valore GUID generato in modo casuale.

</dd> <dt>

*ppolicy* \[ in\]
</dt> <dd>

Puntatore alla struttura [**dei \_ criteri WMDRMNET**](wmdrmnet-policy.md) che definisce i criteri da usare per la licenza foglia.

</dd> <dt>

*ppIWMDRMEncrypt* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IWMDRMEncrypt**](iwmdrmencrypt.md) che può essere utilizzata per crittografare i dati per la nuova licenza foglia.

</dd> <dt>

*ppbLicenseResponse* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve l'indirizzo della risposta di licenza generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della risposta di licenza, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt> </dl> | È necessario un elenco di revoche di contenuti aggiornato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





