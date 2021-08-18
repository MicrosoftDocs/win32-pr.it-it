---
title: Metodo IWMDRMDevice GetDeviceCertificate
description: Il metodo GetDeviceCertificate recupera il certificato del dispositivo.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Metodo GetDeviceCertificate in Gestione dispositivi multimediali di Windows
- Metodo GetDeviceCertificate windows Media Device Manager, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo GetDeviceCertificate
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299233ff4344f44535933221141534ab2b0173ba54e47c9cc340020a2f462eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619821"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a>Metodo IWMDRMDevice::GetDeviceCertificate

Il **metodo GetDeviceCertificate** recupera il certificato del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrDevCert* \[ Cambio\]
</dt> <dd>

Puntatore a un **BSTR** contenente il certificato del dispositivo recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





