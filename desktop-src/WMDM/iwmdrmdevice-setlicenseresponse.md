---
title: Metodo IWMDRMDevice SetLicenseResponse
description: Il metodo SetLicenseResponse imposta la risposta della licenza.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Metodo SetLicenseResponse windows Media Device Manager
- Metodo SetLicenseResponse windows Media Device Manager, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161732002378449f196fdf83c4b880fcc2c02d345a0b08c6e6a464b81acb1dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055719"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>Metodo IWMDRMDevice::SetLicenseResponse

Il **metodo SetLicenseResponse** imposta la risposta della licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbResponse* \[ Pollici\]
</dt> <dd>

Specifica la risposta da impostare.

</dd> <dt>

*cbResponse* \[ Pollici\]
</dt> <dd>

Dimensioni della risposta, in byte.

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

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





