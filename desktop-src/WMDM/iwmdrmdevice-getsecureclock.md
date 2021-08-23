---
title: Metodo IWMDRMDevice GetSecureClock
description: Il metodo GetSecureClock recupera l'orologio sicuro, quindi è possibile applicare licenze basate sull'ora.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Metodo GetSecureClock windows Media Device Manager
- Metodo GetSecureClock windows Media Device Manager , interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo GetSecureClock
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
ms.openlocfilehash: aa9494a594a396550028f083cc2b646f2093f6369ab27ae5494bf70c13628d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619781"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>Metodo IWMDRMDevice::GetSecureClock

Il **metodo GetSecureClock** recupera l'orologio sicuro, quindi è possibile applicare licenze basate sull'ora.

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

*ppbSecureClock* \[ Cambio\]
</dt> <dd>

Recupero dell'orologio sicuro.

</dd> <dt>

*pcbSecureClock* \[ Cambio\]
</dt> <dd>

Dimensioni dell'orologio protetto, in byte.

</dd> <dt>

*pdwFlags* \[ Cambio\]
</dt> <dd>

Flag di stato del dispositivo. Questo valore deve essere uno dei flag seguenti.



| Flag                     | Descrizione                            |
|--------------------------|----------------------------------------|
| DISPOSITIVO WMDRM \_ \_ ISWMDRM   | Il dispositivo supporta Windows DRM multimediale. |
| WMDRM \_ DEVICE \_ NEEDCLOCK | Il dispositivo richiede l'orologio.                |
| DISPOSITIVO WMDRM \_ \_ REVOCATO   | Il dispositivo è stato revocato.           |



 

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

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





