---
title: Metodo IWMDRMNetTransmitter GetRootLicenseResponse (Wmdrmsdk.h)
description: Il metodo GetRootLicenseResponse genera un messaggio di risposta della licenza radice.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Metodo GetRootLicenseResponse in formato Windows Media
- Metodo GetRootLicenseResponse windows Media Format , interfaccia IWMDRMNetTransmitter
- IWMDRMNetTransmitter interface windows Media Format , Metodo GetRootLicenseResponse
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
ms.openlocfilehash: de89389163a9eae66a0dcda14dd6b9699d3db9650140cceac6498b2ab77a4e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707931"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>Metodo IWMDRMNetTransmitter::GetRootLicenseResponse

Il **metodo GetRootLicenseResponse** genera un messaggio di risposta della licenza radice.

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

*bstrKID* \[ Pollici\]
</dt> <dd>

Identificatore di chiave con codifica Base64 da usare per la nuova licenza radice. L'identificatore di chiave deve essere un valore GUID generato in modo casuale.

</dd> <dt>

*ppbLicenseResponse* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve l'indirizzo della risposta di licenza generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della risposta della licenza, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

La licenza radice generata viene creata usando le informazioni dei dati di richiesta di licenza, elaborate per l'interfaccia chiamando [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

La licenza radice viene usata nella generazione di licenze foglia, che viene eseguita chiamando il [**metodo GetLeafLicenseResponse.**](iwmdrmnettransmitter-getleaflicenseresponse.md) **L'interfaccia IWMDRMNetTransmitter** mantiene una copia della licenza radice per tale uso.

La licenza radice creata chiamando questo metodo non dispone di criteri e viene configurata in modo che non possa essere resa persistente nel dispositivo ricevente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





