---
title: Metodo IWMDRMNetTransmitter GetLeafLicenseResponse (Wmdrmsdk.h)
description: Il metodo GetLeafLicenseResponse genera un messaggio di risposta di licenza foglia.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Metodo GetLeafLicenseResponse windows Media Format
- Metodo GetLeafLicenseResponse in formato Windows Media, interfaccia IWMDRMNetTransmitter
- Metodo GetLeafLicenseResponse dell'interfaccia IWMDRMNetTransmitter windows Media Format
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
ms.openlocfilehash: aff470341c3227782d0d34cbdd2ca2a4a51a4cb1b6214b81ea2ea9a384b29ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084831"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>Metodo IWMDRMNetTransmitter::GetLeafLicenseResponse

Il **metodo GetLeafLicenseResponse** genera un messaggio di risposta di licenza foglia.

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

*bstrKID* \[ Pollici\]
</dt> <dd>

Identificatore di chiave con codifica Base64 da usare per la nuova licenza foglia. L'identificatore di chiave deve essere un valore GUID generato in modo casuale.

</dd> <dt>

*pPolicy* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura DI \_ CRITERI WMDRMNET**](wmdrmnet-policy.md) che definisce i criteri da usare per la licenza foglia.

</dd> <dt>

*ppIWMDRMEncrypt* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IWMDRMEncrypt**](iwmdrmencrypt.md) che può essere usata per crittografare i dati per la nuova licenza foglia.

</dd> <dt>

*ppbLicenseResponse* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve l'indirizzo della risposta di licenza generata. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree.**

</dd> <dt>

*pcbLicenseResponse* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni della risposta della licenza, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ TOO \_ SMALL**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





