---
title: Metodo IWMDRMNetTransmitter SetLicenseChallenge (Wmdrmsdk.h)
description: Il metodo SetLicenseChallenge elabora una richiesta di licenza inviata da un ricevitore Windows Media DRM per dispositivi di rete.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Metodo SetLicenseChallenge windows Media Format
- Metodo SetLicenseChallenge windows Media Format , interfaccia IWMDRMNetTransmitter
- Metodo SetLicenseChallenge dell'interfaccia IWMDRMNetTransmitter windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027569"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Metodo IWMDRMNetTransmitter::SetLicenseChallenge

Il **metodo SetLicenseChallenge** elabora una richiesta di licenza inviata da un ricevitore Windows Media DRM per dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbLicenseChallenge* \[ Pollici\]
</dt> <dd>

Puntatore ai dati di richiesta di licenza inviati da un ricevitore.

</dd> <dt>

*cbLicenseChallenge* \[ Pollici\]
</dt> <dd>

Dimensioni della richiesta di licenza in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se questo metodo ha esito positivo, le chiamate successive agli altri metodi **di IWMDRMNetTransmitter** useranno le informazioni nella richiesta elaborata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





