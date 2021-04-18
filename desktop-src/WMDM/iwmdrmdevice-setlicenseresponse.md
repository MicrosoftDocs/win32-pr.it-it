---
title: Metodo IWMDRMDevice viene chiamato SetLicenseResponse
description: Il metodo viene chiamato SetLicenseResponse imposta la risposta della licenza.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Metodo viene chiamato SetLicenseResponse Windows Media Gestione dispositivi
- Metodo viene chiamato SetLicenseResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo viene chiamato SetLicenseResponse
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
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327398"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>Metodo IWMDRMDevice:: viene chiamato SetLicenseResponse

Il metodo **viene chiamato SetLicenseResponse** imposta la risposta della licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbResponse* \[ in\]
</dt> <dd>

Specifica la risposta da impostare.

</dd> <dt>

*cbResponse* \[ in\]
</dt> <dd>

Dimensione della risposta in byte.

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

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





