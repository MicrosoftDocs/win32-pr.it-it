---
title: Metodo IWMDRMDevice SetSecureClockResponse
description: Il metodo SetSecureClockResponse imposta la risposta dell'orologio protetto.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Metodo SetSecureClockResponse in Gestione dispositivi multimediali
- Metodo SetSecureClockResponse windows Media Device Manager, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af9dae5e49240ef0095f499cf8abe34d6931caf7c36cf0ec7fc6908c9821a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031861"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Metodo IWMDRMDevice::SetSecureClockResponse

Il **metodo SetSecureClockResponse** imposta la risposta dell'orologio protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbResponse* \[ Pollici\]
</dt> <dd>

Risposta dell'orologio sicuro da impostare.

</dd> <dt>

*cbResponse* \[ Pollici\]
</dt> <dd>

Dimensione specificata della risposta dell'orologio protetto, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





