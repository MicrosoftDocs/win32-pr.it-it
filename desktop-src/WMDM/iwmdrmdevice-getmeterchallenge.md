---
title: Metodo IWMDRMDevice GetMeterChallenge
description: Il metodo GetMeterChallenge recupera la sfida di misurazione.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Metodo GetMeterChallenge windows Media Device Manager
- Metodo GetMeterChallenge windows Media Device Manager, interfaccia IWMDRMDevice
- Metodo GetMeterChallenge dell'interfaccia IWMDRMDevice di Windows Media Device Manager
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
ms.openlocfilehash: 8ccccf8ffe17bdcbf25c89830e34e7a52294a6c661bc4b7d9193afd215246cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766631"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>Metodo IWMDRMDevice::GetMeterChallenge

Il **metodo GetMeterChallenge** recupera la sfida di misurazione.

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

*bstrMeterCert* \[ Pollici\]
</dt> <dd>

Certificato di misurazione inviato dal proprietario del contenuto al computer host per la raccolta dei dati di misurazione associati nel dispositivo

</dd> <dt>

*ppbMeterChallenge* \[ Cambio\]
</dt> <dd>

È stato recuperato il risultato della sfida di misurazione.

</dd> <dt>

*pcbMeterChallenge* \[ Cambio\]
</dt> <dd>

Dimensioni della richiesta di misurazione, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

I dati di misurazione vengono raccolti e archiviati nell'archivio dati DRM nel dispositivo per il contenuto con la misurazione abilitata. Verranno registrate azioni come la riproduzione. Quando viene chiamata questa funzione, il dispositivo raccoglie i dati di misurazione nell'archivio dati DRM sotto forma di documento XML e li invia al computer host. Se sono presenti troppi dati, vengono inviati in più fasi.

Quando il computer host riceve i dati di misurazione, invia i dati tramite Internet all'URL specificato nel certificato di misurazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





