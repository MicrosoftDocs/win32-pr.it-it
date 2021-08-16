---
title: Metodo IWMDRMDevice GetSecureClockChallenge
description: Il metodo GetSecureClockChallenge recupera il risultato della verifica dell'orologio sicuro.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Metodo GetSecureClockChallenge windows Media Device Manager
- Metodo GetSecureClockChallenge windows Media Device Manager , interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957251"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>Metodo IWMDRMDevice::GetSecureClockChallenge

Il **metodo GetSecureClockChallenge** recupera il risultato della verifica dell'orologio sicuro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbChallenge* \[ Cambio\]
</dt> <dd>

Recupero del risultato della richiesta.

</dd> <dt>

*pcbChallenge* \[ Cambio\]
</dt> <dd>

Dimensioni in byte del risultato della richiesta di richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

 

 





