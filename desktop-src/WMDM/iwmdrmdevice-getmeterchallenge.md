---
title: Metodo IWMDRMDevice GetMeterChallenge
description: Il metodo GetMeterChallenge recupera la richiesta di misurazione.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Metodo GetMeterChallenge Windows Media Gestione dispositivi
- Metodo GetMeterChallenge Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324120"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>Metodo IWMDRMDevice:: GetMeterChallenge

Il metodo **GetMeterChallenge** recupera la richiesta di misurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrMeterCert* \[ in\]
</dt> <dd>

Certificato di misurazione inviato dal proprietario del contenuto al computer host per la raccolta dei dati di misurazione associati nel dispositivo

</dd> <dt>

*ppbMeterChallenge* \[ out\]
</dt> <dd>

Risultato della richiesta di misurazione recuperato.

</dd> <dt>

*pcbMeterChallenge* \[ out\]
</dt> <dd>

Dimensioni in byte della richiesta di misurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

I dati di misurazione vengono raccolti e archiviati nell'archivio dati DRM sul dispositivo per il contenuto con misurazione abilitata. Verranno registrate azioni come Play. Quando questa funzione viene chiamata, il dispositivo raccoglie i dati di misurazione nell'archivio dati DRM sotto forma di documento XML e lo invia a Hostcomputer. Se la quantità di dati è eccessiva, viene inviata in fasi.

Quando il computer host riceve i dati di controllo, invia i dati tramite Internet all'URL specificato nel certificato di misurazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





