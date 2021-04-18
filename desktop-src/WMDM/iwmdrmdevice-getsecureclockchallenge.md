---
title: Metodo IWMDRMDevice GetSecureClockChallenge
description: Il metodo GetSecureClockChallenge Recupera il risultato della verifica del clock protetto.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Metodo GetSecureClockChallenge Windows Media Gestione dispositivi
- Metodo GetSecureClockChallenge Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetSecureClockChallenge
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
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324111"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>Metodo IWMDRMDevice:: GetSecureClockChallenge

Il metodo **GetSecureClockChallenge** Recupera il risultato della verifica del clock protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbChallenge* \[ out\]
</dt> <dd>

Risultato della richiesta di verifica recuperato.

</dd> <dt>

*pcbChallenge* \[ out\]
</dt> <dd>

Dimensioni del risultato della richiesta, in byte.

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

 

 





