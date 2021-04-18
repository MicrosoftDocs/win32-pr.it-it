---
title: Metodo IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: Il metodo GetRootLicenseResponse genera un messaggio di risposta di licenza radice.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Metodo GetRootLicenseResponse Windows Media Format
- Metodo GetRootLicenseResponse Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327463"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>Metodo IWMDRMNetTransmitter:: GetRootLicenseResponse

Il metodo **GetRootLicenseResponse** genera un messaggio di risposta di licenza radice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ in\]
</dt> <dd>

Identificatore di chiave con codifica base64 da usare per la nuova licenza radice. L'identificatore di chiave deve essere un valore GUID generato in modo casuale.

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

La licenza radice generata viene creata usando le informazioni dei dati di richiesta della licenza, elaborati per l'interfaccia chiamando [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

La licenza radice viene utilizzata per la generazione di licenze foglia, che viene eseguita chiamando il metodo [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) . L'interfaccia **IWMDRMNetTransmitter** gestisce una copia della licenza radice per tale uso.

La licenza radice creata chiamando questo metodo non dispone di alcun criterio ed è configurata in modo che non possa essere resa persistente nel dispositivo di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





