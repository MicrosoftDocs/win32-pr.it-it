---
title: Metodo IWMDRMDevice GetSecureClock
description: Il metodo GetSecureClock Recupera il clock sicuro, quindi è possibile applicare licenze basate sul tempo.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Metodo GetSecureClock Windows Media Gestione dispositivi
- Metodo GetSecureClock Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324117"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>Metodo IWMDRMDevice:: GetSecureClock

Il metodo **GetSecureClock** Recupera il clock sicuro, quindi è possibile applicare licenze basate sul tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbSecureClock* \[ out\]
</dt> <dd>

Clock protetto recuperato.

</dd> <dt>

*pcbSecureClock* \[ out\]
</dt> <dd>

Dimensioni del clock sicuro, in byte.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Flag di stato del dispositivo. Questo valore deve essere uno dei flag seguenti.



| Flag                     | Descrizione                            |
|--------------------------|----------------------------------------|
| \_ISWMDRM del dispositivo WMDRM \_   | Il dispositivo supporta Windows Media DRM. |
| \_NEEDCLOCK del dispositivo WMDRM \_ | Il dispositivo deve essere clock.                |
| il dispositivo WMDRM è stato \_ \_ revocato   | Il dispositivo è stato revocato.           |



 

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

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





