---
title: Metodo IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: Il metodo SetLicenseChallenge elabora una richiesta di licenza inviata da un DRM di Windows Media per i dispositivi di rete Receiver.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Metodo SetLicenseChallenge Windows Media Format
- Metodo SetLicenseChallenge Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo SetLicenseChallenge
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
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325551"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Metodo IWMDRMNetTransmitter:: SetLicenseChallenge

Il metodo **SetLicenseChallenge** elabora una richiesta di licenza inviata da un DRM di Windows Media per i dispositivi di rete Receiver.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbLicenseChallenge* \[ in\]
</dt> <dd>

Puntatore ai dati di richiesta della licenza inviati da un ricevitore.

</dd> <dt>

*cbLicenseChallenge* \[ in\]
</dt> <dd>

Dimensioni in byte della richiesta di verifica delle licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se questo metodo ha esito positivo, le chiamate successive agli altri metodi di **IWMDRMNetTransmitter** utilizzeranno le informazioni nella richiesta elaborata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





