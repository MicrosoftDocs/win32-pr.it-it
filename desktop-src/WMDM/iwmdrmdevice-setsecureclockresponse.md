---
title: Metodo IWMDRMDevice SetSecureClockResponse
description: Il metodo SetSecureClockResponse imposta la risposta di clock protetto.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Metodo SetSecureClockResponse Windows Media Gestione dispositivi
- Metodo SetSecureClockResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo SetSecureClockResponse
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
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324878"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Metodo IWMDRMDevice:: SetSecureClockResponse

Il metodo **SetSecureClockResponse** imposta la risposta di clock protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbResponse* \[ in\]
</dt> <dd>

Risposta di clock sicuro da impostare.

</dd> <dt>

*cbResponse* \[ in\]
</dt> <dd>

Dimensione specificata, in byte, della risposta del clock protetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





